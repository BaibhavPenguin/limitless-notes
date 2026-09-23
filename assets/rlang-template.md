<link rel="stylesheet" href="./styles/rlang.css">
<div class="webr-sandbox-wrapper code-sandbox-wrapper">
  <div class="webr-status-badge">
    <span class="webr-status-dot"></span>
    <span class="webr-status-text">Waiting</span>
  </div>

  <div class="webr-island code-island">
    <div class="webr-island-header code-island-header">
      <div class="webr-header-left code-header-left">
        <span class="webr-island-title code-island-title">R Sandbox</span>
      </div>
      <button class="webr-run-btn" onclick="runWebRCode(this)">▶ Run</button>
    </div>
    <div class="webr-island-body code-island-body">
      <div class="webrsource code-source">
        <div class="webr-gutter code-gutter">1</div>
        <textarea 
          spellcheck="false" 
          placeholder="Write R code here..." 
          oninput="updateCodeGutter(this)" 
          onscroll="syncCodeGutterScroll(this)"
        >x <- c(10, 20, 30, 40)
mean(x)</textarea>
      </div>
      <div class="webrterm code-term">
        <pre class="webr-output"></pre>
      </div>
    </div>
  </div>
</div>