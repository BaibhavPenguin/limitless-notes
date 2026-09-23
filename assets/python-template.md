<a href="#" class="py-link">Go Back</a>
<link rel="stylesheet" href="./styles/python.css">
<div class="py-island">
  <div class="py-island-header">
    <div class="py-header-left">
      <span class="py-island-title">Python Sandbox</span>
      <div class="py-status-badge">
        <span class="py-status-dot"></span>
        <span class="py-status-text">Loading...</span>
      </div>
    </div>
    <button class="py-run-btn" onclick="runPythonCode(this)">▶ Run</button>
  </div>
  <div class="py-island-body">
    <div class="pysource">
      <textarea spellcheck="false" placeholder="Write Python code here..." oninput="syncPyHighlight(this); syncPyScroll(this);" onscroll="syncPyScroll(this)"></textarea>
      <pre><code class="language-python"></code></pre>
    </div>
    <div class="pyterm">
      <pre class="py-output"></pre>
    </div>
  </div>
</div>

<!--Run Button Script-->
<script>
  // Sync Prism syntax highlighting with text area
  function syncPyHighlight(textarea) {
    const pysource = textarea.closest('.pysource');
    const codeEl = pysource.querySelector('pre code');
    if (codeEl && window.Prism) {
      codeEl.textContent = textarea.value + (textarea.value.endsWith('\n') ? ' ' : '');
      Prism.highlightElement(codeEl);
    }
  }

  // Keep scroll position in sync between textarea and highlighted overlay
  function syncPyScroll(textarea) {
    const pysource = textarea.closest('.pysource');
    const preEl = pysource.querySelector('pre');
    if (preEl) {
      preEl.scrollTop = textarea.scrollTop;
      preEl.scrollLeft = textarea.scrollLeft;
    }
  }

  // Execute code via the global shared Web Worker
  function runPythonCode(buttonEl) {
    const island = buttonEl.closest('.py-island');
    const sourceArea = island.querySelector('.pysource textarea');
    const outputPre = island.querySelector('.pyterm pre');

    // Use the global persistent shared worker
    if (!sourceArea || !outputPre || !window.__sharedPyWorker) {
      if (outputPre) outputPre.textContent = 'Error: Worker not initialized yet.';
      return;
    }

    const code = sourceArea.value;
    buttonEl.disabled = true;
    const originalText = buttonEl.innerHTML;
    buttonEl.innerHTML = 'Running...';
    outputPre.className = 'py-output';
    outputPre.textContent = 'Executing...';

    // Route response listener directly to shared worker
    window.__sharedPyWorker.onmessage = (e) => {
      // Ignore background readiness ping messages
      if (e.data.type === 'ready') {
        if (typeof updatePyodideBadges === 'function') updatePyodideBadges(true);
        return;
      }

      buttonEl.disabled = false;
      buttonEl.innerHTML = originalText;

      if (e.data.success) {
        outputPre.textContent = e.data.output || '(Execution completed with no output)';
      } else {
        outputPre.className = 'py-output py-err';
        outputPre.textContent = e.data.error;
      }
    };

    // Send code payload to persistent worker
    window.__sharedPyWorker.postMessage({ type: 'run', code });
  }

  // Initial syntax highlight pass for default text on page render
  document.querySelectorAll('.pysource textarea').forEach(textarea => {
    syncPyHighlight(textarea);
    // Sync status badge state if worker was already loaded
    if (window.__isPyodideReady && typeof updatePyodideBadges === 'function') {
      updatePyodideBadges(true);
    }
  });
</script>