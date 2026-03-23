<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
<title>RiskScan PRL — Análisis Visual de Riesgos Laborales</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
<style>
* { box-sizing: border-box; margin: 0; padding: 0; }
body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif; background: #f4f1ea; color: #1a1a1a; min-height: 100vh; font-size: 14px; }
header { background: #1a1a1a; color: #fff; padding: 0 20px; height: 54px; display: flex; align-items: center; justify-content: space-between; position: sticky; top: 0; z-index: 99; }
.logo { font-size: 17px; font-weight: 700; }
.logo em { color: #d94f35; font-style: normal; }
.badge { background: #d94f35; font-size: 9px; font-weight: 700; letter-spacing: .1em; padding: 2px 7px; border-radius: 3px; margin-left: 7px; }
.lang { display: flex; border: 1px solid rgba(255,255,255,.22); border-radius: 5px; overflow: hidden; }
.lang button { background: none; border: none; color: #fff; padding: 5px 13px; cursor: pointer; font-size: 11px; font-weight: 600; font-family: inherit; transition: background .15s; }
.lang button.on { background: #d94f35; }
main { max-width: 860px; margin: 0 auto; padding: 28px 16px 60px; }
.hero { text-align: center; margin-bottom: 26px; }
.hero h1 { font-size: clamp(22px, 4vw, 32px); font-weight: 700; line-height: 1.2; margin-bottom: 10px; }
.hero h1 span { color: #d94f35; }
.hero p { color: #666; font-size: 13px; max-width: 520px; margin: 0 auto; line-height: 1.6; }
.card { background: #fff; border-radius: 12px; padding: 18px; margin-bottom: 13px; border: 1px solid #e5e0d8; }
.card-title { font-weight: 700; font-size: 13px; margin-bottom: 14px; }
.sectors { display: grid; grid-template-columns: repeat(auto-fill, minmax(112px, 1fr)); gap: 7px; }
.sec-btn { border: 1.5px solid #e5e0d8; background: none; border-radius: 8px; padding: 8px 10px; cursor: pointer; font-size: 12px; font-family: inherit; color: #1a1a1a; display: flex; align-items: center; gap: 5px; transition: all .15s; text-align: left; width: 100%; }
.sec-btn:hover { border-color: #d94f35; background: #fdf3f1; }
.sec-btn.sel { border-color: #d94f35; background: #d94f35; color: #fff; }
.upload-zone { border: 2px dashed #ccc; border-radius: 10px; padding: 24px 16px; text-align: center; background: #fafaf8; }
.upload-zone p { color: #888; font-size: 12px; margin-bottom: 11px; }
.pick-btn { background: #1a1a1a; color: #fff; border: none; border-radius: 7px; padding: 11px 22px; font-size: 13px; font-weight: 600; cursor: pointer; font-family: inherit; -webkit-tap-highlight-color: transparent; touch-action: manipulation; display: inline-block; }
.pick-btn:active { opacity: .8; }
.previews { display: grid; grid-template-columns: repeat(auto-fill, minmax(78px, 1fr)); gap: 7px; margin-top: 11px; }
.prev { position: relative; aspect-ratio: 1; border-radius: 7px; overflow: hidden; background: #ddd; }
.prev img { width: 100%; height: 100%; object-fit: cover; display: block; }
.prev canvas { width: 100%; height: 100%; object-fit: cover; display: block; }
.prev .rm { position: absolute; top: 3px; right: 3px; width: 20px; height: 20px; background: rgba(0,0,0,.68); color: #fff; border: none; border-radius: 50%; font-size: 11px; cursor: pointer; display: flex; align-items: center; justify-content: center; font-family: inherit; line-height: 1; }
.prev .video-badge { position: absolute; bottom: 3px; left: 3px; background: rgba(0,0,0,.72); color: #fff; font-size: 9px; font-weight: 700; padding: 2px 5px; border-radius: 3px; letter-spacing: .05em; }
.prev .video-overlay { position: absolute; inset: 0; display: flex; align-items: center; justify-content: center; background: rgba(0,0,0,.35); }
.prev .play-icon { width: 28px; height: 28px; background: rgba(255,255,255,.9); border-radius: 50%; display: flex; align-items: center; justify-content: center; }
.prev .play-icon::after { content: ''; border-left: 9px solid #1a1a1a; border-top: 5px solid transparent; border-bottom: 5px solid transparent; margin-left: 2px; }
textarea { width: 100%; border: 1.5px solid #e5e0d8; border-radius: 8px; padding: 10px 12px; font-family: inherit; font-size: 13px; resize: vertical; min-height: 68px; background: #fafaf8; color: #1a1a1a; outline: none; }
textarea:focus { border-color: #d94f35; }
.err { background: #fde8e4; border: 1px solid #f5bfb3; color: #c0392b; border-radius: 8px; padding: 10px 14px; font-size: 12px; margin-bottom: 10px; display: none; }
.err.show { display: block; }
#analyzeBtn { width: 100%; padding: 14px; background: #bbb; color: #fff; border: none; border-radius: 10px; font-size: 15px; font-weight: 700; cursor: not-allowed; font-family: inherit; transition: background .2s; margin-top: 4px; }
#analyzeBtn.ready { background: #d94f35; cursor: pointer; }
#analyzeBtn.ready:hover { background: #be3d24; }
#loader { display: none; text-align: center; padding: 50px 20px; }
#loader.show { display: block; }
.spinner { width: 38px; height: 38px; border: 3px solid #e5e0d8; border-top-color: #d94f35; border-radius: 50%; animation: spin .8s linear infinite; margin: 0 auto 13px; }
@keyframes spin { to { transform: rotate(360deg); } }
#loader p { color: #666; font-size: 13px; }
/* Video progress bar */
.video-progress { margin-top: 12px; }
.video-progress-bar-wrap { background: #e5e0d8; border-radius: 4px; height: 6px; overflow: hidden; margin-top: 6px; }
.video-progress-bar { background: #d94f35; height: 100%; border-radius: 4px; transition: width .3s ease; width: 0%; }
.video-progress-label { font-size: 11px; color: #888; margin-top: 4px; }
#results { display: none; }
#results.show { display: block; }
.res-top { display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 10px; margin-bottom: 16px; }
.res-top h2 { font-size: 21px; font-weight: 700; }
.exp-btn { padding: 8px 15px; border: 1.5px solid #1a1a1a; border-radius: 7px; background: none; font-size: 12px; font-weight: 700; cursor: pointer; font-family: inherit; transition: all .15s; }
.exp-btn:hover { background: #1a1a1a; color: #fff; }
.stats { display: grid; grid-template-columns: repeat(2, 1fr); gap: 8px; margin-bottom: 14px; }
@media (min-width: 480px) { .stats { grid-template-columns: repeat(4, 1fr); } }
.stat { background: #fff; border: 1px solid #e5e0d8; border-radius: 10px; padding: 12px 14px; text-align: center; }
.stat .n { font-size: 23px; font-weight: 700; line-height: 1; margin-bottom: 3px; }
.stat .l { font-size: 9px; color: #888; text-transform: uppercase; letter-spacing: .07em; }
.sec-title { font-weight: 700; font-size: 13px; border-bottom: 2px solid #e5e0d8; padding-bottom: 6px; margin: 16px 0 10px; }
.summary { font-size: 12px; color: #666; margin-bottom: 12px; line-height: 1.6; }
.risk-card { background: #fff; border: 1px solid #e5e0d8; border-radius: 10px; margin-bottom: 9px; overflow: hidden; }
.risk-head { display: flex; align-items: flex-start; justify-content: space-between; gap: 10px; padding: 12px 14px; cursor: pointer; user-select: none; }
.risk-head:hover { background: #fafaf8; }
.rname { font-weight: 600; font-size: 13px; margin-bottom: 2px; }
.rdesc { font-size: 11px; color: #888; }
.sev { padding: 3px 8px; border-radius: 20px; font-size: 9px; font-weight: 700; letter-spacing: .06em; flex-shrink: 0; }
.sev-alta { background: #fde8e4; color: #c0392b; }
.sev-media { background: #fef3e0; color: #b7770d; }
.sev-baja { background: #e6f4ee; color: #1e7a4a; }
.chev { color: #bbb; font-size: 10px; transition: transform .2s; display: inline-block; flex-shrink: 0; }
.chev.open { transform: rotate(180deg); }
.risk-body { border-top: 1px solid #e5e0d8; padding: 10px 14px; display: none; }
.risk-body.open { display: block; }
.form-item { margin-bottom: 9px; padding: 9px 11px; border-left: 3px solid #d94f35; background: #fafaf8; }
.form-item.rec { border-left-color: #1e7a4a; }
.ftag { font-size: 9px; font-weight: 700; letter-spacing: .1em; margin-bottom: 3px; }
.ftag.ob { color: #d94f35; }
.ftag.re { color: #1e7a4a; }
.fname { font-weight: 600; font-size: 12px; margin-bottom: 3px; }
.fjust { font-size: 11px; color: #666; margin-bottom: 4px; }
.fnorm { display: flex; flex-wrap: wrap; gap: 4px; align-items: center; }
.fnorm > span { font-size: 10px; color: #888; }
.chip { background: #eef0f5; border-radius: 3px; padding: 1px 5px; font-size: 10px; font-family: monospace; }
.benefits { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-top: 14px; }
@media (max-width: 440px) { .benefits { grid-template-columns: 1fr; } }
.ben { border-radius: 10px; padding: 14px; }
.ben.health { background: linear-gradient(135deg, #eaf5f0, #f5faf7); border: 1px solid #b8dece; }
.ben.save { background: linear-gradient(135deg, #fef6e8, #fffcf5); border: 1px solid #f0d89a; }
.ben-title { font-weight: 700; font-size: 12px; margin-bottom: 8px; }
.ben ul { padding-left: 15px; margin: 0; }
.ben li { font-size: 11px; margin-bottom: 4px; }
.new-btn { display: inline-flex; align-items: center; gap: 6px; margin-top: 18px; padding: 9px 18px; border: 1.5px solid #1a1a1a; border-radius: 8px; background: none; cursor: pointer; font-size: 13px; font-weight: 600; font-family: inherit; transition: all .15s; }
.new-btn:hover { background: #1a1a1a; color: #fff; }
footer { text-align: center; padding: 20px; color: #aaa; font-size: 11px; border-top: 1px solid #e5e0d8; margin-top: 30px; }
</style>
</head>
<body>
<header>
  <div class="logo">Risk<em>Scan</em><span class="badge">PRL</span></div>
  <div class="lang">
    <button id="btn-es" class="on" onclick="setLang('es')">ES</button>
    <button id="btn-ca" onclick="setLang('ca')">CA</button>
  </div>
</header>
<main>
  <div class="hero">
    <h1 id="h1">Detecta riesgos laborales desde tus <span>fotos y vídeos</span></h1>
    <p id="hsub">Sube imágenes del lugar de trabajo y obtén un informe completo con formaciones obligatorias, recomendadas y referencias normativas.</p>
  </div>
  <div id="formView">
    <div class="card">
      <div class="card-title" id="t1">1. Selecciona el sector de la empresa</div>
      <div class="sectors" id="sectorGrid"></div>
    </div>
    <div class="card">
      <div class="card-title" id="t2">2. Sube fotos y/o vídeos del lugar de trabajo</div>
      <input type="file" id="fileInput" multiple accept="image/*,video/*" style="display:none" onchange="handleFiles(this)">
      <div class="upload-zone">
        <p id="dzSub">JPG · PNG · MP4 · MOV</p>
        <button class="pick-btn" id="pickBtn" type="button" onclick="document.getElementById('fileInput').click()">📎 Seleccionar archivos</button>
      </div>
      <div class="previews" id="previews"></div>
    </div>
    <div class="card">
      <div class="card-title" id="t3">3. Contexto adicional (opcional)</div>
      <textarea id="ctx" placeholder="Ej: almacén con carretillas elevadoras, turnos nocturnos..."></textarea>
    </div>
    <div class="err" id="errBox"></div>
    <button id="analyzeBtn" onclick="analyze()">🔍 <span id="abtn">Analizar riesgos</span></button>
  </div>
  <div id="loader">
    <div class="spinner"></div>
    <p id="loaderMsg">Analizando imágenes...</p>
    <div id="videoProgressWrap" class="video-progress" style="display:none; max-width:320px; margin:12px auto 0;">
      <div class="video-progress-bar-wrap">
        <div class="video-progress-bar" id="videoProgressBar"></div>
      </div>
      <div class="video-progress-label" id="videoProgressLabel"></div>
    </div>
  </div>
  <div id="results">
    <div class="res-top">
      <h2 id="tRes">Informe de Riesgos</h2>
      <button class="exp-btn" onclick="exportPDF()">📄 <span id="tPdf">Exportar PDF</span></button>
    </div>
    <div class="stats" id="statsRow"></div>
    <p class="summary" id="summaryTxt"></p>
    <div id="riskContainer"></div>
    <div class="benefits" id="benefits"></div>
    <button class="new-btn" onclick="resetApp()">↩ <span id="tNew">Nuevo análisis</span></button>
  </div>
</main>
<footer>
  <p id="footerTxt">RiskScan PRL — Herramienta de apoyo técnico. No sustituye la evaluación profesional según LPRL.</p>
</footer>
<script>
var lang = 'es', sector = null, files = [], result = null;
var TX = {
  es: {
    h1: 'Detecta riesgos laborales desde tus <span>fotos y vídeos</span>',
    hsub: 'Sube imágenes del lugar de trabajo y obtén un informe completo con formaciones obligatorias, recomendadas y referencias normativas.',
    t1: '1. Selecciona el sector de la empresa', t2: '2. Sube fotos y/o vídeos del lugar de trabajo',
    t3: '3. Contexto adicional (opcional)', dzSub: 'JPG · PNG · MP4 · MOV',
    pickBtn: '📎 Seleccionar archivos', abtn: 'Analizar riesgos',
    loadFrames: 'Extrayendo fotogramas del vídeo...', loadAnalyze: 'Analizando imágenes y detectando riesgos...',
    frameProgress: 'Fotograma {n} de {total}',
    noSec: 'Selecciona un sector antes de continuar.', noFiles: 'Sube al menos una imagen o vídeo.',
    videoTooBig: 'El vídeo "{name}" es demasiado grande (máx. 500 MB). Usa un vídeo más corto o comprimido.',
    errApi: 'Error en el análisis', tRes: 'Informe de Riesgos', tPdf: 'Exportar PDF', tNew: 'Nuevo análisis',
    secOb: '🔴 Formaciones Obligatorias por Normativa', secRe: '🟢 Formaciones Recomendadas',
    OB: 'OBLIGATORIA', RE: 'RECOMENDADA', norm: 'Normativa:',
    health: '💚 Mejoras de salud para el trabajador', saving: '💰 Ahorro económico potencial',
    sRisk: 'Riesgos', sOb: 'Oblig.', sRe: 'Recom.', sSav: 'Ahorro/año',
    sev: { alta: 'ALTA', media: 'MEDIA', baja: 'BAJA' },
    ctx: 'Ej: almacén con carretillas elevadoras, turnos nocturnos...',
    footer: 'RiskScan PRL — Herramienta de apoyo técnico. No sustituye la evaluación profesional según LPRL.'
  },
  ca: {
    h1: 'Detecta riscos laborals des de les teves <span>fotos i vídeos</span>',
    hsub: "Puja imatges del lloc de treball i obtén un informe complet amb formacions obligatòries, recomanades i referències normatives.",
    t1: "1. Selecciona el sector de l'empresa", t2: '2. Puja fotos i/o vídeos del lloc de treball',
    t3: '3. Context addicional (opcional)', dzSub: 'JPG · PNG · MP4 · MOV',
    pickBtn: '📎 Seleccionar arxius', abtn: 'Analitzar riscos',
    loadFrames: 'Extraient fotogrames del vídeo...', loadAnalyze: 'Analitzant imatges i detectant riscos...',
    frameProgress: 'Fotograma {n} de {total}',
    noSec: 'Selecciona un sector abans de continuar.', noFiles: 'Puja almenys una imatge o vídeo.',
    videoTooBig: 'El vídeo "{name}" és massa gran (màx. 500 MB). Usa un vídeo més curt o comprimit.',
    errApi: "Error en l'anàlisi", tRes: 'Informe de Riscos', tPdf: 'Exportar PDF', tNew: 'Nova anàlisi',
    secOb: '🔴 Formacions Obligatòries per Normativa', secRe: '🟢 Formacions Recomanades',
    OB: 'OBLIGATÒRIA', RE: 'RECOMANADA', norm: 'Normativa:',
    health: '💚 Millores de salut per al treballador', saving: '💰 Estalvi econòmic potencial',
    sRisk: 'Riscos', sOb: 'Oblig.', sRe: 'Recom.', sSav: 'Estalvi/any',
    sev: { alta: 'ALTA', media: 'MITJA', baja: 'BAIXA' },
    ctx: 'Ex: magatzem amb carretons elevadors, torns nocturns...',
    footer: "RiskScan PRL — Eina de suport tècnic. No substitueix l'avaluació professional segons LPRL."
  }
};
var SECTORS = [
  { id: 'construccion', icon: '🏗️', es: 'Construcción', ca: 'Construcció' },
  { id: 'industria', icon: '🏭', es: 'Industria', ca: 'Indústria' },
  { id: 'logistica', icon: '🚛', es: 'Logística', ca: 'Logística' },
  { id: 'hosteleria', icon: '🍽️', es: 'Hostelería', ca: 'Hostaleria' },
  { id: 'oficinas', icon: '💼', es: 'Oficinas', ca: 'Oficines' },
  { id: 'sanitario', icon: '🏥', es: 'Sanitario', ca: 'Sanitari' },
  { id: 'agricola', icon: '🌾', es: 'Agrícola', ca: 'Agrícola' },
  { id: 'comercio', icon: '🛒', es: 'Comercio', ca: 'Comerç' },
  { id: 'educacion', icon: '🎓', es: 'Educación', ca: 'Educació' },
  { id: 'otro', icon: '🔧', es: 'Otro', ca: 'Altre' }
];

function setLang(l) {
  lang = l;
  document.getElementById('btn-es').className = l === 'es' ? 'on' : '';
  document.getElementById('btn-ca').className = l === 'ca' ? 'on' : '';
  var t = TX[l];
  document.getElementById('h1').innerHTML = t.h1;
  document.getElementById('hsub').textContent = t.hsub;
  document.getElementById('t1').textContent = t.t1;
  document.getElementById('t2').textContent = t.t2;
  document.getElementById('t3').textContent = t.t3;
  document.getElementById('dzSub').textContent = t.dzSub;
  document.getElementById('pickBtn').textContent = t.pickBtn;
  document.getElementById('abtn').textContent = t.abtn;
  document.getElementById('tRes').textContent = t.tRes;
  document.getElementById('tPdf').textContent = t.tPdf;
  document.getElementById('tNew').textContent = t.tNew;
  document.getElementById('ctx').placeholder = t.ctx;
  document.getElementById('footerTxt').textContent = t.footer;
  buildSectors();
  if (result) renderResults(result);
}

function buildSectors() {
  var g = document.getElementById('sectorGrid');
  g.innerHTML = '';
  SECTORS.forEach(function(s) {
    var b = document.createElement('button');
    b.className = 'sec-btn' + (sector === s.id ? ' sel' : '');
    b.dataset.id = s.id;
    b.innerHTML = '<span>' + s.icon + '</span><span>' + s[lang] + '</span>';
    b.onclick = function() {
      sector = s.id;
      document.querySelectorAll('.sec-btn').forEach(function(x) { x.className = 'sec-btn' + (x.dataset.id === s.id ? ' sel' : ''); });
      checkReady();
    };
    g.appendChild(b);
  });
}

function checkReady() {
  var btn = document.getElementById('analyzeBtn');
  var ok = sector && files.length > 0;
  btn.className = ok ? 'ready' : '';
  btn.disabled = !ok;
}

function handleFiles(input) {
  var t = TX[lang];
  var errEl = document.getElementById('errBox');
  Array.from(input.files).forEach(function(f) {
    if (!f.type.startsWith('image/') && !f.type.startsWith('video/')) return;
    if (files.some(function(x) { return x.file.name === f.name && x.file.size === f.size; })) return;
    // Check video size (500 MB max)
    if (f.type.startsWith('video/') && f.size > 500 * 1024 * 1024) {
      errEl.textContent = t.videoTooBig.replace('{name}', f.name);
      errEl.className = 'err show';
      return;
    }
    var entry = { file: f, isVideo: f.type.startsWith('video/'), url: null, thumbCanvas: null };
    files.push(entry);
    // Generate thumbnail for videos
    if (entry.isVideo) {
      generateVideoThumbnail(f, files.length - 1);
    } else {
      entry.url = URL.createObjectURL(f);
    }
    renderPreviews();
    checkReady();
  });
  input.value = '';
}

// Generate a real thumbnail from video first frame
function generateVideoThumbnail(file, idx) {
  var v = document.createElement('video');
  v.muted = true;
  v.playsInline = true;
  v.src = URL.createObjectURL(file);
  v.addEventListener('loadeddata', function() {
    v.currentTime = Math.min(1, v.duration * 0.1);
  });
  v.addEventListener('seeked', function() {
    var c = document.createElement('canvas');
    c.width = 160; c.height = 160;
    var ctx2 = c.getContext('2d');
    // Draw centered crop
    var vw = v.videoWidth, vh = v.videoHeight;
    var scale = Math.max(160/vw, 160/vh);
    var dw = vw*scale, dh = vh*scale;
    ctx2.drawImage(v, (160-dw)/2, (160-dh)/2, dw, dh);
    if (files[idx]) {
      files[idx].thumbCanvas = c;
      renderPreviews();
    }
    URL.revokeObjectURL(v.src);
  });
  v.onerror = function() { URL.revokeObjectURL(v.src); };
  v.load();
}

function renderPreviews() {
  var g = document.getElementById('previews');
  g.innerHTML = '';
  files.forEach(function(e, i) {
    var d = document.createElement('div');
    d.className = 'prev';
    if (e.isVideo) {
      if (e.thumbCanvas) {
        // Show real thumbnail
        var img = document.createElement('img');
        img.src = e.thumbCanvas.toDataURL('image/jpeg', 0.8);
        d.appendChild(img);
      } else {
        // Placeholder while thumbnail loads
        d.innerHTML = '<div style="width:100%;height:100%;display:flex;align-items:center;justify-content:center;font-size:26px;background:#222">🎬</div>';
      }
      // Play overlay icon
      var overlay = document.createElement('div');
      overlay.className = 'video-overlay';
      overlay.innerHTML = '<div class="play-icon"></div>';
      d.appendChild(overlay);
      // Video badge with filename truncated
      var badge = document.createElement('div');
      badge.className = 'video-badge';
      badge.textContent = 'VID';
      d.appendChild(badge);
    } else {
      var img = document.createElement('img');
      img.src = e.url;
      d.appendChild(img);
    }
    var rm = document.createElement('button');
    rm.className = 'rm';
    rm.textContent = '✕';
    (function(idx) { rm.onclick = function(ev) { ev.stopPropagation(); files.splice(idx, 1); renderPreviews(); checkReady(); }; })(i);
    d.appendChild(rm);
    g.appendChild(d);
  });
}

function fileToBase64(file) {
  return new Promise(function(res, rej) {
    var r = new FileReader();
    r.onload = function() { res(r.result.split(',')[1]); };
    r.onerror = rej;
    r.readAsDataURL(file);
  });
}

// Robust video frame extractor — works on mobile Safari, Chrome, Firefox
function extractFrames(file, numFrames) {
  numFrames = numFrames || 5;
  return new Promise(function(resolve) {
    var v = document.createElement('video');
    v.muted = true;
    v.playsInline = true;
    v.preload = 'auto';
    var objectUrl = URL.createObjectURL(file);
    v.src = objectUrl;

    var canvas = document.createElement('canvas');
    var frames = [];
    var frameIdx = 0;
    var seekInProgress = false;
    var timeoutId = null;
    var timestamps = [];

    function cleanup() {
      clearTimeout(timeoutId);
      URL.revokeObjectURL(objectUrl);
    }

    function captureCurrentFrame() {
      canvas.width = Math.min(v.videoWidth || 640, 1280);
      canvas.height = Math.min(v.videoHeight || 360, 720);
      // Maintain aspect ratio
      if (v.videoWidth && v.videoHeight) {
        var ratio = v.videoWidth / v.videoHeight;
        if (canvas.width / canvas.height > ratio) {
          canvas.width = Math.round(canvas.height * ratio);
        } else {
          canvas.height = Math.round(canvas.width / ratio);
        }
      }
      canvas.getContext('2d').drawImage(v, 0, 0, canvas.width, canvas.height);
      var b64 = canvas.toDataURL('image/jpeg', 0.72).split(',')[1];
      frames.push(b64);
    }

    function seekToNext() {
      if (frameIdx >= timestamps.length) {
        cleanup();
        resolve(frames);
        return;
      }
      seekInProgress = true;
      // Timeout fallback: if seeked doesn't fire in 4s, capture what we have and move on
      clearTimeout(timeoutId);
      timeoutId = setTimeout(function() {
        if (seekInProgress) {
          // Try to capture anyway
          try { captureCurrentFrame(); } catch(e) {}
          frameIdx++;
          seekInProgress = false;
          seekToNext();
        }
      }, 4000);
      v.currentTime = timestamps[frameIdx];
    }

    v.addEventListener('seeked', function() {
      if (!seekInProgress) return;
      clearTimeout(timeoutId);
      seekInProgress = false;
      try { captureCurrentFrame(); } catch(e) {}
      frameIdx++;
      // Small delay helps some browsers (especially mobile) stabilize between seeks
      setTimeout(seekToNext, 80);
    });

    function onReady() {
      var duration = v.duration;
      if (!duration || isNaN(duration) || duration === Infinity) {
        // Can't seek — try playing to get duration
        cleanup();
        resolve([]);
        return;
      }
      // Calculate evenly spaced timestamps, skip very start and end
      var step = duration / (numFrames + 1);
      for (var i = 1; i <= numFrames; i++) {
        timestamps.push(Math.min(step * i, duration - 0.1));
      }
      seekToNext();
    }

    v.addEventListener('loadedmetadata', function() {
      // Some browsers need a small play then pause to allow seeking
      if (v.duration && !isNaN(v.duration)) {
        onReady();
      }
    });

    v.addEventListener('durationchange', function() {
      if (v.duration && !isNaN(v.duration) && timestamps.length === 0) {
        onReady();
      }
    });

    v.onerror = function() {
      cleanup();
      resolve(frames); // return what we have
    };

    // Global timeout: if nothing happens in 15s, give up
    var globalTimeout = setTimeout(function() {
      cleanup();
      resolve(frames);
    }, 15000);

    v.addEventListener('loadedmetadata', function() { clearTimeout(globalTimeout); }, { once: false });
    v.load();
  });
}

function setProgress(pct, label) {
  var wrap = document.getElementById('videoProgressWrap');
  var bar = document.getElementById('videoProgressBar');
  var lbl = document.getElementById('videoProgressLabel');
  if (pct >= 0) {
    wrap.style.display = 'block';
    bar.style.width = pct + '%';
    lbl.textContent = label || '';
  } else {
    wrap.style.display = 'none';
  }
}
</script>
<script>
async function analyze() {
  var t = TX[lang];
  var errEl = document.getElementById('errBox');
  errEl.className = 'err';
  if (!sector) { errEl.textContent = t.noSec; errEl.className = 'err show'; return; }
  if (!files.length) { errEl.textContent = t.noFiles; errEl.className = 'err show'; return; }

  document.getElementById('formView').style.display = 'none';
  document.getElementById('loader').className = 'show';
  document.getElementById('results').className = '';

  var loaderMsg = document.getElementById('loaderMsg');
  var imageContents = [];

  for (var i = 0; i < files.length; i++) {
    var entry = files[i];
    if (entry.isVideo) {
      loaderMsg.textContent = t.loadFrames;
      setProgress(0, '');
      var numFrames = 5;
      var frames = await extractFrames(entry.file, numFrames);
      frames.forEach(function(b64, j) {
        var pct = Math.round(((j + 1) / frames.length) * 100);
        var label = t.frameProgress.replace('{n}', j+1).replace('{total}', frames.length);
        setProgress(pct, label);
        imageContents.push({ type: 'text', text: 'Vídeo "' + entry.file.name + '" — Fotograma ' + (j+1) + ' de ' + frames.length + ':' });
        imageContents.push({ type: 'image', source: { type: 'base64', media_type: 'image/jpeg', data: b64 } });
      });
      if (frames.length === 0) {
        // Fallback: no frames extracted, note it as context
        imageContents.push({ type: 'text', text: 'Vídeo adjunto: "' + entry.file.name + '" (no se pudieron extraer fotogramas — analiza en base al contexto y sector).' });
      }
      setProgress(-1);
    } else {
      loaderMsg.textContent = t.loadAnalyze;
      var b64 = await fileToBase64(entry.file);
      imageContents.push({ type: 'text', text: 'Imagen: ' + entry.file.name });
      imageContents.push({ type: 'image', source: { type: 'base64', media_type: entry.file.type || 'image/jpeg', data: b64 } });
    }
  }

  loaderMsg.textContent = t.loadAnalyze;
  setProgress(-1);

  var sectorLabel = SECTORS.find(function(s) { return s.id === sector; })[lang];
  var ctx = document.getElementById('ctx').value.trim();
  var respLang = lang === 'ca' ? 'catalán' : 'castellano';

  var payload = {
    model: 'claude-sonnet-4-20250514',
    max_tokens: 4000,
    system: 'Eres un experto en Prevención de Riesgos Laborales (PRL) en España con profundo conocimiento de la LPRL (Ley 31/1995), sus reglamentos de desarrollo y los criterios del INSST. Respondes siempre en ' + respLang + '. Analiza todas las imágenes y responde ÚNICAMENTE con un JSON válido, sin texto adicional, sin bloques de código: {"sector":"","resumen":"","riesgos":[{"nombre":"","descripcion":"","severidad":"alta|media|baja","formaciones":[{"nombre":"","tipo":"obligatoria|recomendada","justificacion":"","normativa":[]}]}],"saludMejoras":[],"ahorroEconomico":[],"ahorroEstimado":""}. Detecta TODOS los riesgos visibles. Cita normativa española real.',
    messages: [{ role: 'user', content: [{ type: 'text', text: 'Sector: ' + sectorLabel + (ctx ? '. Contexto: ' + ctx : '') + '.' }].concat(imageContents) }]
  };

  try {
    var resp = await fetch('/api/analyze', { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify(payload) });
    if (!resp.ok) { var ed = await resp.json().catch(function() { return {}; }); throw new Error((ed.error && ed.error.message) || 'HTTP ' + resp.status); }
    var data = await resp.json();
    var raw = data.content.map(function(b) { return b.text || ''; }).join('').replace(/^```[\w]*\s*/m, '').replace(/\s*```\s*$/m, '').trim();
    result = JSON.parse(raw);
    document.getElementById('loader').className = '';
    renderResults(result);
    document.getElementById('results').className = 'show';
    document.getElementById('results').scrollIntoView({ behavior: 'smooth' });
  } catch (err) {
    document.getElementById('loader').className = '';
    document.getElementById('formView').style.display = '';
    errEl.textContent = t.errApi + ': ' + err.message;
    errEl.className = 'err show';
  }
}

function renderResults(data) {
  var t = TX[lang];
  var obSet = new Set(), reSet = new Set();
  data.riesgos.forEach(function(r) { r.formaciones.forEach(function(f) { if (f.tipo === 'obligatoria') obSet.add(f.nombre); else reSet.add(f.nombre); }); });
  document.getElementById('statsRow').innerHTML =
    '<div class="stat"><div class="n" style="color:#d94f35">' + data.riesgos.length + '</div><div class="l">' + TX[lang].sRisk + '</div></div>' +
    '<div class="stat"><div class="n" style="color:#b7770d">' + obSet.size + '</div><div class="l">' + TX[lang].sOb + '</div></div>' +
    '<div class="stat"><div class="n" style="color:#1e7a4a">' + reSet.size + '</div><div class="l">' + TX[lang].sRe + '</div></div>' +
    '<div class="stat"><div class="n" style="font-size:13px;color:#1e7a4a;padding-top:5px">' + (data.ahorroEstimado || '—') + '</div><div class="l">' + TX[lang].sSav + '</div></div>';
  document.getElementById('summaryTxt').textContent = data.resumen || '';
  var c = document.getElementById('riskContainer'); c.innerHTML = '';
  var obR = data.riesgos.filter(function(r) { return r.formaciones.some(function(f) { return f.tipo === 'obligatoria'; }); });
  var reR = data.riesgos.filter(function(r) { return r.formaciones.some(function(f) { return f.tipo === 'recomendada'; }) && !r.formaciones.some(function(f) { return f.tipo === 'obligatoria'; }); });
  function addSection(title, risks) {
    if (!risks.length) return;
    var h = document.createElement('div'); h.className = 'sec-title'; h.textContent = title; c.appendChild(h);
    risks.forEach(function(r) { c.appendChild(buildRiskCard(r, TX[lang])); });
  }
  addSection(TX[lang].secOb, obR);
  addSection(TX[lang].secRe, reR);
  document.getElementById('benefits').innerHTML =
    '<div class="ben health"><div class="ben-title">' + TX[lang].health + '</div><ul>' + (data.saludMejoras || []).map(function(m) { return '<li>' + m + '</li>'; }).join('') + '</ul></div>' +
    '<div class="ben save"><div class="ben-title">' + TX[lang].saving + '</div><ul>' + (data.ahorroEconomico || []).map(function(m) { return '<li>' + m + '</li>'; }).join('') + '</ul></div>';
}

function buildRiskCard(risk, t) {
  var div = document.createElement('div'); div.className = 'risk-card';
  var head = document.createElement('div'); head.className = 'risk-head';
  head.innerHTML = '<div style="flex:1"><div class="rname">' + risk.nombre + '</div><div class="rdesc">' + risk.descripcion + '</div></div><div style="display:flex;align-items:center;gap:7px;flex-shrink:0"><span class="sev sev-' + risk.severidad + '">' + (t.sev[risk.severidad] || risk.severidad.toUpperCase()) + '</span><span class="chev">▼</span></div>';
  var body = document.createElement('div'); body.className = 'risk-body';
  risk.formaciones.forEach(function(f) {
    var ob = f.tipo === 'obligatoria';
    body.innerHTML += '<div class="form-item' + (ob ? '' : ' rec') + '"><div class="ftag ' + (ob ? 'ob' : 're') + '">' + (ob ? t.OB : t.RE) + '</div><div class="fname">' + f.nombre + '</div><div class="fjust">' + f.justificacion + '</div><div class="fnorm"><span>' + t.norm + '</span>' + (f.normativa || []).map(function(n) { return '<span class="chip">' + n + '</span>'; }).join('') + '</div></div>';
  });
  head.onclick = function() { var open = body.classList.toggle('open'); head.querySelector('.chev').classList.toggle('open', open); };
  div.appendChild(head); div.appendChild(body); return div;
}

function exportPDF() {
  if (!result) return;
  var t = TX[lang];
  var jsPDF = window.jspdf.jsPDF;
  var doc = new jsPDF({ unit: 'mm', format: 'a4' });
  var lm = 15, pw = 180, y = 15;
  function line(txt, size, bold, color, indent) {
    size = size || 10; bold = bold || false; color = color || [30,30,30]; indent = indent || 0;
    doc.setFontSize(size); doc.setFont('helvetica', bold ? 'bold' : 'normal'); doc.setTextColor(color[0], color[1], color[2]);
    doc.splitTextToSize(txt, pw - indent).forEach(function(l) { if (y > 280) { doc.addPage(); y = 15; } doc.text(l, lm + indent, y); y += size * 0.44; }); y += 1;
  }
  doc.setFillColor(26,26,26); doc.rect(0,0,210,14,'F');
  doc.setFontSize(11); doc.setFont('helvetica','bold'); doc.setTextColor(255,255,255);
  doc.text('RiskScan PRL — ' + t.tRes, 10, 9);
  doc.setFontSize(8); doc.setFont('helvetica','normal');
  doc.text(new Date().toLocaleDateString('es-ES'), 170, 9);
  y = 22;
  line(result.sector || '', 10, false, [100,100,100]);
  y += 2; line(result.resumen || '', 10, false, [80,80,80]); y += 4;
  result.riesgos.forEach(function(r) {
    if (y > 260) { doc.addPage(); y = 15; }
    doc.setFillColor(245,241,235); doc.rect(lm-2, y-4, pw+4, 8, 'F');
    line(r.nombre + ' [' + (t.sev[r.severidad] || r.severidad.toUpperCase()) + ']', 11, true, [26,26,26]);
    line(r.descripcion, 9, false, [120,120,120]);
    r.formaciones.forEach(function(f) {
      var ob = f.tipo === 'obligatoria';
      line('• [' + (ob ? t.OB : t.RE) + '] ' + f.nombre, 9, true, ob ? [217,79,53] : [30,122,74], 3);
      line(f.justificacion, 9, false, [80,80,80], 6);
      line(t.norm + ' ' + (f.normativa || []).join(' | '), 8, false, [150,150,150], 6);
    }); y += 3;
  });
  y += 4; line(t.health, 11, true, [30,122,74]);
  (result.saludMejoras || []).forEach(function(m) { line('• ' + m, 9, false, [60,60,60], 3); });
  y += 3; line(t.saving, 11, true, [183,119,13]);
  (result.ahorroEconomico || []).forEach(function(m) { line('• ' + m, 9, false, [60,60,60], 3); });
  if (result.ahorroEstimado) { y += 3; line(t.sSav + ': ' + result.ahorroEstimado, 10, true, [30,122,74]); }
  doc.save('RiskScan_PRL_Informe.pdf');
}

function resetApp() {
  files = []; sector = null; result = null;
  document.getElementById('previews').innerHTML = '';
  document.getElementById('ctx').value = '';
  document.getElementById('errBox').className = 'err';
  document.getElementById('results').className = '';
  document.getElementById('formView').style.display = '';
  setProgress(-1);
  checkReady();
  document.querySelectorAll('.sec-btn').forEach(function(b) { b.className = 'sec-btn'; });
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

buildSectors();
</script>
</body>
</html>
