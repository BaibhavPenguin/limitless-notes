<link rel="stylesheet" href="./styles/mysql.css">
<div class="code-sandbox-wrapper mysql-sandbox-wrapper">
  <div class="mysql-status-badge">
    <span class="mysql-status-dot"></span>
    <span class="mysql-status-text">Waiting</span>
  </div>

  <div class="mysql-island">
    <div class="mysql-island-header">
      <div class="mysql-header-left">
        <span class="mysql-island-title">MySQL Sandbox</span>
      </div>
      <div class="mysql-header-actions">
        <button class="mysql-clear-btn" onclick="clearMySQLTerminal(this)">Clear</button>
        <button class="mysql-enter-btn" onclick="runMySQLCode(this)">⏎ Enter</button>
      </div>
    </div>
    
    <div class="mysql-island-body">
      <!-- Output Window (Top) -->
      <div class="mysqlterm">
        <pre class="mysql-output"></pre>
      </div>

      <!--Line Editor (Bottom)-->
      <div class="mysqlsource">
        <textarea 
          class="mysql-line-edit"
          rows="1"
          spellcheck="false" 
          placeholder="Enter SQL statements here (e.g. SHOW DATABASES;)..." 
          oninput="autoExpandSQLEdit(this)" 
          onkeydown="handleSQLKeyDown(event, this)"
        ></textarea>
      </div>
    </div>
  </div>
</div>