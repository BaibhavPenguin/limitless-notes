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
      <textarea 
        spellcheck="false" 
        placeholder="Write Python code here..." 
        oninput="syncPyHighlight(this); syncPyScroll(this);" 
        onscroll="syncPyScroll(this)"
      >print("Hello, World!")</textarea>
      <pre><code class="language-python"></code></pre>
    </div>
    <div class="pyterm">
      <pre class="py-output"></pre>
    </div>
  </div>
</div>

<script>
  function updatePyodideBadges(isReady) {
    document.querySelectorAll('.py-status-badge').forEach(badge => {
      if (isReady) {
        badge.classList.add('ready');
        badge.querySelector('.py-status-text').textContent = 'Python Ready';
      } else {
        badge.classList.remove('ready');
        badge.querySelector('.py-status-text').textContent = 'Loading...';
      }
    });
  }

  function syncPyHighlight(textarea) {
    const pysource = textarea.closest('.pysource');
    const codeEl = pysource.querySelector('pre code');
    if (!codeEl) return;

    codeEl.textContent = textarea.value + (textarea.value.endsWith('\n') ? ' ' : '');
    
    if (window.Prism) {
      Prism.highlightElement(codeEl);
    }
  }

  function syncPyScroll(textarea) {
    const pysource = textarea.closest('.pysource');
    const preEl = pysource.querySelector('pre');
    if (preEl) {
      preEl.scrollTop = textarea.scrollTop;
      preEl.scrollLeft = textarea.scrollLeft;
    }
  }

  function runPythonCode(buttonEl) {
    const island = buttonEl.closest('.py-island');
    const sourceArea = island.querySelector('.pysource textarea');
    const outputPre = island.querySelector('.pyterm pre');

    if (!sourceArea || !outputPre) return;

    if (!window.__sharedPyWorker) {
      outputPre.className = 'py-output py-err';
      outputPre.textContent = 'Error: Shared Pyodide worker script not found on page.';
      return;
    }

    const code = sourceArea.value;
    buttonEl.disabled = true;
    const originalText = buttonEl.innerHTML;
    buttonEl.innerHTML = 'Running...';
    outputPre.className = 'py-output';
    outputPre.textContent = 'Executing...';

    const handleResult = (e) => {
      if (e.data.type === 'ready') {
        window.__isPyodideReady = true;
        updatePyodideBadges(true);
        return;
      }

      if (e.data.type === 'result') {
        window.__sharedPyWorker.removeEventListener('message', handleResult);
        buttonEl.disabled = false;
        buttonEl.innerHTML = originalText;

        if (e.data.success) {
          outputPre.textContent = e.data.output || '(Execution completed with no output)';
        } else {
          outputPre.className = 'py-output py-err';
          outputPre.textContent = e.data.error;
        }
      }
    };

    window.__sharedPyWorker.addEventListener('message', handleResult);
    window.__sharedPyWorker.postMessage({ type: 'run', code });
  }

  // Mount syntax highlighting and sync initial status
  document.querySelectorAll('.pysource textarea').forEach(textarea => {
    syncPyHighlight(textarea);
  });

  if (window.__isPyodideReady) {
    updatePyodideBadges(true);
  }
</script>