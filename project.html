<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes, viewport-fit=cover">
  <title>Цифровой двойник · Тверской район · ИТС Москва</title>
  
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="mobile-web-app-capable" content="yes">
  <meta name="theme-color" content="#0b1722">
  <link rel="manifest" href="data:application/manifest+json,{name:'Цифровой двойник Тверской',short_name:'Двойник',icons:[{src:'https://cdn-icons-png.flaticon.com/512/3097/3097180.png',sizes:'192x192'}],start_url:'.',display:'standalone',background_color:'#0b1722',theme_color:'#1a3a52'}">
  
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/leaflet.draw/1.0.4/leaflet.draw.css" />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js"></script>
  
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Inter', sans-serif;
      background: #0b1722;
      min-height: 100vh;
      padding: 12px;
      color: #eef4ff;
    }
    .app-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 14px;
      flex-wrap: wrap;
      gap: 8px;
    }
    .title-section h1 {
      font-weight: 600;
      font-size: 1.4rem;
      color: #ffffff;
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .badge {
      background: #1e3a5f;
      padding: 4px 10px;
      border-radius: 30px;
      font-size: 0.7rem;
      font-weight: 500;
      color: #cbdff5;
      border: 1px solid #356a92;
    }
    .status-bar {
      display: flex;
      gap: 12px;
      background: rgba(15, 30, 45, 0.8);
      backdrop-filter: blur(10px);
      padding: 5px 14px;
      border-radius: 40px;
      border: 1px solid #2c5370;
      font-size: 0.75rem;
    }
    .status-dot { width: 7px; height: 7px; border-radius: 50%; background: #2ecc71; box-shadow: 0 0 6px #2ecc71; margin-right: 4px; }
    
    .dashboard {
      display: grid;
      grid-template-columns: 1.4fr 1fr;
      gap: 14px;
      max-width: 1600px;
      margin: 0 auto;
    }
    @media (max-width: 800px) { .dashboard { grid-template-columns: 1fr; } }
    
    .map-card {
      background: #0f1c28;
      border-radius: 18px;
      border: 1px solid #2a4a66;
      overflow: hidden;
      display: flex;
      flex-direction: column;
    }
    #map { height: 480px; width: 100%; background: #1b2b3a; }
    @media (min-width: 800px) { #map { height: 540px; } }
    
    .map-toolbar {
      padding: 6px 12px;
      background: #0e1a26;
      border-top: 1px solid #253e53;
      display: flex;
      gap: 5px;
      align-items: center;
      flex-wrap: wrap;
    }
    .btn {
      background: #1d3e5c;
      border: 1px solid #346792;
      color: #e2ecf5;
      padding: 6px 12px;
      border-radius: 30px;
      font-weight: 500;
      font-size: 0.75rem;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 5px;
      transition: 0.15s;
      white-space: nowrap;
    }
    .btn i { font-size: 0.85rem; }
    .btn:hover { background: #2a5580; }
    .btn-primary { background: #1e4f73; border-color: #3b82f6; }
    .btn-warning { background: #5e3a1a; border-color: #d97706; }
    .btn-success { background: #1e5a3a; border-color: #2ecc71; }
    
    .right-panel { display: flex; flex-direction: column; gap: 12px; }
    .card {
      background: #0f1c28;
      border-radius: 16px;
      border: 1px solid #2a4a66;
      padding: 12px 14px;
    }
    .card-header {
      display: flex;
      justify-content: space-between;
      margin-bottom: 10px;
      color: #c6dcf5;
      font-weight: 500;
      font-size: 0.85rem;
    }
    .kpi-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
    }
    .kpi {
      background: #132433;
      border-radius: 12px;
      padding: 10px;
      border: 1px solid #244a62;
    }
    .kpi-label { font-size: 0.7rem; color: #98b8d6; margin-bottom: 4px; }
    .kpi-value { font-size: 1.6rem; font-weight: 700; color: #f0f6ff; line-height: 1.2; }
    .unit { font-size: 0.65rem; color: #8daac5; margin-left: 2px; }
    
    .tl-panel { display: flex; gap: 6px; justify-content: space-around; margin: 10px 0; }
    .tl-item { text-align: center; flex: 1; }
    .tl-circle { width: 24px; height: 24px; border-radius: 50%; background: #2c3e50; margin: 0 auto 3px; border: 2px solid #1a3b4e; }
    .tl-circle.red { background: #c0392b; box-shadow: 0 0 6px #c0392b; }
    .tl-circle.yellow { background: #f39c12; box-shadow: 0 0 6px #f39c12; }
    .tl-circle.green { background: #27ae60; box-shadow: 0 0 6px #27ae60; }
    
    .slider-container { display: flex; align-items: center; gap: 8px; margin: 10px 0; }
    input[type="range"] { flex: 1; height: 4px; background: #1f405b; border-radius: 4px; -webkit-appearance: none; }
    input[type="range"]::-webkit-slider-thumb { -webkit-appearance: none; width: 16px; height: 16px; background: #3b82f6; border-radius: 50%; cursor: pointer; border: 2px solid white; }
    
    canvas { width: 100% !important; height: 120px !important; }
    .info-note {
      background: #102433;
      border-radius: 10px;
      padding: 6px 10px;
      font-size: 0.65rem;
      color: #aac2db;
      border-left: 3px solid #3b82f6;
      margin-top: 6px;
    }
    .route-display {
      display: flex;
      gap: 5px;
      margin: 6px 0;
    }
    .route-point {
      flex: 1;
      background: #102433;
      border: 1px solid #2a577b;
      border-radius: 16px;
      padding: 4px 8px;
      font-size: 0.65rem;
      color: #c3daf5;
      overflow: hidden;
      text-overflow: ellipsis;
      white-space: nowrap;
    }
    .flex-row { display: flex; gap: 5px; flex-wrap: wrap; margin-bottom: 5px; }
  </style>
</head>
<body>

<div class="app-header">
  <div class="title-section">
    <h1><i class="fas fa-road"></i> Цифровой двойник <span class="badge"><i class="fas fa-map-pin"></i> Тверской</span></h1>
  </div>
  <div class="status-bar">
    <div class="status-item"><span class="status-dot"></span> Активна</div>
    <div class="status-item"><i class="far fa-clock"></i> <span id="liveTime">--:--:--</span></div>
  </div>
</div>

<div class="dashboard">
  <div class="map-card">
    <div id="map"></div>
    <div class="map-toolbar">
      <button class="btn" onclick="spawnBatch()"><i class="fas fa-plus-circle"></i><span> +3</span></button>
      <button class="btn btn-primary" id="routePickBtn" onclick="toggleRoutePicking()"><i class="fas fa-route"></i><span> Маршрут</span></button>
      <button class="btn" id="selectAreaBtn" onclick="toggleAreaSelection()"><i class="fas fa-vector-square"></i><span> Выделить</span></button>
      <button class="btn btn-warning" onclick="clearAllCars()"><i class="fas fa-trash-alt"></i><span> Очистить</span></button>
      <span style="flex:1; text-align:right; font-size:0.7rem; color:#8daac5;" id="selectionHint"></span>
    </div>
  </div>

  <div class="right-panel">
    <div class="card">
      <div class="card-header"><span><i class="fas fa-chart-bar"></i> Обстановка</span></div>
      <div class="kpi-grid">
        <div class="kpi"><div class="kpi-label"><i class="fas fa-car"></i> Машин</div><div class="kpi-value" id="cars">0</div></div>
        <div class="kpi"><div class="kpi-label"><i class="fas fa-gauge-high"></i> Скорость</div><div class="kpi-value" id="speed">0<span class="unit">км/ч</span></div></div>
        <div class="kpi"><div class="kpi-label"><i class="fas fa-traffic-light"></i> Загрузка</div><div class="kpi-value" id="trafficPercent">0<span class="unit">%</span></div></div>
        <div class="kpi"><div class="kpi-label"><i class="fas fa-hourglass-start"></i> Задержка</div><div class="kpi-value" id="delay">0<span class="unit">сек</span></div></div>
      </div>
    </div>

    <div class="card">
      <div class="card-header"><span><i class="fas fa-traffic-light"></i> Светофоры</span></div>
      <div class="tl-panel" id="trafficLightsPanel"></div>
      <div class="info-note" id="tlHint"><i class="fas fa-sync-alt fa-spin"></i> Определение по маршруту...</div>
    </div>

    <div class="card">
      <div class="card-header"><span><i class="fas fa-sliders-h"></i> Управление</span></div>
      <div class="route-display">
        <div class="route-point" id="startPointDisplay"><i class="fas fa-circle" style="color:#27ae60;"></i> <span>55.7587, 37.6133</span></div>
        <div class="route-point" id="endPointDisplay"><i class="fas fa-flag" style="color:#c0392b;"></i> <span>55.7661, 37.6016</span></div>
      </div>
      <button class="btn" style="margin-bottom:6px;" onclick="resetDefaultRoute()"><i class="fas fa-undo-alt"></i> Сбросить</button>
      
      <div class="slider-container">
        <i class="fas fa-car-side"></i>
        <input type="range" id="carSlider" min="0" max="40" value="8" step="1">
        <span id="sliderValue">8</span>
      </div>
      <div class="flex-row">
        <button class="btn btn-primary" onclick="applySliderCount()">Применить</button>
        <button class="btn" onclick="spawnCarAt(0.5)"><i class="fas fa-location-dot"></i> Центр</button>
        <button class="btn" onclick="removeLastCar()">−1</button>
      </div>
      <div class="flex-row">
        <button class="btn" id="clickSpawnBtn" onclick="toggleClickSpawn()"><i class="fas fa-mouse"></i> Клик</button>
        <button class="btn" id="rushHourBtn" onclick="toggleRushHour()"><i class="fas fa-clock"></i> Час пик</button>
        <button class="btn" onclick="downloadReport()"><i class="fas fa-file-export"></i> Отчёт</button>
      </div>
    </div>

    <div class="card">
      <div class="card-header"><span><i class="fas fa-chart-line"></i> Загрузка (10 мин)</span></div>
      <canvas id="trafficChart"></canvas>
    </div>
  </div>
</div>

<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/leaflet.draw/1.0.4/leaflet.draw.js"></script>

<script>
  (function(){
    "use strict";

    const map = L.map('map', { center: [55.7635, 37.6085], zoom: 15, zoomControl: true });
    L.tileLayer('https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png', {
      attribution: '&copy; OSM, CartoDB', maxZoom: 19
    }).addTo(map);

    const drawnItems = new L.FeatureGroup();
    map.addLayer(drawnItems);
    const drawControl = new L.Control.Draw({
      draw: { polygon: false, polyline: false, circle: false, marker: false, circlemarker: false,
        rectangle: { shapeOptions: { color: '#2dd4bf', weight: 2, fillOpacity: 0.2 } } },
      edit: { featureGroup: drawnItems, remove: true }
    });
    let areaSelectionActive = false;

    // Состояние
    let road = [];
    let roadSegments = [];
    let segmentBounds = [];
    const cars = [];
    let animationFrame = null;
    let trafficHistory = [25, 30, 35, 40, 38, 42, 48, 45, 50, 52];
    let chart;
    let clickSpawnActive = false;
    let routePickingActive = false, routePickStage = 0;
    let tempStart = null, tempEnd = null, tempMarker = null;
    let rushHourActive = false, rushInterval = null;
    let routeLengthKm = 1.2;
    let trafficLights = [];
    const tlMarkers = [];

    const carsSpan = document.getElementById('cars');
    const speedSpan = document.getElementById('speed');
    const trafficPercentSpan = document.getElementById('trafficPercent');
    const delaySpan = document.getElementById('delay');
    const liveTimeSpan = document.getElementById('liveTime');
    const slider = document.getElementById('carSlider');
    const sliderVal = document.getElementById('sliderValue');
    const hint = document.getElementById('selectionHint');
    const startSpan = document.querySelector('#startPointDisplay span');
    const endSpan = document.querySelector('#endPointDisplay span');
    const tlPanel = document.getElementById('trafficLightsPanel');
    const tlHint = document.getElementById('tlHint');

    const defaultStart = [55.7587, 37.6133];
    const defaultEnd   = [55.7661, 37.6016];

    // База перекрёстков Тверской (расширенная)
    const knownIntersections = [
      { lat: 55.7605, lng: 37.6110, name: 'Тверская/Бульвар' },
      { lat: 55.7640, lng: 37.6075, name: 'Тверская/Страстной' },
      { lat: 55.7665, lng: 37.6040, name: 'Пушкинская пл.' },
      { lat: 55.7580, lng: 37.6140, name: 'Охотный ряд' },
      { lat: 55.7622, lng: 37.6095, name: 'Тверская/Газетный' }
    ];

    const GREEN_TIME = 30;
    const YELLOW_TIME = 3;
    const RED_TIME = 30;

    // Улучшенное обнаружение светофоров на маршруте
    function detectTrafficLightsOnRoute(routePoints) {
      const detected = [];
      knownIntersections.forEach(inter => {
        let minDist = Infinity, bestIdx = 0;
        routePoints.forEach((pt, idx) => {
          const d = map.distance(L.latLng(pt), L.latLng([inter.lat, inter.lng]));
          if (d < minDist) { minDist = d; bestIdx = idx; }
        });
        // Увеличим радиус до 250 метров и убедимся, что точка не слишком близко к началу/концу (не менее 5% маршрута)
        const progress = bestIdx / (routePoints.length - 1);
        if (minDist < 250 && progress > 0.05 && progress < 0.95) {
          detected.push({
            id: `tl_${detected.length}`,
            name: inter.name,
            progress: progress,
            state: Math.random() > 0.5 ? 'green' : 'red',
            timer: Math.floor(Math.random() * 20),
            greenTime: GREEN_TIME, yellowTime: YELLOW_TIME, redTime: RED_TIME,
            pos: routePoints[bestIdx]
          });
        }
      });
      // Сортировка по прогрессу и удаление дубликатов (близкие по прогрессу)
      detected.sort((a,b) => a.progress - b.progress);
      const filtered = [];
      detected.forEach(tl => {
        if (filtered.length === 0 || tl.progress - filtered[filtered.length-1].progress > 0.1) {
          filtered.push(tl);
        }
      });
      return filtered.slice(0, 4);
    }

    function updateTrafficLightsUI() {
      tlPanel.innerHTML = '';
      if (trafficLights.length === 0) {
        tlHint.innerHTML = '<i class="fas fa-info-circle"></i> На данном маршруте светофоры не обнаружены.';
        return;
      }
      tlHint.innerHTML = '<i class="fas fa-check-circle" style="color:#27ae60;"></i> Активные светофоры';
      trafficLights.forEach(tl => {
        const div = document.createElement('div');
        div.className = 'tl-item';
        const shortName = tl.name.includes('/') ? tl.name.split('/')[1] : tl.name;
        div.innerHTML = `<div class="tl-circle ${tl.state}" id="${tl.id}"></div><span style="font-size:0.6rem;">${shortName}</span>`;
        tlPanel.appendChild(div);
      });
    }

    function updateTrafficLights(deltaSec = 0.1) {
      trafficLights.forEach(tl => {
        tl.timer += deltaSec;
        if (tl.state === 'green' && tl.timer >= tl.greenTime) { tl.state = 'yellow'; tl.timer = 0; }
        else if (tl.state === 'yellow' && tl.timer >= tl.yellowTime) { tl.state = 'red'; tl.timer = 0; }
        else if (tl.state === 'red' && tl.timer >= tl.redTime) { tl.state = 'green'; tl.timer = 0; }
      });
      tlMarkers.forEach((m, i) => {
        if (trafficLights[i]) {
          m.setLatLng(trafficLights[i].pos);
          m.setStyle({ fillColor: trafficLights[i].state === 'green' ? '#27ae60' : (trafficLights[i].state === 'yellow' ? '#f39c12' : '#c0392b') });
        }
      });
      updateTrafficLightsUI();
    }

    async function fetchOSRMRoute(start, end) {
      try {
        const url = `https://router.project-osrm.org/route/v1/driving/${start[1]},${start[0]};${end[1]},${end[0]}?overview=full&geometries=geojson`;
        const r = await fetch(url); const d = await r.json();
        if (d.routes?.length) {
          const coords = d.routes[0].geometry.coordinates.map(c => [c[1], c[0]]);
          let dist = 0;
          for (let i=1; i<coords.length; i++) dist += map.distance(L.latLng(coords[i-1]), L.latLng(coords[i]));
          routeLengthKm = dist / 1000;
          return coords;
        }
      } catch(e) {}
      return null;
    }

    function buildSegments(roadPoints) {
      const segmentCount = 8;
      const total = roadPoints.length;
      const segSize = Math.floor(total / segmentCount);
      const segments = [], bounds = [];
      for (let i = 0; i < segmentCount; i++) {
        const startIdx = i * segSize;
        const endIdx = (i === segmentCount - 1) ? total - 1 : (i + 1) * segSize;
        segments.push(roadPoints.slice(startIdx, endIdx + 1));
        bounds.push({ start: startIdx / total, end: endIdx / total });
      }
      return { segments, bounds };
    }

    function getSegmentColor(load) {
      if (load < 30) return '#2ecc71'; else if (load < 50) return '#f1c40f'; else if (load < 70) return '#e67e22'; else return '#c0392b';
    }

    function renderSegments() {
      roadSegments.forEach(s => map.removeLayer(s));
      roadSegments = [];
      if (road.length < 2) return;
      const { segments } = buildSegments(road);
      segmentBounds = buildSegments(road).bounds;
      const counts = new Array(segments.length).fill(0);
      cars.forEach(car => {
        for (let i=0; i<segmentBounds.length; i++) {
          if (car.progress >= segmentBounds[i].start && car.progress < segmentBounds[i].end) { counts[i]++; break; }
        }
      });
      segments.forEach((seg, idx) => {
        const localLoad = Math.min(98, counts[idx] * 15 + 12);
        roadSegments.push(L.polyline(seg, { color: getSegmentColor(localLoad), weight: 6, opacity: 0.9 }).addTo(map));
      });
    }

    async function setRoute(start, end) {
      const newRoad = await fetchOSRMRoute(start, end);
      if (newRoad) {
        road = newRoad;
        // Обновление светофоров
        trafficLights = detectTrafficLightsOnRoute(road);
        tlMarkers.forEach(m => map.removeLayer(m));
        tlMarkers.length = 0;
        trafficLights.forEach(tl => {
          const marker = L.circleMarker(tl.pos, { radius: 7, color: '#fff', weight: 2, fillColor: '#27ae60', fillOpacity: 0.9 })
            .addTo(map).bindTooltip(tl.name);
          tlMarkers.push(marker);
        });
        updateTrafficLightsUI();
        renderSegments();
        map.setView(road[Math.floor(road.length/2)], 15);
        startSpan.textContent = `${start[0].toFixed(4)}, ${start[1].toFixed(4)}`;
        endSpan.textContent = `${end[0].toFixed(4)}, ${end[1].toFixed(4)}`;
        return true;
      }
      alert('Не удалось построить маршрут. Убедитесь, что точки находятся на дорогах.');
      return false;
    }

    async function resetDefaultRoute() { await setRoute(defaultStart, defaultEnd); }

    function animateCars() {
      if (!road.length) { animationFrame = requestAnimationFrame(animateCars); return; }
      updateTrafficLights(0.1);
      const speedKmh = 38;
      const speedMs = speedKmh / 3.6;
      const baseProgress = (speedMs * 0.0167) / (routeLengthKm * 1000);
      const loadFactor = Math.max(0.4, 1 - cars.length / 45);
      
      for (let car of cars) {
        let delta = baseProgress * car.speedFactor * loadFactor;
        let nextProgress = car.progress + delta;
        let canMove = true;
        for (let tl of trafficLights) {
          if (tl.state === 'red' && car.progress < tl.progress && nextProgress >= tl.progress) {
            const stopProgress = tl.progress - (5 / (routeLengthKm * 1000));
            car.progress = Math.min(car.progress, stopProgress);
            canMove = false;
            break;
          }
        }
        if (canMove) {
          car.progress = Math.min(nextProgress, 1.0);
        }
        if (car.progress >= 1.0) car.progress = 0.0;
        const total = road.length - 1;
        const idx1 = Math.floor(car.progress * total), idx2 = idx1 + 1;
        if (idx2 < road.length) {
          const frac = (car.progress * total) - idx1;
          const p1 = road[idx1], p2 = road[idx2];
          car.marker.setLatLng([p1[0] + (p2[0]-p1[0])*frac, p1[1] + (p2[1]-p1[1])*frac]);
        }
      }
      renderSegments();
      animationFrame = requestAnimationFrame(animateCars);
    }

    function spawnCarAt(progress = null) {
      if (!road.length) return;
      const prog = (progress !== null) ? progress : Math.random();
      const icon = L.divIcon({ html: '<i class="fas fa-car" style="font-size:18px; color:#ecf0f1;"></i>', iconSize:[24,24], iconAnchor:[12,12] });
      const marker = L.marker(road[0], { icon, zIndexOffset: 500 }).addTo(map);
      cars.push({ marker, progress: prog, speedFactor: 0.85 + Math.random()*0.4 });
      updateStats(); renderSegments();
      return marker;
    }

    window.spawnBatch = () => { for(let i=0;i<3;i++) spawnCarAt(Math.random()); };
    window.removeLastCar = () => { if(cars.length) { map.removeLayer(cars.pop().marker); updateStats(); renderSegments(); } };
    window.clearAllCars = () => { while(cars.length) map.removeLayer(cars.pop().marker); updateStats(); renderSegments(); };
    window.applySliderCount = function() {
      const target = parseInt(slider.value);
      while(cars.length < target) spawnCarAt(Math.random());
      while(cars.length > target) removeLastCar();
    };
    slider.oninput = () => sliderVal.textContent = slider.value;

    window.toggleRushHour = function() {
      rushHourActive = !rushHourActive;
      const btn = document.getElementById('rushHourBtn');
      btn.classList.toggle('btn-success', rushHourActive);
      if (rushHourActive) {
        if (rushInterval) clearInterval(rushInterval);
        rushInterval = setInterval(() => { for(let i=0;i<2;i++) spawnCarAt(Math.random()); }, 2000);
        hint.textContent = 'Режим Час пик активирован';
      } else {
        if (rushInterval) { clearInterval(rushInterval); rushInterval = null; }
        hint.textContent = '';
      }
    };

    window.toggleAreaSelection = function() {
      if (!areaSelectionActive) { map.addControl(drawControl); areaSelectionActive = true; document.getElementById('selectAreaBtn').classList.add('btn-primary'); hint.textContent = 'Выделите прямоугольник'; }
      else { map.removeControl(drawControl); areaSelectionActive = false; document.getElementById('selectAreaBtn').classList.remove('btn-primary'); hint.textContent = ''; drawnItems.clearLayers(); }
    };
    map.on(L.Draw.Event.CREATED, e => {
      const bounds = e.layer.getBounds(); drawnItems.addLayer(e.layer);
      const toRemove = []; cars.forEach((c,i) => { if(bounds.contains(c.marker.getLatLng())) toRemove.push(i); });
      for(let i=toRemove.length-1; i>=0; i--) { map.removeLayer(cars[toRemove[i]].marker); cars.splice(toRemove[i],1); }
      updateStats(); renderSegments(); drawnItems.clearLayers(); toggleAreaSelection();
    });

    function updateStats() {
      const cnt = cars.length; carsSpan.textContent = cnt;
      const avgLoad = Math.min(98, Math.floor(cnt * 7 + 15 + Math.random()*6));
      trafficPercentSpan.textContent = avgLoad + '%';
      speedSpan.textContent = Math.max(20, Math.floor(55 - avgLoad * 0.45));
      delaySpan.textContent = Math.floor(avgLoad * 0.8 + 2);
      trafficHistory.push(avgLoad); if(trafficHistory.length>10) trafficHistory.shift();
      if(chart) chart.data.datasets[0].data = trafficHistory;
      chart.update();
    }

    function initChart() {
      const ctx = document.getElementById('trafficChart').getContext('2d');
      chart = new Chart(ctx, { type:'line', data:{ labels: Array.from({length:10},(_,i)=>i+1), datasets:[{ data:trafficHistory, borderColor:'#3b82f6', borderWidth:3, tension:0.3 }] }, options:{ responsive:true, maintainAspectRatio:false, plugins:{legend:{display:false}}, scales:{ y:{max:100, grid:{color:'#2a4a66'}, ticks:{color:'#b0cce6'}}, x:{ticks:{color:'#b0cce6'}} } } });
    }

    function updateClock() { liveTimeSpan.textContent = new Date().toLocaleTimeString('ru-RU', { hour12: false }); }
    setInterval(updateClock, 1000); updateClock();
    setInterval(updateStats, 3000);

    window.toggleClickSpawn = function() {
      clickSpawnActive = !clickSpawnActive;
      document.getElementById('clickSpawnBtn').classList.toggle('btn-primary', clickSpawnActive);
      if(clickSpawnActive) { map.on('click', e => { if(!road.length) return; let minD=Infinity, bestP=0; road.forEach((p,i)=>{ const d=map.distance(e.latlng, L.latLng(p)); if(d<minD){ minD=d; bestP=i/(road.length-1); }}); spawnCarAt(bestP); }); hint.textContent='Кликните на дороге'; }
      else { map.off('click'); hint.textContent=''; }
    };

    window.toggleRoutePicking = function() {
      if(routePickingActive) {
        routePickingActive=routePickStage=0; map.off('click', routePickHandler); document.getElementById('routePickBtn').classList.remove('btn-primary');
        if(tempMarker){ map.removeLayer(tempMarker); tempMarker=null; } hint.textContent='';
      } else {
        if(clickSpawnActive) toggleClickSpawn(); if(areaSelectionActive) toggleAreaSelection();
        routePickingActive=true; routePickStage=1; document.getElementById('routePickBtn').classList.add('btn-primary'); hint.textContent='Кликните: начальная точка'; map.on('click', routePickHandler);
      }
    };
    function routePickHandler(e) {
      if(routePickStage===1){ tempStart=[e.latlng.lat, e.latlng.lng]; if(tempMarker) map.removeLayer(tempMarker); tempMarker=L.marker(tempStart,{icon:L.divIcon({html:'<i class="fas fa-play" style="color:#27ae60;"></i>',iconSize:[20,20]})}).addTo(map); hint.textContent='Теперь конечная точка'; routePickStage=2; }
      else { tempEnd=[e.latlng.lat, e.latlng.lng]; if(tempMarker) map.removeLayer(tempMarker); setRoute(tempStart, tempEnd).then(() => { toggleRoutePicking(); }); }
    }

    window.downloadReport = function() {
      const avgLoad = parseInt(trafficPercentSpan.textContent);
      const rec = avgLoad>70?'Рекомендуется объезд':(avgLoad>40?'Движение умеренное':'Свободно');
      const report = `ДОКЛАД О ДОРОЖНОЙ ОБСТАНОВКЕ\nРайон: Тверской\nВремя: ${new Date().toLocaleString()}\nПротяжённость: ${routeLengthKm.toFixed(2)} км\nМашин: ${cars.length}\nСкорость: ${speedSpan.textContent}\nЗагрузка: ${avgLoad}%\nЗадержка: ${delaySpan.textContent}\nСветофоров: ${trafficLights.length}\nРекомендация: ${rec}`;
      const blob = new Blob([report], {type: 'text/plain'});
      const a = document.createElement('a'); a.href = URL.createObjectURL(blob); a.download = `traffic_report_${Date.now()}.txt`; a.click();
    };

    window.spawnCarAt = spawnCarAt;
    window.resetDefaultRoute = resetDefaultRoute;

    async function init() {
      initChart();
      await setRoute(defaultStart, defaultEnd);
      animationFrame = requestAnimationFrame(animateCars);
      for(let i=0;i<6;i++) spawnCarAt(Math.random());
      updateStats();
    }
    init();
  })();
</script>
</body>
</html>
