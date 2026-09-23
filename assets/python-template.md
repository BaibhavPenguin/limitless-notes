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
      <textarea spellcheck="false" placeholder="Write Python code here...">print("Hello, World!")</textarea>
    </div>
    <div class="pyterm">
      <pre class="py-output"></pre>
    </div>
  </div>
</div>