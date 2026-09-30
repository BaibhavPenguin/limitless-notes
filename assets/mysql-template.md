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
</div>
<div class="mysql-island-body">
<!-- Output Window (Terminal Black) -->
<div class="mysqlterm">
<pre class="mysql-output">Welcome to the MariaDB monitor. Commands end with ;</pre>
</div>
<!-- Line Editor (Middle) -->
<div class="mysqlsource">
<textarea class="mysql-line-edit" rows="1" spellcheck="false" placeholder="Enter SQL statements here (e.g. SHOW DATABASES;)..." oninput="autoExpandSQLEdit(this)" onkeydown="handleSQLKeyDown(event, this)"></textarea>
</div>
<!-- Bottom Actions Bar (Below Line Edit) -->
<div class="mysql-island-footer">
<div class="mysql-footer-hint">Press <span>Enter</span> to run, <span>Shift + Enter</span> for new line</div>
<div class="mysql-footer-actions">
<button class="mysql-btn mysql-clear-btn" onclick="clearMySQLTerminal(this)">Clear</button>
<button class="mysql-btn mysql-enter-btn" onclick="runMySQLCode(this)">⏎ Enter</button>
</div>
</div>
</div>
</div>
</div>