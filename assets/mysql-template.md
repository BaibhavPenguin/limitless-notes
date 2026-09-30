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
      <button class="mysql-enter-btn" onclick="runMySQLCode(this)">⏎ Enter</button>
    </div>
    <div class="mysql-island-body">
      <div class="mysqlsource">
        <div class="mysql-gutter">1</div>
        <textarea 
          spellcheck="false" 
          placeholder="Enter SQL statements here..." 
          oninput="updateCodeGutter(this)" 
          onscroll="syncCodeGutterScroll(this)"
        >CREATE TABLE users (id INT PRIMARY KEY, name VARCHAR(50));
INSERT INTO users VALUES (1, 'Limitless'), (2, 'MariaDB');
SELECT * FROM users;</textarea>
      </div>
      <div class="mysqlterm">
        <pre class="mysql-output"></pre>
      </div>
    </div>
  </div>
</div>