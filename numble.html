<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CIPHERLE</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;700;800&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0a0a0f;
    --surface: #13131a;
    --surface2: #1c1c28;
    --border: #2a2a3d;
    --text: #e8e8f0;
    --text-dim: #6b6b8a;
    --green: #4ade80;
    --green-bg: #14532d;
    --yellow: #fbbf24;
    --yellow-bg: #451a03;
    --gray: #374151;
    --gray-bg: #1f2937;
    --accent: #818cf8;
    --accent2: #f472b6;
    --cell-size: 62px;
    --gap: 6px;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Space Mono', monospace;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    overflow-x: hidden;
  }
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: linear-gradient(var(--border) 1px, transparent 1px), linear-gradient(90deg, var(--border) 1px, transparent 1px);
    background-size: 40px 40px;
    opacity: 0.25;
    pointer-events: none;
  }
  header {
    width: 100%;
    max-width: 500px;
    padding: 20px 16px 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: relative;
    z-index: 1;
  }
  .logo {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 28px;
    letter-spacing: 6px;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  .header-icons { display: flex; gap: 10px; }
  .icon-btn {
    background: var(--surface);
    border: 1px solid var(--border);
    color: var(--text-dim);
    width: 36px;
    height: 36px;
    border-radius: 8px;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 16px;
    transition: all 0.15s;
  }
  .icon-btn:hover { color: var(--text); border-color: var(--accent); background: var(--surface2); }
  .stats-bar {
    display: flex;
    gap: 20px;
    padding: 12px 16px;
    width: 100%;
    max-width: 500px;
    justify-content: center;
    position: relative;
    z-index: 1;
  }
  .stat { display: flex; flex-direction: column; align-items: center; gap: 2px; }
  .stat-value { font-family: 'Syne', sans-serif; font-size: 22px; font-weight: 800; color: var(--accent); }
  .stat-label { font-size: 9px; letter-spacing: 1.5px; color: var(--text-dim); text-transform: uppercase; }
  .stat-sep { width: 1px; background: var(--border); align-self: stretch; margin: 4px 0; }
  .mode-bar {
    display: flex;
    gap: 8px;
    padding: 0 16px 12px;
    width: 100%;
    max-width: 500px;
    justify-content: center;
    position: relative;
    z-index: 1;
  }
  .mode-btn {
    background: var(--surface);
    border: 1px solid var(--border);
    color: var(--text-dim);
    padding: 5px 14px;
    border-radius: 20px;
    cursor: pointer;
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    letter-spacing: 1px;
    transition: all 0.15s;
  }
  .mode-btn.active { background: var(--accent); border-color: var(--accent); color: #000; font-weight: 700; }
  .timer-bar { font-size: 11px; letter-spacing: 2px; color: var(--text-dim); padding-bottom: 8px; position: relative; z-index: 1; }
  .timer-bar span { color: var(--accent2); font-weight: 700; }
  .streak-display { font-size: 11px; letter-spacing: 1px; color: var(--text-dim); padding: 0 16px 4px; text-align: center; position: relative; z-index: 1; }
  .grid-wrapper { position: relative; z-index: 1; padding: 8px 16px; }
  .grid { display: flex; flex-direction: column; gap: var(--gap); }
  .row { display: flex; gap: var(--gap); }
  .cell {
    width: var(--cell-size);
    height: var(--cell-size);
    border: 2px solid var(--border);
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Syne', sans-serif;
    font-size: 26px;
    font-weight: 800;
    color: var(--text);
    background: var(--surface);
    transition: border-color 0.1s;
  }
  .cell.filled { border-color: var(--text-dim); animation: pop 0.1s ease; }
  .cell.active-row { border-color: var(--accent); }
  @keyframes pop { 0%{transform:scale(1)} 50%{transform:scale(1.08)} 100%{transform:scale(1)} }
  .cell.reveal { animation: flip 0.5s ease forwards; }
  @keyframes flip {
    0%{transform:rotateX(0deg)}
    50%{transform:rotateX(90deg);background:var(--surface);border-color:var(--border)}
    100%{transform:rotateX(0deg)}
  }
  .cell.correct { background: var(--green-bg); border-color: var(--green); color: var(--green); }
  .cell.present { background: var(--yellow-bg); border-color: var(--yellow); color: var(--yellow); }
  .cell.absent { background: var(--gray-bg); border-color: var(--gray); color: var(--text-dim); }
  .row.shake { animation: shake 0.4s ease; }
  @keyframes shake { 0%,100%{transform:translateX(0)} 20%{transform:translateX(-8px)} 40%{transform:translateX(8px)} 60%{transform:translateX(-5px)} 80%{transform:translateX(5px)} }
  .message {
    position: fixed;
    top: 80px;
    left: 50%;
    transform: translateX(-50%);
    background: var(--text);
    color: var(--bg);
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 14px;
    letter-spacing: 2px;
    padding: 10px 20px;
    border-radius: 8px;
    z-index: 100;
    pointer-events: none;
    opacity: 0;
    transition: opacity 0.3s;
    white-space: nowrap;
  }
  .message.show { opacity: 1; }
  .numpad { position: relative; z-index: 1; padding: 16px; width: 100%; max-width: 500px; }
  .numpad-grid { display: grid; grid-template-columns: repeat(5, 1fr); gap: 8px; }
  .key {
    background: var(--surface2);
    border: 1px solid var(--border);
    color: var(--text);
    border-radius: 10px;
    padding: 0;
    height: 52px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Syne', sans-serif;
    font-size: 20px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.1s;
    user-select: none;
    -webkit-tap-highlight-color: transparent;
  }
  .key:active, .key.pressing { background: var(--accent); color: #000; transform: scale(0.94); }
  .key.del { font-size: 13px; grid-column: span 2; letter-spacing: 1px; }
  .key.enter {
    font-size: 12px;
    grid-column: span 3;
    letter-spacing: 2px;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    color: #000;
    border-color: transparent;
    font-weight: 700;
  }
  .key.enter:active { opacity: 0.8; transform: scale(0.97); }
  .overlay {
    position: fixed;
    inset: 0;
    background: #0a0a0fcc;
    backdrop-filter: blur(8px);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 200;
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.3s;
  }
  .overlay.show { opacity: 1; pointer-events: all; }
  .modal {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 32px;
    max-width: 360px;
    width: calc(100% - 32px);
    text-align: center;
    transform: translateY(20px);
    transition: transform 0.3s;
  }
  .overlay.show .modal { transform: translateY(0); }
  .modal-emoji { font-size: 52px; margin-bottom: 12px; display: block; }
  .modal-title { font-family: 'Syne', sans-serif; font-size: 26px; font-weight: 800; letter-spacing: 3px; margin-bottom: 6px; }
  .modal-subtitle { color: var(--text-dim); font-size: 12px; letter-spacing: 1.5px; margin-bottom: 20px; }
  .modal-answer {
    font-family: 'Syne', sans-serif;
    font-size: 36px;
    font-weight: 800;
    letter-spacing: 8px;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 20px;
  }
  .modal-emoji-grid {
    font-size: 20px;
    letter-spacing: 2px;
    line-height: 1.8;
    margin-bottom: 20px;
    padding: 12px;
    background: var(--surface2);
    border-radius: 10px;
    border: 1px solid var(--border);
  }
  .modal-buttons { display: flex; gap: 10px; }
  .btn { flex: 1; padding: 12px; border-radius: 10px; border: none; font-family: 'Syne', sans-serif; font-size: 13px; font-weight: 700; letter-spacing: 2px; cursor: pointer; transition: all 0.15s; }
  .btn-primary { background: linear-gradient(135deg, var(--accent), var(--accent2)); color: #000; }
  .btn-secondary { background: var(--surface2); border: 1px solid var(--border); color: var(--text); }
  .btn:hover { opacity: 0.85; transform: translateY(-1px); }
  .settings-modal { text-align: left; }
  .settings-title { font-family: 'Syne', sans-serif; font-size: 18px; font-weight: 800; letter-spacing: 3px; margin-bottom: 20px; text-align: center; }
  .setting-row { display: flex; align-items: center; justify-content: space-between; padding: 12px 0; border-bottom: 1px solid var(--border); }
  .setting-row:last-of-type { border-bottom: none; }
  .setting-label { font-size: 13px; letter-spacing: 0.5px; }
  .setting-desc { font-size: 10px; color: var(--text-dim); margin-top: 2px; letter-spacing: 0.5px; }
  .toggle { width: 44px; height: 24px; background: var(--gray); border-radius: 12px; cursor: pointer; position: relative; transition: background 0.2s; border: none; flex-shrink: 0; }
  .toggle::after { content: ''; position: absolute; top: 3px; left: 3px; width: 18px; height: 18px; background: white; border-radius: 50%; transition: left 0.2s; }
  .toggle.on { background: var(--accent); }
  .toggle.on::after { left: 23px; }
  @media (max-width: 400px) {
    :root { --cell-size: 54px; --gap: 5px; }
    .key { height: 46px; font-size: 18px; }
    .logo { font-size: 22px; }
  }
</style>
</head>
<body>

<div class="message" id="message"></div>

<header>
  <div class="logo">CIPHERLE</div>
  <div class="header-icons">
    <button class="icon-btn" id="settingsBtn" title="Settings">⚙</button>
    <button class="icon-btn" id="helpBtn" title="How to play">?</button>
  </div>
</header>

<div class="stats-bar">
  <div class="stat"><div class="stat-value" id="statPlayed">0</div><div class="stat-label">Played</div></div>
  <div class="stat-sep"></div>
  <div class="stat"><div class="stat-value" id="statWon">0</div><div class="stat-label">Won</div></div>
  <div class="stat-sep"></div>
  <div class="stat"><div class="stat-value" id="statStreak">0</div><div class="stat-label">Streak</div></div>
  <div class="stat-sep"></div>
  <div class="stat"><div class="stat-value" id="statBest">—</div><div class="stat-label">Best</div></div>
</div>

<div class="mode-bar">
  <button class="mode-btn active" data-mode="daily">📅 Daily</button>
  <button class="mode-btn" data-mode="easy">Easy</button>
  <button class="mode-btn" data-mode="hard">Hard</button>
</div>

<div class="timer-bar" id="timerBar">⏱ <span id="timerDisplay">00:00</span></div>
<div class="streak-display" id="streakDisplay" style="display:none"></div>

<div class="grid-wrapper"><div class="grid" id="grid"></div></div>

<div class="numpad"><div class="numpad-grid" id="numpad"></div></div>

<!-- RESULT OVERLAY -->
<div class="overlay" id="resultOverlay">
  <div class="modal">
    <span class="modal-emoji" id="resultEmoji"></span>
    <div class="modal-title" id="resultTitle"></div>
    <div class="modal-subtitle" id="resultSubtitle"></div>
    <div class="modal-answer" id="resultAnswer"></div>
    <div class="modal-emoji-grid" id="emojiGrid"></div>
    <div class="modal-buttons">
      <button class="btn btn-secondary" id="shareBtn">📤 Share</button>
      <button class="btn btn-primary" id="playAgainBtn">Play Again</button>
    </div>
  </div>
</div>

<!-- HELP OVERLAY -->
<div class="overlay" id="helpOverlay">
  <div class="modal settings-modal">
    <div class="settings-title">HOW TO PLAY</div>
    <p style="font-size:13px;color:var(--text-dim);line-height:1.7;margin-bottom:16px;">Guess the hidden 5-digit number in 6 attempts. After each guess, digits are colored:</p>
    <div style="display:flex;flex-direction:column;gap:10px;margin-bottom:20px;">
      <div style="display:flex;align-items:center;gap:12px;">
        <div style="width:44px;height:44px;background:var(--green-bg);border:2px solid var(--green);border-radius:8px;display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-weight:800;font-size:20px;color:var(--green);">7</div>
        <span style="font-size:13px;color:var(--text-dim);">Correct digit, correct position</span>
      </div>
      <div style="display:flex;align-items:center;gap:12px;">
        <div style="width:44px;height:44px;background:var(--yellow-bg);border:2px solid var(--yellow);border-radius:8px;display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-weight:800;font-size:20px;color:var(--yellow);">3</div>
        <span style="font-size:13px;color:var(--text-dim);">Correct digit, wrong position</span>
      </div>
      <div style="display:flex;align-items:center;gap:12px;">
        <div style="width:44px;height:44px;background:var(--gray-bg);border:2px solid var(--gray);border-radius:8px;display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-weight:800;font-size:20px;color:var(--text-dim);">9</div>
        <span style="font-size:13px;color:var(--text-dim);">Digit not in the number</span>
      </div>
    </div>
    <div style="font-size:11px;color:var(--text-dim);margin-bottom:16px;line-height:1.6;">
      <b style="color:var(--text)">Easy:</b> No repeating digits<br>
      <b style="color:var(--text)">Hard:</b> Digits may repeat<br>
      <b style="color:var(--text)">Daily:</b> Same number for everyone, resets at midnight
    </div>
    <button class="btn btn-primary" onclick="document.getElementById('helpOverlay').classList.remove('show')">GOT IT</button>
  </div>
</div>

<!-- SETTINGS OVERLAY -->
<div class="overlay" id="settingsOverlay">
  <div class="modal settings-modal">
    <div class="settings-title">SETTINGS</div>
    <div class="setting-row">
      <div><div class="setting-label">Allow Leading Zeros</div><div class="setting-desc">Numbers can start with 0</div></div>
      <button class="toggle on" id="toggleLeadingZeros"></button>
    </div>
    <div class="setting-row">
      <div><div class="setting-label">Timer</div><div class="setting-desc">Show elapsed time</div></div>
      <button class="toggle on" id="toggleTimer"></button>
    </div>
    <br>
    <button class="btn btn-primary" onclick="document.getElementById('settingsOverlay').classList.remove('show')">DONE</button>
  </div>
</div>

<script>
const MAX_GUESSES = 6;
const CODE_LENGTH = 5;

let target = '';
let guesses = [];
let currentGuess = '';
let gameOver = false;
let mode = 'daily';
let timerInterval = null;
let timerStart = null;
let elapsedSeconds = 0;

let settings = { leadingZeros: true, timer: true };
let stats = { played: 0, won: 0, streak: 0, maxStreak: 0, best: 0 };

function loadStats() {
  try { Object.assign(stats, JSON.parse(localStorage.getItem('numble_stats') || '{}')); } catch(e) {}
}
function saveStats() { localStorage.setItem('numble_stats', JSON.stringify(stats)); }
function loadSettings() {
  try { Object.assign(settings, JSON.parse(localStorage.getItem('numble_settings') || '{}')); } catch(e) {}
}
function saveSettings() { localStorage.setItem('numble_settings', JSON.stringify(settings)); }

function getDailyTarget() {
  const today = new Date();
  const seed = today.getFullYear() * 10000 + (today.getMonth()+1) * 100 + today.getDate();
  let s = seed;
  let result = '';
  const used = new Set();
  for (let i = 0; i < CODE_LENGTH; i++) {
    let d;
    do {
      s = (s * 1664525 + 1013904223) >>> 0;
      d = s % 10;
    } while (used.has(d) || (!settings.leadingZeros && i === 0 && d === 0));
    used.add(d);
    result += d;
  }
  return result;
}

function getRandomTarget(allowRepeats) {
  const digits = [];
  const used = new Set();
  for (let i = 0; i < CODE_LENGTH; i++) {
    let d, attempts = 0;
    do {
      d = Math.floor(Math.random() * 10);
      attempts++;
    } while ((!allowRepeats && used.has(d) || (!settings.leadingZeros && i === 0 && d === 0)) && attempts < 50);
    used.add(d);
    digits.push(d);
  }
  return digits.join('');
}

function getFeedback(guess, target) {
  const result = Array(CODE_LENGTH).fill('absent');
  const targetArr = target.split('');
  const guessArr = guess.split('');
  const targetUsed = Array(CODE_LENGTH).fill(false);
  const guessUsed = Array(CODE_LENGTH).fill(false);
  for (let i = 0; i < CODE_LENGTH; i++) {
    if (guessArr[i] === targetArr[i]) {
      result[i] = 'correct'; targetUsed[i] = true; guessUsed[i] = true;
    }
  }
  for (let i = 0; i < CODE_LENGTH; i++) {
    if (guessUsed[i]) continue;
    for (let j = 0; j < CODE_LENGTH; j++) {
      if (targetUsed[j]) continue;
      if (guessArr[i] === targetArr[j]) { result[i] = 'present'; targetUsed[j] = true; break; }
    }
  }
  return result;
}

function buildGrid() {
  const grid = document.getElementById('grid');
  grid.innerHTML = '';
  for (let r = 0; r < MAX_GUESSES; r++) {
    const row = document.createElement('div');
    row.className = 'row'; row.id = `row-${r}`;
    for (let c = 0; c < CODE_LENGTH; c++) {
      const cell = document.createElement('div');
      cell.className = 'cell'; cell.id = `cell-${r}-${c}`;
      row.appendChild(cell);
    }
    grid.appendChild(row);
  }
}

function updateCurrentRow() {
  const rowIdx = guesses.length;
  for (let c = 0; c < CODE_LENGTH; c++) {
    const cell = document.getElementById(`cell-${rowIdx}-${c}`);
    if (!cell) return;
    cell.textContent = currentGuess[c] || '';
    cell.className = 'cell' + (currentGuess[c] ? ' filled' : '') + ' active-row';
  }
}

function revealRow(rowIdx, feedback, guess) {
  return new Promise(resolve => {
    for (let c = 0; c < CODE_LENGTH; c++) {
      const cell = document.getElementById(`cell-${rowIdx}-${c}`);
      const delay = c * 120;
      setTimeout(() => {
        cell.classList.add('reveal');
        setTimeout(() => { cell.textContent = guess[c]; cell.className = `cell reveal ${feedback[c]}`; }, 250 + delay);
      }, delay);
    }
    setTimeout(resolve, CODE_LENGTH * 120 + 400);
  });
}

function buildNumpad() {
  const pad = document.getElementById('numpad');
  pad.innerHTML = '';
  for (let i = 0; i <= 9; i++) {
    const key = document.createElement('button');
    key.className = 'key'; key.textContent = i; key.dataset.key = i;
    key.addEventListener('click', () => handleInput(String(i)));
    pad.appendChild(key);
  }
  const del = document.createElement('button');
  del.className = 'key del'; del.textContent = '← DEL';
  del.addEventListener('click', () => handleDelete());
  pad.appendChild(del);
  const enter = document.createElement('button');
  enter.className = 'key enter'; enter.textContent = 'ENTER ↵';
  enter.addEventListener('click', () => handleEnter());
  pad.appendChild(enter);
}

function handleInput(digit) {
  if (gameOver || currentGuess.length >= CODE_LENGTH) return;
  currentGuess += digit;
  updateCurrentRow();
  const key = document.querySelector(`[data-key="${digit}"]`);
  if (key) { key.classList.add('pressing'); setTimeout(() => key.classList.remove('pressing'), 150); }
}

function handleDelete() {
  if (gameOver || currentGuess.length === 0) return;
  currentGuess = currentGuess.slice(0, -1);
  updateCurrentRow();
}

async function handleEnter() {
  if (gameOver) return;
  if (currentGuess.length < CODE_LENGTH) {
    const row = document.getElementById(`row-${guesses.length}`);
    row.classList.add('shake'); setTimeout(() => row.classList.remove('shake'), 400);
    showMessage('Need 5 digits!'); return;
  }
  const feedback = getFeedback(currentGuess, target);
  const guess = currentGuess;
  currentGuess = '';
  await revealRow(guesses.length, feedback, guess);
  guesses.push({ guess, feedback });
  const won = feedback.every(f => f === 'correct');
  if (won) {
    gameOver = true; stopTimer();
    stats.played++; stats.won++; stats.streak++;
    if (stats.streak > stats.maxStreak) stats.maxStreak = stats.streak;
    if (stats.best === 0 || guesses.length < stats.best) stats.best = guesses.length;
    saveStats(); updateStatsDisplay();
    setTimeout(() => showResult(true), 300); return;
  }
  if (guesses.length >= MAX_GUESSES) {
    gameOver = true; stopTimer();
    stats.played++; stats.streak = 0;
    saveStats(); updateStatsDisplay();
    setTimeout(() => showResult(false), 300); return;
  }
  updateCurrentRow();
}

function startTimer() {
  if (!settings.timer) return;
  timerStart = Date.now() - elapsedSeconds * 1000;
  timerInterval = setInterval(() => {
    elapsedSeconds = Math.floor((Date.now() - timerStart) / 1000);
    const m = Math.floor(elapsedSeconds / 60).toString().padStart(2, '0');
    const s = (elapsedSeconds % 60).toString().padStart(2, '0');
    document.getElementById('timerDisplay').textContent = `${m}:${s}`;
  }, 500);
}
function stopTimer() { clearInterval(timerInterval); timerInterval = null; }

function buildEmojiGrid() {
  return guesses.map(({ feedback }) =>
    feedback.map(f => f === 'correct' ? '🟩' : f === 'present' ? '🟨' : '⬜').join('')
  ).join('\n');
}

function showResult(won) {
  document.getElementById('resultEmoji').textContent = won ? (guesses.length <= 2 ? '🎯' : '🎉') : '💀';
  document.getElementById('resultTitle').textContent = won ? 'SOLVED!' : 'GAME OVER';
  const t = elapsedSeconds;
  const tStr = t < 60 ? `${t}s` : `${Math.floor(t/60)}m ${t%60}s`;
  document.getElementById('resultSubtitle').textContent = won ? `${guesses.length}/6 guesses · ${tStr}` : 'The answer was';
  document.getElementById('resultAnswer').textContent = target;
  document.getElementById('emojiGrid').textContent = buildEmojiGrid();
  document.getElementById('resultOverlay').classList.add('show');
}

function updateStatsDisplay() {
  document.getElementById('statPlayed').textContent = stats.played;
  document.getElementById('statWon').textContent = stats.won;
  document.getElementById('statStreak').textContent = stats.streak;
  document.getElementById('statBest').textContent = stats.best || '—';
  if (stats.streak > 1) {
    const el = document.getElementById('streakDisplay');
    el.style.display = ''; el.innerHTML = `🔥 ${stats.streak} game streak`;
  }
}

let msgTimeout;
function showMessage(text) {
  const el = document.getElementById('message');
  el.textContent = text; el.classList.add('show');
  clearTimeout(msgTimeout);
  msgTimeout = setTimeout(() => el.classList.remove('show'), 1800);
}

function newGame() {
  guesses = []; currentGuess = ''; gameOver = false; elapsedSeconds = 0;
  stopTimer();
  if (mode === 'daily') target = getDailyTarget();
  else if (mode === 'easy') target = getRandomTarget(false);
  else target = getRandomTarget(true);
  buildGrid(); updateCurrentRow();
  document.getElementById('timerDisplay').textContent = '00:00';
  document.getElementById('timerBar').style.display = settings.timer ? '' : 'none';
  document.getElementById('resultOverlay').classList.remove('show');
  startTimer();
}

document.querySelectorAll('.mode-btn').forEach(btn => {
  btn.addEventListener('click', () => {
    document.querySelectorAll('.mode-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active'); mode = btn.dataset.mode; newGame();
  });
});

document.getElementById('playAgainBtn').addEventListener('click', () => {
  if (mode === 'daily') {
    mode = 'easy';
    document.querySelectorAll('.mode-btn').forEach(b => b.classList.remove('active'));
    document.querySelector('[data-mode="easy"]').classList.add('active');
  }
  newGame();
});

document.getElementById('shareBtn').addEventListener('click', () => {
  const won = guesses.length > 0 && guesses[guesses.length-1]?.feedback.every(f => f === 'correct');
  const text = `NUMBLE ${mode === 'daily' ? '📅' : mode === 'hard' ? '💀' : ''} ${won ? guesses.length : 'X'}/6\n\n${buildEmojiGrid()}`;
  if (navigator.clipboard) navigator.clipboard.writeText(text).then(() => showMessage('Copied!'));
});

function bindToggle(id, key) {
  const btn = document.getElementById(id);
  btn.classList.toggle('on', settings[key]);
  btn.addEventListener('click', () => {
    settings[key] = !settings[key]; btn.classList.toggle('on', settings[key]); saveSettings();
    if (key === 'timer') document.getElementById('timerBar').style.display = settings.timer ? '' : 'none';
  });
}
bindToggle('toggleLeadingZeros', 'leadingZeros');
bindToggle('toggleTimer', 'timer');

document.getElementById('settingsBtn').addEventListener('click', () => document.getElementById('settingsOverlay').classList.add('show'));
document.getElementById('helpBtn').addEventListener('click', () => document.getElementById('helpOverlay').classList.add('show'));

document.querySelectorAll('.overlay').forEach(overlay => {
  overlay.addEventListener('click', e => {
    if (e.target === overlay && overlay.id !== 'resultOverlay') overlay.classList.remove('show');
  });
});

document.addEventListener('keydown', e => {
  if (e.ctrlKey || e.metaKey || e.altKey) return;
  if (e.key >= '0' && e.key <= '9') handleInput(e.key);
  else if (e.key === 'Backspace' || e.key === 'Delete') handleDelete();
  else if (e.key === 'Enter') handleEnter();
});

loadStats(); loadSettings(); updateStatsDisplay(); buildNumpad(); newGame();
</script>
</body>
</html>
