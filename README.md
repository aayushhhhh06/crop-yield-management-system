:root {
    --bg: #f3f8f3;
    --panel: #ffffff;
    --panel-soft: #f5fbf7;
    --sidebar: #123a2b;
    --primary: #2d8f5d;
    --primary-soft: #ebf9f0;
    --secondary: #2d6cdf;
    --secondary-soft: #edf4ff;
    --warning: #f59e0b;
    --warning-soft: #fff7e6;
    --purple: #7c5af5;
    --purple-soft: #f1ebff;
    --text: #1a2b1f;
    --muted: #475467;
    --border: #dfeae5;
    --danger: #db4c4c;
    --shadow: 0 15px 35px rgba(20, 52, 38, 0.08);
}

* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: linear-gradient(135deg, #edf9ef 0%, #f7fbff 100%);
    color: var(--text);
}

button, input, select, textarea {
    font: inherit;
}

.page-shell {
    display: flex;
    min-height: 100vh;
}

.sidebar {
    width: 250px;
    background: var(--sidebar);
    color: #fff;
    padding: 22px 18px;
}

.brand h2 {
    margin: 0 0 30px 0;
    font-size: 1.8rem;
}

.nav {
    display: flex;
    flex-direction: column;
    gap: 12px;
}

.nav a {
    text-decoration: none;
    color: #e9f7ef;
    padding: 12px 14px;
    border-radius: 12px;
    transition: 0.2s ease;
    font-weight: 600;
}

.nav a:hover {
    background: rgba(255,255,255,0.08);
}

.main-panel {
    flex: 1;
    padding: 30px;
}

.header-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 25px;
}

.eyebrow {
    margin: 0;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-size: 0.72rem;
    color: var(--muted);
}

.header-row h1 {
    margin: 6px 0 0 0;
    font-size: clamp(2rem, 3vw, 2.7rem);
}

.header-badge {
    background: var(--primary-soft);
    color: var(--primary);
    border: 1px solid #d7eedd;
    border-radius: 999px;
    padding: 10px 16px;
    font-weight: 600;
}

.stats-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(200px, 1fr));
    gap: 20px;
    margin-bottom: 25px;
}

.stat-card, .card {
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 18px;
    box-shadow: var(--shadow);
    padding: 22px;
}

.stat-card {
    position: relative;
    overflow: hidden;
}

.stat-card::before {
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    width: 6px;
    background: currentColor;
}

.stat-card.green { background: var(--primary-soft); color: var(--primary); }
.stat-card.blue { background: var(--secondary-soft); color: var(--secondary); }
.stat-card.orange { background: var(--warning-soft); color: var(--warning); }
.stat-card.purple { background: var(--purple-soft); color: var(--purple); }

.stat-card span {
    display: block;
    font-size: 0.8rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin-bottom: 10px;
    opacity: 0.8;
}

.stat-card h2 {
    margin: 0;
    font-size: clamp(1.5rem, 2vw, 2.2rem);
}

.chart-grid {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 20px;
    margin-bottom: 25px;
}

.bar-chart {
    display: flex;
    align-items: end;
    gap: 10px;
    height: 200px;
    padding-top: 10px;
}

.bar-wrap {
    flex: 1;
    display: flex;
    align-items: end;
    justify-content: center;
    height: 100%;
}

.bar {
    width: 100%;
    min-height: 12px;
    background: linear-gradient(to top, var(--primary), #7fd3a4);
    border-radius: 12px 12px 0 0;
}

.bar-labels {
    display: grid;
    grid-template-columns: repeat(6, minmax(0, 1fr));
    gap: 8px;
    margin-top: 10px;
    font-size: 0.75rem;
    color: var(--muted);
}

.form-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(300px, 1fr));
    gap: 20px;
    margin-bottom: 25px;
}

.full-width {
    margin-top: 25px;
}

.form-card {
    margin-top: 25px;
}

.record-form {
    display: grid;
    grid-template-columns: repeat(3, minmax(180px, 1fr));
    gap: 12px;
}

form {
    display: grid;
    gap: 12px;
}

input, select, textarea, button {
    width: 100%;
    border-radius: 12px;
    border: 1px solid var(--border);
    padding: 12px 14px;
    background: #fff;
}

textarea {
    min-height: 90px;
    resize: vertical;
}

button {
    background: var(--primary);
    color: white;
    border: none;
    font-weight: 700;
    cursor: pointer;
    transition: transform 0.15s ease;
}

button:hover {
    transform: translateY(-1px);
}

.ghost-btn {
    background: var(--primary-soft);
    color: var(--primary);
    border: 1px solid #d3ecdd;
}

.delete-btn {
    background: var(--danger);
}

.action-list {
    display: grid;
    gap: 12px;
}

.table-wrap {
    overflow-x: auto;
}

table {
    width: 100%;
    border-collapse: collapse;
    min-width: 900px;
}

th, td {
    text-align: left;
    padding: 12px 10px;
    border-bottom: 1px solid var(--border);
}

th {
    background: #f7faf8;
}

.flash-stack {
    margin-bottom: 20px;
}

.flash {
    padding: 12px 14px;
    border-radius: 12px;
    margin-top: 8px;
    font-weight: 600;
}

.flash-success {
    background: #eafaf1;
    color: #136d45;
    border: 1px solid #ccebd8;
}

.flash-error {
    background: #fff1f1;
    color: #b42318;
    border: 1px solid #f7d3d3;
}

.login-wrapper {
    min-height: 100vh;
    display: grid;
    place-items: center;
    background: linear-gradient(135deg, #ebf9ef, #eef5ff);
}

.login-box {
    width: min(440px, 90vw);
    background: white;
    border: 1px solid var(--border);
    border-radius: 24px;
    box-shadow: var(--shadow);
    padding: 32px 28px;
}

.login-box h1 {
    margin: 0 0 10px;
    font-size: 2rem;
    color: var(--primary);
}

.login-box p {
    margin: 0 0 20px;
    color: var(--muted);
}

.login-form {
    display: grid;
    gap: 16px;
}

.login-form label {
    display: grid;
    gap: 8px;
    font-weight: 600;
}

.credentials-box {
    margin-top: 22px;
    background: var(--panel-soft);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 14px 16px;
    color: var(--muted);
}

.credentials-box p {
    margin: 6px 0 0;
}

@media (max-width: 980px) {
    .page-shell {
        flex-direction: column;
    }

    .sidebar {
        width: 100%;
    }

    .stats-grid {
        grid-template-columns: repeat(2, minmax(200px, 1fr));
    }

    .chart-grid,
    .form-grid,
    .record-form {
        grid-template-columns: 1fr;
    }
}

@media (max-width: 620px) {
    .stats-grid {
        grid-template-columns: 1fr;
    }

    .main-panel {
        padding: 20px 15px 30px;
    }

    .header-row {
        flex-direction: column;
        align-items: flex-start;
        gap: 12px;
    }
}































































































