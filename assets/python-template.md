<div class="py-island">
  <div class="py-island-header">
    <span class="py-island-title">Python Sandbox</span>
    <button class="py-run-btn" onclick="runPythonCode(this)">▶ Run</button>
  </div>
  <div class="py-island-body">
    <div class="pysource">
      <textarea spellcheck="false" placeholder="Write Python code here...">import numpy as np
import pandas as pd

# Generate sample data using NumPy
data = np.random.randn(5, 3)

# Create Pandas DataFrame
df = pd.DataFrame(data, columns=['Alpha', 'Beta', 'Gamma'])
print(df)</textarea>
    </div>
    <div class="pyterm">
      <pre class="py-output">Click "Run" to execute python code...</pre>
    </div>
  </div>
</div>

<script>
  function runPythonCode(buttonEl) {
    const island = buttonEl.closest('.py-island');
    const sourceArea = island.querySelector('.pysource textarea');
    const outputPre = island.querySelector('.pyterm pre');

    if (!sourceArea || !outputPre || !window.__pyodideWorkerUrl) return;

    const code = sourceArea.value;
    buttonEl.disabled = true;
    const originalText = buttonEl.innerHTML;
    buttonEl.innerHTML = 'Running...';
    outputPre.className = 'py-output';
    outputPre.textContent = 'Executing...';

    const execWorker = new Worker(window.__pyodideWorkerUrl);

    execWorker.onmessage = (e) => {
      buttonEl.disabled = false;
      buttonEl.innerHTML = originalText;

      if (e.data.success) {
        outputPre.textContent = e.data.output || '(Execution completed with no output)';
      } else {
        outputPre.className = 'py-output py-err';
        outputPre.textContent = e.data.error;
      }
      execWorker.terminate();
    };

    execWorker.postMessage({ code });
  }
</script>