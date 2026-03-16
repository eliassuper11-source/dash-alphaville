<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Evolive Alphaville — Dashboard</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=DM+Sans:wght@300;400;500;600&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js"></script>
<style>
/* ===================== TOKENS ===================== */
:root {
  --bg:       #0A0F1E;
  --bg2:      #0F1628;
  --bg3:      #131C33;
  --bg4:      #1A2540;
  --gold:     #E8B84B;
  --gold-dim: rgba(232,184,75,0.08);
  --gold-glow:rgba(232,184,75,0.18);
  --branco:   #FFFFFF;
  --cinza1:   #F0F0F0;
  --cinza3:   #9AA0B4;
  --cinza4:   #555E7A;
  --azul-g:   #4285f4;
  --roxo-m:   #9b59b6;
  --verde-w:  #25d366;
  --org:      #E8B84B;
  --ok:       #22c55e;
  --warn:     #f59e0b;
  --bad:      #ef4444;
  --ok-bg:    rgba(34,197,94,0.10);
  --warn-bg:  rgba(245,158,11,0.10);
  --bad-bg:   rgba(239,68,68,0.10);
}

/* ===================== RESET ===================== */
*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
body {
  background: var(--bg);
  color: var(--branco);
  font-family: 'DM Sans', sans-serif;
  min-height: 100vh;
  overflow-x: hidden;
}

/* fundo atmosférico */
body::before {
  content: '';
  position: fixed; inset: 0;
  background:
    radial-gradient(ellipse 60% 40% at 10% 80%, rgba(232,184,75,0.04) 0%, transparent 60%),
    radial-gradient(ellipse 50% 30% at 90% 10%, rgba(232,184,75,0.03) 0%, transparent 50%);
  pointer-events: none; z-index: 0;
}

/* ===================== LOADING ===================== */
#loading {
  position: fixed; inset: 0;
  background: var(--bg);
  display: flex; flex-direction: column;
  align-items: center; justify-content: center;
  z-index: 999; gap: 20px;
}
.loading-logo {
  font-family: 'Inter', sans-serif;
  font-weight: 800; font-size: 28px;
  letter-spacing: 0.05em;
  color: var(--gold);
}
.loading-logo span { color: var(--cinza3); font-weight: 400; font-size: 16px; display: block; text-align: center; margin-top: 4px; letter-spacing: 0.15em; }
.loading-bar { width: 200px; height: 1px; background: var(--bg4); overflow: hidden; }
.loading-fill { height: 100%; background: var(--gold); animation: loadbar 1.8s ease-in-out infinite; }
@keyframes loadbar { 0%{width:0%;margin-left:0} 60%{width:55%;margin-left:20%} 100%{width:0%;margin-left:100%} }
.loading-text { font-size: 11px; color: var(--cinza4); font-family: 'DM Mono', monospace; letter-spacing: 0.05em; }

/* ===================== HEADER ===================== */
header {
  position: sticky; top: 0; z-index: 100;
  background: rgba(10,15,30,0.92);
  backdrop-filter: blur(24px);
  border-bottom: 1px solid rgba(232,184,75,0.10);
  padding: 0 32px; height: 60px;
  display: flex; align-items: center; justify-content: space-between;
}
.logo { display: flex; align-items: center; gap: 12px; }
.logo-mark {
  width: 32px; height: 32px;
  border: 1.5px solid var(--gold);
  border-radius: 8px;
  display: flex; align-items: center; justify-content: center;
  font-family: 'Inter', sans-serif; font-weight: 800; font-size: 13px;
  color: var(--gold); letter-spacing: 0;
}
.logo-text {
  font-family: 'Inter', sans-serif; font-weight: 600; font-size: 14px;
  letter-spacing: 0.02em;
}
.logo-text span { color: var(--gold); }
.header-right { display: flex; align-items: center; gap: 16px; }
.status-pill {
  display: flex; align-items: center; gap: 6px;
  background: rgba(34,197,94,0.08);
  border: 1px solid rgba(34,197,94,0.2);
  border-radius: 20px; padding: 4px 11px;
  font-size: 11px; font-weight: 500; color: var(--ok);
}
.status-dot { width: 5px; height: 5px; background: var(--ok); border-radius: 50%; animation: pulse 2s infinite; }
@keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:.4;transform:scale(.7)} }
.last-update { font-size: 11px; color: var(--cinza4); font-family: 'DM Mono', monospace; }
.btn-refresh {
  background: transparent;
  border: 1px solid rgba(232,184,75,0.25);
  color: var(--gold); border-radius: 8px;
  padding: 6px 13px; font-size: 12px; cursor: pointer;
  font-family: 'DM Sans', sans-serif;
  transition: all .2s;
}
.btn-refresh:hover { background: var(--gold); color: var(--bg); }

/* ===================== MAIN ===================== */
main {
  position: relative; z-index: 1;
  padding: 28px 32px 56px;
  max-width: 1600px; margin: 0 auto;
}

/* ===================== SECTION LABEL ===================== */
.section-label {
  font-family: 'Inter', sans-serif;
  font-size: 10px; font-weight: 600;
  letter-spacing: 1.8px; text-transform: uppercase;
  color: var(--gold); margin-bottom: 16px;
  display: flex; align-items: center; gap: 10px;
}
.section-label::after {
  content: ''; flex: 1; height: 1px;
  background: linear-gradient(to right, rgba(232,184,75,0.3), transparent);
}

/* ===================== ERRO ===================== */
#error-msg {
  display: none;
  background: var(--bad-bg); border: 1px solid rgba(239,68,68,0.3);
  border-radius: 10px; padding: 14px 18px;
  color: var(--bad); font-size: 13px; margin-bottom: 20px; line-height: 1.6;
}

/* ===================== SCORECARDS ===================== */
.scorecards {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 14px; margin-bottom: 32px;
}
.card {
  background: var(--bg3);
  border: 1px solid rgba(255,255,255,0.05);
  border-radius: 14px; padding: 20px 22px;
  position: relative; overflow: hidden;
  transition: transform .2s, border-color .2s;
}
.card:hover { transform: translateY(-2px); border-color: rgba(232,184,75,0.2); }
.card::before {
  content: ''; position: absolute;
  top: 0; left: 0; right: 0; height: 2px;
  background: var(--cc, var(--gold));
}
.card-google { --cc: var(--azul-g); }
.card-meta   { --cc: var(--roxo-m); }
.card-wa     { --cc: var(--verde-w); }
.card-total  { --cc: var(--gold); background: linear-gradient(135deg, #060C1C, var(--bg3)); }

.card-header { display: flex; align-items: center; justify-content: space-between; margin-bottom: 14px; }
.canal-badge { display: flex; align-items: center; gap: 6px; font-size: 11px; font-weight: 600; letter-spacing: .4px; text-transform: uppercase; color: var(--cinza3); }
.canal-dot   { width: 6px; height: 6px; border-radius: 50%; background: var(--cc, var(--gold)); }
.meta-badge  { font-size: 10px; font-family: 'DM Mono', monospace; padding: 3px 8px; border-radius: 6px; font-weight: 500; }
.meta-ok   { background: var(--ok-bg);   color: var(--ok);   }
.meta-warn { background: var(--warn-bg); color: var(--warn); }
.meta-bad  { background: var(--bad-bg);  color: var(--bad);  }

.card-value { font-family: 'Inter', sans-serif; font-size: 34px; font-weight: 700; line-height: 1; margin-bottom: 3px; letter-spacing: -0.5px; }
.card-label { font-size: 11px; color: var(--cinza4); margin-bottom: 14px; }

.faixa-meta { font-size: 10px; color: var(--cinza4); margin-bottom: 4px; }
.faixa-meta strong { color: var(--cinza3); }

.progress-wrap  { margin-bottom: 13px; }
.progress-label { display: flex; justify-content: space-between; font-size: 10px; color: var(--cinza4); margin-bottom: 5px; }
.progress-bar   { height: 2px; background: rgba(255,255,255,0.06); border-radius: 2px; overflow: hidden; }
.progress-fill  { height: 100%; border-radius: 2px; transition: width 1s ease; background: var(--cc, var(--gold)); }

.card-metrics { display: flex; gap: 16px; padding-top: 12px; border-top: 1px solid rgba(255,255,255,0.05); }
.metric       { display: flex; flex-direction: column; gap: 2px; }
.metric-val   { font-family: 'DM Mono', monospace; font-size: 12px; font-weight: 500; }
.metric-label { font-size: 9px; color: var(--cinza4); text-transform: uppercase; letter-spacing: .5px; }

/* ===================== CHARTS ===================== */
.charts-grid {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 14px; margin-bottom: 32px;
}
.chart-card {
  background: var(--bg3);
  border: 1px solid rgba(255,255,255,0.05);
  border-radius: 14px; padding: 22px;
}
.chart-header { display: flex; align-items: flex-start; justify-content: space-between; margin-bottom: 18px; }
.chart-title  { font-family: 'Inter', sans-serif; font-size: 13px; font-weight: 600; }
.chart-subtitle { font-size: 11px; color: var(--cinza4); margin-top: 3px; }
.legend { display: flex; gap: 12px; flex-wrap: wrap; margin-top: 5px; }
.legend-item { display: flex; align-items: center; gap: 5px; font-size: 10px; color: var(--cinza3); }
.legend-dot  { width: 8px; height: 8px; border-radius: 2px; }

/* ===================== TABELAS ===================== */
.tables-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 14px; margin-bottom: 32px;
}
.table-card {
  background: var(--bg3);
  border: 1px solid rgba(255,255,255,0.05);
  border-radius: 14px; overflow: hidden;
}
.table-card.destaque {
  border-color: rgba(232,184,75,0.3);
  box-shadow: 0 0 0 1px rgba(232,184,75,0.06), 0 4px 24px rgba(232,184,75,0.05);
}
.table-header {
  padding: 15px 18px 13px;
  border-bottom: 1px solid rgba(255,255,255,0.05);
  display: flex; align-items: flex-start; justify-content: space-between;
}
.table-title  { font-family: 'Inter', sans-serif; font-size: 12px; font-weight: 600; }
.table-tag {
  font-size: 9px; font-weight: 700; padding: 2px 7px; border-radius: 5px;
  background: var(--gold-dim); color: var(--gold);
  border: 1px solid rgba(232,184,75,0.2);
  letter-spacing: .5px; text-transform: uppercase;
  margin-top: 3px; display: inline-block;
}
.table-tag.muted {
  background: rgba(255,255,255,0.04); color: var(--cinza4);
  border-color: rgba(255,255,255,0.08);
}
.table-period { font-size: 10px; color: var(--cinza4); font-family: 'DM Mono', monospace; margin-top: 3px; }
.sem-num { font-family: 'Inter', sans-serif; font-size: 15px; font-weight: 700; color: var(--gold); opacity: .6; line-height: 1; }

table { width: 100%; border-collapse: collapse; }
thead th {
  padding: 7px 14px; font-size: 9px; font-weight: 600;
  letter-spacing: .8px; text-transform: uppercase; color: var(--cinza4);
  text-align: right; background: rgba(0,0,0,0.15);
}
thead th:first-child { text-align: left; }
tbody tr { border-bottom: 1px solid rgba(255,255,255,0.04); transition: background .15s; }
tbody tr:hover { background: rgba(255,255,255,0.02); }
tbody tr:last-child { border-bottom: none; }
tbody td { padding: 9px 14px; font-size: 12px; text-align: right; font-family: 'DM Mono', monospace; }
tbody td:first-child { text-align: left; font-family: 'DM Sans', sans-serif; font-weight: 500; display: flex; align-items: center; gap: 7px; }
.cd { width: 5px; height: 5px; border-radius: 50%; flex-shrink: 0; }
.cpl-pill { font-size: 10px; padding: 2px 6px; border-radius: 5px; font-family: 'DM Mono', monospace; }
.delta { font-size: 10px; font-family: 'DM Mono', monospace; }
.delta-up { color: var(--ok); }
.delta-dn { color: var(--bad); }
.delta-eq { color: var(--cinza4); }
tfoot td {
  padding: 9px 14px; font-size: 12px; font-weight: 600; text-align: right;
  border-top: 1px solid rgba(255,255,255,0.08);
  font-family: 'DM Mono', monospace; color: var(--gold);
}
tfoot td:first-child { text-align: left; font-family: 'DM Sans', sans-serif; font-size: 10px; letter-spacing: .3px; text-transform: uppercase; }

/* ===================== MENSAL + VENDAS ===================== */
.monthly-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 14px; margin-bottom: 32px;
}
.monthly-card {
  background: var(--bg3);
  border: 1px solid rgba(255,255,255,0.05);
  border-radius: 14px; padding: 22px;
}
.monthly-big {
  display: grid; grid-template-columns: repeat(3,1fr);
  gap: 18px; margin-top: 18px;
}
.monthly-item { display: flex; flex-direction: column; gap: 3px; }
.monthly-num  { font-family: 'Inter', sans-serif; font-size: 22px; font-weight: 700; letter-spacing: -0.3px; }
.monthly-lbl  { font-size: 10px; color: var(--cinza4); text-transform: uppercase; letter-spacing: .5px; }

/* Card vendas */
.vendas-card { background: linear-gradient(135deg, #050A18, var(--bg3)) !important; border-color: rgba(232,184,75,0.15) !important; }
.vendas-top  { display: flex; align-items: flex-start; justify-content: space-between; margin-bottom: 16px; }
.roas-pill   { font-size: 11px; font-family: 'DM Mono', monospace; padding: 4px 10px; border-radius: 20px; background: var(--gold-dim); color: var(--gold); border: 1px solid rgba(232,184,75,0.25); font-weight: 600; }
.v-kpis      { display: grid; grid-template-columns: repeat(3,1fr); gap: 10px; margin-bottom: 14px; }
.vkpi        { background: rgba(0,0,0,0.25); border-radius: 10px; padding: 13px; border: 1px solid rgba(255,255,255,0.04); }
.vkpi-val    { font-family: 'Inter', sans-serif; font-size: 20px; font-weight: 700; letter-spacing: -0.3px; line-height: 1; margin-bottom: 2px; }
.vkpi-lbl    { font-size: 9px; color: var(--cinza4); text-transform: uppercase; letter-spacing: .5px; }
.vkpi-sub    { font-size: 10px; color: var(--cinza3); font-family: 'DM Mono', monospace; margin-top: 3px; }

.v-canais-pagos { display: grid; grid-template-columns: repeat(4,1fr); gap: 8px; margin-bottom: 8px; }
.vcanal      { background: rgba(0,0,0,0.2); border-radius: 9px; padding: 10px 12px; border-left: 3px solid var(--cc, var(--gold)); }
.vcanal-topo { display: flex; align-items: center; justify-content: space-between; margin-bottom: 5px; }
.vcanal-nome { font-size: 10px; font-weight: 600; color: var(--cinza3); text-transform: uppercase; letter-spacing: .4px; }
.vcanal-conv { font-size: 9px; font-family: 'DM Mono', monospace; color: var(--gold); background: var(--gold-dim); padding: 1px 5px; border-radius: 4px; }
.vcanal-qtd  { font-family: 'Inter', sans-serif; font-size: 18px; font-weight: 700; color: var(--branco); line-height: 1; }
.vcanal-info { font-size: 10px; color: var(--cinza4); font-family: 'DM Mono', monospace; margin-top: 2px; }

/* ===================== ANIMAÇÕES ===================== */
@keyframes fadeUp { from{opacity:0;transform:translateY(12px)} to{opacity:1;transform:translateY(0)} }
.fade-up { animation: fadeUp .4s ease both; }
.d1{animation-delay:.05s}.d2{animation-delay:.10s}.d3{animation-delay:.15s}.d4{animation-delay:.20s}.d5{animation-delay:.25s}

/* ===================== SCROLLBAR ===================== */
::-webkit-scrollbar { width: 4px; }
::-webkit-scrollbar-track { background: var(--bg2); }
::-webkit-scrollbar-thumb { background: var(--bg4); border-radius: 2px; }
</style>
</head>
<body>

<!-- LOADING -->
<div id="loading">
  <div class="loading-logo">EVOLIVE<span>ALPHAVILLE</span></div>
  <div class="loading-bar"><div class="loading-fill"></div></div>
  <div class="loading-text" id="ltxt">Conectando...</div>
</div>

<!-- HEADER -->
<header>
  <div class="logo">
    <div class="logo-mark">AV</div>
    <div class="logo-text">EVOLIVE <span>Alphaville</span></div>
  </div>
  <div class="header-right">
    <div class="status-pill"><div class="status-dot"></div><span>Ao vivo</span></div>
    <div class="last-update" id="last-update">—</div>
    <button class="btn-refresh" onclick="loadAll()">↻ Atualizar</button>
  </div>
</header>

<!-- APP -->
<main id="app" style="display:none">
  <div id="error-msg"></div>

  <!-- SCORECARDS -->
  <div class="section-label">Última Semana Fechada — <span id="lbl-sem-dest" style="color:var(--cinza3);font-weight:400;letter-spacing:0;text-transform:none;font-family:'DM Mono',monospace;font-size:11px">—</span></div>
  <div class="scorecards">

    <!-- Google -->
    <div class="card card-google fade-up d1">
      <div class="card-header">
        <div class="canal-badge"><div class="canal-dot"></div>Google Ads</div>
        <div class="meta-badge" id="b-g">—</div>
      </div>
      <div class="card-value" id="v-g">—</div>
      <div class="card-label">leads na semana</div>
      <div class="faixa-meta">Meta: <strong>4–8/dia</strong></div>
      <div class="progress-wrap">
        <div class="progress-label"><span>Ref: <b id="mg">6</b>/dia</span><span id="pg-pct">—</span></div>
        <div class="progress-bar"><div class="progress-fill" id="pg" style="width:0%"></div></div>
      </div>
      <div class="card-metrics">
        <div class="metric"><div class="metric-val" id="ig">—</div><div class="metric-label">Investido</div></div>
        <div class="metric"><div class="metric-val" id="cg">—</div><div class="metric-label">CPL</div></div>
      </div>
    </div>

    <!-- Meta -->
    <div class="card card-meta fade-up d2">
      <div class="card-header">
        <div class="canal-badge"><div class="canal-dot"></div>Meta Ads</div>
        <div class="meta-badge" id="b-m">—</div>
      </div>
      <div class="card-value" id="v-m">—</div>
      <div class="card-label">leads na semana</div>
      <div class="faixa-meta">Meta: <strong>2–4/dia</strong></div>
      <div class="progress-wrap">
        <div class="progress-label"><span>Ref: <b id="mm">3</b>/dia</span><span id="pm-pct">—</span></div>
        <div class="progress-bar"><div class="progress-fill" id="pm" style="width:0%"></div></div>
      </div>
      <div class="card-metrics">
        <div class="metric"><div class="metric-val" id="im">—</div><div class="metric-label">Investido</div></div>
        <div class="metric"><div class="metric-val" id="cm">—</div><div class="metric-label">CPL</div></div>
      </div>
    </div>

    <!-- WhatsApp -->
    <div class="card card-wa fade-up d3">
      <div class="card-header">
        <div class="canal-badge"><div class="canal-dot"></div>WhatsApp</div>
        <div class="meta-badge" id="b-w">—</div>
      </div>
      <div class="card-value" id="v-w">—</div>
      <div class="card-label">leads na semana</div>
      <div class="faixa-meta">Meta: <strong>6–12/dia</strong></div>
      <div class="progress-wrap">
        <div class="progress-label"><span>Ref: <b id="mw">9</b>/dia</span><span id="pw-pct">—</span></div>
        <div class="progress-bar"><div class="progress-fill" id="pw" style="width:0%"></div></div>
      </div>
      <div class="card-metrics">
        <div class="metric"><div class="metric-val" id="iw">—</div><div class="metric-label">Investido</div></div>
        <div class="metric"><div class="metric-val" id="cw">—</div><div class="metric-label">CPL</div></div>
      </div>
    </div>

    <!-- Total -->
    <div class="card card-total fade-up d4">
      <div class="card-header">
        <div class="canal-badge"><div class="canal-dot"></div>Total Geral</div>
        <div class="meta-badge" id="b-t">—</div>
      </div>
      <div class="card-value" id="v-t">—</div>
      <div class="card-label">leads na semana</div>
      <div class="faixa-meta">Meta: <strong>13–20/dia</strong></div>
      <div class="progress-wrap">
        <div class="progress-label"><span>Ref: <b id="mt">16</b>/dia</span><span id="pt-pct">—</span></div>
        <div class="progress-bar"><div class="progress-fill" id="pt" style="width:0%"></div></div>
      </div>
      <div class="card-metrics">
        <div class="metric"><div class="metric-val" id="it">—</div><div class="metric-label">Investido</div></div>
        <div class="metric"><div class="metric-val" id="ct">—</div><div class="metric-label">CPL Médio</div></div>
      </div>
    </div>

  </div>

  <!-- CHARTS -->
  <div class="section-label">Evolução do Mês Atual</div>
  <div class="charts-grid fade-up d3">
    <div class="chart-card">
      <div class="chart-header">
        <div>
          <div class="chart-title">Leads por Canal</div>
          <div class="chart-subtitle">Evolução diária — mês atual</div>
        </div>
        <div class="legend">
          <div class="legend-item"><div class="legend-dot" style="background:var(--azul-g)"></div>Google</div>
          <div class="legend-item"><div class="legend-dot" style="background:var(--roxo-m)"></div>Meta</div>
          <div class="legend-item"><div class="legend-dot" style="background:var(--verde-w)"></div>WhatsApp</div>
        </div>
      </div>
      <div style="height:230px"><canvas id="chart-leads"></canvas></div>
    </div>
    <div class="chart-card">
      <div class="chart-header"><div><div class="chart-title">CPL por Canal</div><div class="chart-subtitle">Acumulado do mês</div></div></div>
      <div style="height:230px"><canvas id="chart-cpl"></canvas></div>
    </div>
  </div>

  <!-- TABELAS SEMANAIS -->
  <div class="section-label">Comparativo de Semanas Fechadas</div>
  <div class="tables-grid fade-up d4">
    <div class="table-card destaque">
      <div class="table-header">
        <div><div class="table-title">Última Semana Fechada</div><span class="table-tag">Em destaque</span><div class="table-period" id="p-s1">—</div></div>
        <div class="sem-num" id="n-s1">—</div>
      </div>
      <table><thead><tr><th>Canal</th><th>Leads</th><th>Invest.</th><th>CPL</th></tr></thead><tbody id="tb-s1"></tbody><tfoot id="tf-s1"></tfoot></table>
    </div>
    <div class="table-card">
      <div class="table-header">
        <div><div class="table-title">Semana Anterior</div><span class="table-tag muted">Fechada</span><div class="table-period" id="p-s2">—</div></div>
        <div class="sem-num" style="color:var(--cinza4)" id="n-s2">—</div>
      </div>
      <table><thead><tr><th>Canal</th><th>Leads</th><th>Invest.</th><th>CPL</th><th>Δ</th></tr></thead><tbody id="tb-s2"></tbody><tfoot id="tf-s2"></tfoot></table>
    </div>
    <div class="table-card">
      <div class="table-header">
        <div><div class="table-title">2 Semanas Atrás</div><span class="table-tag muted">Fechada</span><div class="table-period" id="p-s3">—</div></div>
        <div class="sem-num" style="color:var(--cinza4)" id="n-s3">—</div>
      </div>
      <table><thead><tr><th>Canal</th><th>Leads</th><th>Invest.</th><th>CPL</th><th>Δ</th></tr></thead><tbody id="tb-s3"></tbody><tfoot id="tf-s3"></tfoot></table>
    </div>
  </div>

  <!-- MENSAL + VENDAS -->
  <div class="section-label">Resumo do Mês</div>
  <div class="monthly-grid fade-up d5">
    <div class="monthly-card">
      <div class="chart-title">Tráfego — <span id="mes-nome">—</span></div>
      <div class="chart-subtitle" style="margin-top:3px">Consolidado por canal</div>
      <div class="monthly-big" id="monthly-canais"></div>
    </div>
    <div class="monthly-card vendas-card">
      <div class="vendas-top">
        <div>
          <div class="chart-title">Vendas — <span id="mes-nome-v">—</span></div>
          <div class="chart-subtitle" style="margin-top:3px">Contratos fechados · Preenchimento manual</div>
        </div>
        <div class="roas-pill" id="v-roas-pill">ROAS —</div>
      </div>
      <div class="v-kpis">
        <div class="vkpi">
          <div class="vkpi-val" id="v-qtd" style="color:var(--gold)">—</div>
          <div class="vkpi-lbl">Contratos</div>
          <div class="vkpi-sub" id="v-receita">—</div>
        </div>
        <div class="vkpi">
          <div class="vkpi-val" id="v-roas" style="color:var(--ok)">—</div>
          <div class="vkpi-lbl">ROAS c/ pagos</div>
          <div class="vkpi-sub" id="v-conv">—</div>
        </div>
        <div class="vkpi">
          <div class="vkpi-val" id="v-ticket" style="color:var(--warn)">—</div>
          <div class="vkpi-lbl">Ticket médio</div>
          <div class="vkpi-sub" id="v-invest">—</div>
        </div>
      </div>
      <div class="v-canais-pagos" id="v-canais-pagos"></div>
    </div>
  </div>

</main>

<script>
// ============================================================
//  CONFIGURAÇÃO — substitua pela URL do Web App após publicar
// ============================================================
const PROXY_URL = 'https://script.google.com/macros/s/AKfycbzzae8G3Jk5SPcPKQ2J2i3mc7qKOH1W2o3cVOPAttgeNhPFfEDe3HnwWk6UCWvSIJwGMg/exec';

// ============================================================
const MESES = ['Janeiro','Fevereiro','Março','Abril','Maio','Junho','Julho','Agosto','Setembro','Outubro','Novembro','Dezembro'];

function fR(v, d=2)  { return 'R$ ' + Number(v||0).toLocaleString('pt-BR',{minimumFractionDigits:d,maximumFractionDigits:d}); }
function fRk(v)      { const n=Number(v||0); return n>=1000?'R$'+(n/1000).toFixed(1)+'k':fR(n,0); }

// ============================================================
async function loadAll() {
  document.getElementById('loading').style.display = 'flex';
  document.getElementById('app').style.display     = 'none';
  document.getElementById('ltxt').textContent      = 'Carregando dados...';

  try {
    const res  = await fetch(PROXY_URL);
    const data = await res.json();
    if (data.error) throw new Error(data.error);

    renderTrafego(data);
    renderVendas(data);

    const n = new Date();
    document.getElementById('last-update').textContent =
      'Atualizado ' + n.getHours().toString().padStart(2,'0') + ':' + n.getMinutes().toString().padStart(2,'0');

    document.getElementById('loading').style.display = 'none';
    document.getElementById('app').style.display     = 'block';

  } catch(e) {
    document.getElementById('loading').style.display = 'none';
    document.getElementById('app').style.display     = 'block';
    const el = document.getElementById('error-msg');
    el.style.display = 'block';
    el.textContent   = 'Erro ao carregar dados: ' + e.message;
  }
}

// ============================================================
//  TRÁFEGO
// ============================================================
function renderTrafego(data) {
  const { metas, rows } = data;
  rows.forEach(r => { r.dt = new Date(r.data + 'T00:00:00'); });

  document.getElementById('mg').textContent = metas.google;
  document.getElementById('mm').textContent = metas.meta;
  document.getElementById('mw').textContent = metas.wa;
  document.getElementById('mt').textContent = metas.total;

  const rowsComDados = rows.filter(r => r.totLeads>0||r.gLeads>0||r.mLeads>0||r.wLeads>0);
  const semsComDados = [...new Set(rowsComDados.map(r => r.sem))].sort((a,b)=>a-b);

  const hoje        = new Date();
  const semHoje     = rows.find(r => r.dt.getFullYear()===hoje.getFullYear()&&r.dt.getMonth()===hoje.getMonth()&&r.dt.getDate()===hoje.getDate());
  const numSemHoje  = semHoje ? semHoje.sem : semsComDados[semsComDados.length-1];
  const semsFechadas= semsComDados.filter(s => s < numSemHoje);

  const s1num = semsFechadas[semsFechadas.length-1] || semsComDados[semsComDados.length-1];
  const s2num = semsFechadas[semsFechadas.length-2] || s1num-1;
  const s3num = semsFechadas[semsFechadas.length-3] || s1num-2;

  const getSem = n => rows.filter(r => r.sem === n);
  const s1rows = getSem(s1num), s2rows = getSem(s2num), s3rows = getSem(s3num);

  const soma = arr => ({
    gL: arr.reduce((s,r)=>s+r.gLeads,0),  gI: arr.reduce((s,r)=>s+r.gInvest,0),
    mL: arr.reduce((s,r)=>s+r.mLeads,0),  mI: arr.reduce((s,r)=>s+r.mInvest,0),
    wL: arr.reduce((s,r)=>s+r.wLeads,0),  wI: arr.reduce((s,r)=>s+r.wInvest,0),
    tL: arr.reduce((s,r)=>s+r.totLeads,0),tI: arr.reduce((s,r)=>s+r.totInvest,0),
  });

  const s1 = soma(s1rows), s2 = soma(s2rows), s3 = soma(s3rows);
  const cpl = (inv, leads) => leads>0&&inv>0 ? inv/leads : 0;
  const diasUteis = s1rows.filter(r=>r.dt.getDay()!==0&&r.dt.getDay()!==6).length || 5;

  renderCard('g', s1.gL, s1.gI, cpl(s1.gI,s1.gL), metas.google * diasUteis);
  renderCard('m', s1.mL, s1.mI, cpl(s1.mI,s1.mL), metas.meta   * diasUteis);
  renderCard('w', s1.wL, s1.wI, cpl(s1.wI,s1.wL), metas.wa     * diasUteis);
  const tL = s1.gL+s1.mL+s1.wL, tI = s1.gI+s1.mI+s1.wI;
  renderCard('t', tL, tI, cpl(tI,tL), metas.total * diasUteis);

  const fmtP = arr => {
    if (!arr.length) return '—';
    const d1=arr[0].dt, d2=arr[arr.length-1].dt;
    return d1.getDate()+'/'+(d1.getMonth()+1)+' – '+d2.getDate()+'/'+(d2.getMonth()+1);
  };

  document.getElementById('lbl-sem-dest').textContent = 'Semana ' + s1num + ' — ' + fmtP(s1rows);
  document.getElementById('n-s1').textContent = 'S' + s1num;
  document.getElementById('n-s2').textContent = 'S' + s2num;
  document.getElementById('n-s3').textContent = 'S' + s3num;
  document.getElementById('p-s1').textContent = fmtP(s1rows);
  document.getElementById('p-s2').textContent = fmtP(s2rows);
  document.getElementById('p-s3').textContent = fmtP(s3rows);

  renderTabela('tb-s1','tf-s1', s1, null);
  renderTabela('tb-s2','tf-s2', s2, s1);
  renderTabela('tb-s3','tf-s3', s3, s1);

  const mesAtual = rowsComDados.length ? rowsComDados[rowsComDados.length-1].mes : hoje.getMonth()+1;
  const diasMes  = rows.filter(r => r.mes === mesAtual);
  renderCharts(diasMes);
  renderMensal(diasMes, mesAtual);
}

function renderCard(id, leads, invest, cplVal, metaLeads) {
  const pct = metaLeads > 0 ? Math.round((leads / metaLeads) * 100) : 0;
  document.getElementById('v-'  + id).textContent = leads || '—';
  document.getElementById('i'   + id).textContent = invest > 0 ? fR(invest) : '—';
  document.getElementById('c'   + id).textContent = cplVal > 0 ? fR(cplVal) : '—';
  document.getElementById('p'   + id).style.width = Math.min(pct,100) + '%';
  document.getElementById('p'   + id + '-pct').textContent = pct + '%';

  const badge = document.getElementById('b-' + id);
  if (!leads)        { badge.className='meta-badge meta-warn'; badge.textContent='Sem dados'; }
  else if (pct>=90)  { badge.className='meta-badge meta-ok';   badge.textContent='✓ Na meta'; }
  else if (pct>=65)  { badge.className='meta-badge meta-warn'; badge.textContent='~ Abaixo';  }
  else               { badge.className='meta-badge meta-bad';  badge.textContent='✗ Longe';   }
}

function renderTabela(tbodyId, tfootId, s, ref) {
  const canais = [
    { nome:'Google Ads', cor:'var(--azul-g)',  l:s.gL, i:s.gI, rl:ref?ref.gL:null },
    { nome:'Meta Ads',   cor:'var(--roxo-m)',  l:s.mL, i:s.mI, rl:ref?ref.mL:null },
    { nome:'WhatsApp',   cor:'var(--verde-w)', l:s.wL, i:s.wI, rl:ref?ref.wL:null },
  ];
  const tbody = document.getElementById(tbodyId); tbody.innerHTML = '';
  let tL=0, tI=0;
  canais.forEach(c => {
    tL += c.l; tI += c.i;
    const cv  = c.l>0&&c.i>0 ? c.i/c.l : 0;
    const cls = cv>0 ? (cv<=30?'meta-ok':(cv<=40?'meta-warn':'meta-bad')) : '';
    let dH = '';
    if (ref && c.rl!==null) {
      const d=c.l-c.rl;
      const dc = d>0?'delta-up':d<0?'delta-dn':'delta-eq';
      dH = '<td><span class="delta '+dc+'">'+(d>0?'+':'')+d+'</span></td>';
    }
    tbody.innerHTML += '<tr><td><div class="cd" style="background:'+c.cor+'"></div>'+c.nome+'</td>'
      +'<td>'+(c.l||'—')+'</td>'
      +'<td>'+(c.i>0?fR(c.i):'—')+'</td>'
      +'<td>'+(cv>0?'<span class="cpl-pill '+cls+'">'+fR(cv)+'</span>':'—')+'</td>'
      +dH+'</tr>';
  });
  const tc = tI>0&&tL>0 ? tI/tL : 0;
  document.getElementById(tfootId).innerHTML =
    '<tr><td>TOTAL</td><td>'+(tL||'—')+'</td><td>'+(tI>0?fR(tI):'—')+'</td>'
    +'<td>'+(tc>0?fR(tc):'—')+'</td>'+(ref?'<td></td>':'')+'</tr>';
}

let chL=null, chC=null;
function renderCharts(dias) {
  const labels = dias.map(d => d.dt.getDate()+'/'+(d.dt.getMonth()+1));
  const baseOpts = {
    responsive: true, maintainAspectRatio: false,
    plugins: {
      legend:  { display: false },
      tooltip: { backgroundColor:'#0A0F1E', borderColor:'rgba(232,184,75,0.15)', borderWidth:1, titleColor:'#fff', bodyColor:'#9AA0B4' }
    },
    scales: {
      x: { grid:{color:'rgba(232,184,75,0.05)'}, ticks:{color:'#555E7A',font:{size:9}} },
      y: { grid:{color:'rgba(232,184,75,0.05)'}, ticks:{color:'#555E7A',font:{size:9}} }
    }
  };

  if (chL) chL.destroy();
  chL = new Chart(document.getElementById('chart-leads'), {
    type: 'line',
    data: { labels, datasets: [
      { label:'Google', data:dias.map(d=>d.gLeads||null), borderColor:'#4285f4', backgroundColor:'rgba(66,133,244,0.06)', tension:.4, pointRadius:2, fill:true, spanGaps:true },
      { label:'Meta',   data:dias.map(d=>d.mLeads||null), borderColor:'#9b59b6', backgroundColor:'rgba(155,89,182,0.06)', tension:.4, pointRadius:2, fill:true, spanGaps:true },
      { label:'WA',     data:dias.map(d=>d.wLeads||null), borderColor:'#25d366', backgroundColor:'rgba(37,211,102,0.06)', tension:.4, pointRadius:2, fill:true, spanGaps:true },
    ]},
    options: baseOpts
  });

  const tG=dias.reduce((s,d)=>s+d.gLeads,0), iG=dias.reduce((s,d)=>s+d.gInvest,0);
  const tM=dias.reduce((s,d)=>s+d.mLeads,0), iM=dias.reduce((s,d)=>s+d.mInvest,0);
  const tW=dias.reduce((s,d)=>s+d.wLeads,0), iW=dias.reduce((s,d)=>s+d.wInvest,0);
  const cG=tG>0?iG/tG:0, cM=tM>0?iM/tM:0, cW=tW>0?iW/tW:0;

  if (chC) chC.destroy();
  chC = new Chart(document.getElementById('chart-cpl'), {
    type: 'doughnut',
    data: {
      labels: ['Google R$'+cG.toFixed(2), 'Meta R$'+cM.toFixed(2), 'WA R$'+cW.toFixed(2)],
      datasets: [{ data:[Math.max(cG,.01),Math.max(cM,.01),Math.max(cW,.01)],
        backgroundColor:['rgba(66,133,244,.7)','rgba(155,89,182,.7)','rgba(37,211,102,.7)'],
        borderColor:['#4285f4','#9b59b6','#25d366'], borderWidth:2 }]
    },
    options: {
      responsive:true, maintainAspectRatio:false, cutout:'65%',
      plugins: {
        legend: { position:'bottom', labels:{color:'#555E7A',font:{size:10},boxWidth:10,padding:10} },
        tooltip:{ backgroundColor:'#0A0F1E', titleColor:'#fff', bodyColor:'#9AA0B4' }
      }
    }
  });
}

function renderMensal(dias, mesNum) {
  document.getElementById('mes-nome').textContent = MESES[(mesNum||1)-1];
  const tG=dias.reduce((s,d)=>s+d.gLeads,0), tM=dias.reduce((s,d)=>s+d.mLeads,0);
  const tW=dias.reduce((s,d)=>s+d.wLeads,0), tT=dias.reduce((s,d)=>s+d.totLeads,0);
  const iT=dias.reduce((s,d)=>s+d.totInvest,0), cT=tT>0?iT/tT:0;
  document.getElementById('monthly-canais').innerHTML = [
    {n:tG,  l:'Leads Google', c:'var(--azul-g)'},
    {n:tM,  l:'Leads Meta',   c:'var(--roxo-m)'},
    {n:tW,  l:'Leads WA',     c:'var(--verde-w)'},
    {n:tT,  l:'Total Leads',  c:'var(--gold)'},
    {n:fR(iT), l:'Investido', c:'var(--branco)'},
    {n:fR(cT), l:'CPL Médio', c:'var(--branco)'},
  ].map(i=>'<div class="monthly-item"><div class="monthly-num" style="color:'+i.c+'">'+i.n+'</div><div class="monthly-lbl">'+i.l+'</div></div>').join('');
}

// ============================================================
//  VENDAS — lê do array vendas retornado pelo doGet
// ============================================================
function renderVendas(data) {
  const vendas  = data.vendas  || [];
  const rows    = data.rows    || [];
  const hoje    = new Date();
  const mesAtual= rows.length ? rows.filter(r=>r.totLeads>0||r.gLeads>0).slice(-1)[0]?.mes || hoje.getMonth()+1 : hoje.getMonth()+1;

  document.getElementById('mes-nome-v').textContent = MESES[(mesAtual||1)-1];

  // Filtra vendas do mês atual
  const vendasMes = vendas.filter(v => {
    const d = new Date(v.data + 'T00:00:00');
    return d.getMonth()+1 === mesAtual;
  });

  if (!vendasMes.length) {
    document.getElementById('v-qtd').textContent    = '0';
    document.getElementById('v-receita').textContent= 'sem registros';
    document.getElementById('v-roas').textContent   = '—';
    document.getElementById('v-conv').textContent   = '—';
    document.getElementById('v-ticket').textContent = '—';
    document.getElementById('v-invest').textContent = '—';
    document.getElementById('v-roas-pill').textContent = 'ROAS —';
    renderCanaisVendas([], data.rows, mesAtual);
    return;
  }

  const totalQtd   = vendasMes.length;
  const totalValor = vendasMes.reduce((s,v) => s + v.valor, 0);
  const ticket     = totalQtd > 0 ? totalValor / totalQtd : 0;

  // Investimento do mês (tráfego pago)
  const diasMes   = (data.rows||[]).filter(r => r.mes === mesAtual);
  const investMes = diasMes.reduce((s,r) => s + r.totInvest, 0);

  // ROAS com canais pagos (exclui Orgânico)
  const vendasPagas = vendasMes.filter(v => v.canal !== 'Orgânico');
  const valorPago   = vendasPagas.reduce((s,v) => s + v.valor, 0);
  const roas        = investMes > 0 ? valorPago / investMes : 0;

  // Conversão total (leads → vendas)
  const totalLeadsMes = diasMes.reduce((s,r) => s + r.totLeads, 0);
  const conv          = totalLeadsMes > 0 ? ((totalQtd / totalLeadsMes)*100).toFixed(1) : 0;

  document.getElementById('v-qtd').textContent    = totalQtd;
  document.getElementById('v-receita').textContent= fRk(totalValor) + ' em receita';
  document.getElementById('v-roas').textContent   = roas > 0 ? roas.toFixed(2) + 'x' : '—';
  document.getElementById('v-conv').textContent   = conv > 0 ? conv + '% conv lead→venda' : '—';
  document.getElementById('v-ticket').textContent = ticket > 0 ? fRk(ticket) : '—';
  document.getElementById('v-invest').textContent = investMes > 0 ? fRk(investMes) + ' investido' : '—';
  document.getElementById('v-roas-pill').textContent = roas > 0 ? 'ROAS ' + roas.toFixed(2) + 'x' : 'ROAS —';

  renderCanaisVendas(vendasMes, diasMes, mesAtual);
}

function renderCanaisVendas(vendasMes, diasMes, mesAtual) {
  const canais = [
    { key:'Google Ads', nome:'Google', cor:'var(--azul-g)' },
    { key:'Meta Ads',   nome:'Meta',   cor:'var(--roxo-m)' },
    { key:'WhatsApp',   nome:'WA',     cor:'var(--verde-w)' },
    { key:'Orgânico',   nome:'Org.',   cor:'var(--gold)' },
  ];

  // Leads por canal no mês (para calcular conversão por canal)
  const leadsCanal = {
    'Google Ads': diasMes.reduce((s,r)=>s+r.gLeads,0),
    'Meta Ads':   diasMes.reduce((s,r)=>s+r.mLeads,0),
    'WhatsApp':   diasMes.reduce((s,r)=>s+r.wLeads,0),
    'Orgânico':   0,
  };

  document.getElementById('v-canais-pagos').innerHTML = canais.map(c => {
    const vends = vendasMes.filter(v => v.canal === c.key);
    const qtd   = vends.length;
    const valor = vends.reduce((s,v) => s+v.valor, 0);
    const leads = leadsCanal[c.key] || 0;
    const conv  = leads > 0 ? ((qtd/leads)*100).toFixed(0) : null;
    return `<div class="vcanal" style="--cc:${c.cor}">
      <div class="vcanal-topo">
        <span class="vcanal-nome">${c.nome}</span>
        ${conv!==null?'<span class="vcanal-conv">'+conv+'%</span>':''}
      </div>
      <div class="vcanal-qtd">${qtd}</div>
      <div class="vcanal-info">${valor>0?fRk(valor):'sem valor'}</div>
    </div>`;
  }).join('');
}

// ============================================================
loadAll();
</script>
</body>
</html>
