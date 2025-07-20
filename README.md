<!DOCTYPE html>
<html>
<head>
 <title>Clicker Game</title>
 <style>
 body {
 font-family: Arial, sans-serif;
 text-align: center;
 background-color: #222;
 color: #fff;
 margin-top:50px;
 }
 h1 {
 font-size:2em;
 }
 #score {
 font-size:1.5em;
 margin:20px 0;
 }
 #stats {
 background-color: #333;
 padding: 15px;
 margin: 20px auto;
 border-radius: 10px;
 max-width: 600px;
 }
 #stats h3 {
 margin-top: 0;
 color: #4CAF50;
 }
 .stat-line {
 margin: 8px 0;
 font-size: 14px;
 }
 .top-stat {
 font-size: 16px;
 font-weight: bold;
 color: #FFD700;
 }
 .big-stats {
 display: flex;
 justify-content: space-around;
 margin: 20px auto;
 max-width: 1200px;
 }
 .stat-box {
 background-color: #333;
 padding: 20px;
 border-radius: 10px;
 width: 45%;
 }
 .stat-box h3 {
 color: #4CAF50;
 margin-top: 0;
 }
 button {
 padding:10px 20px;
 margin:5px;
 font-size:14px;
 cursor: pointer;
 border: none;
 border-radius:5px;
 }
 #clickBtn {
 background-color: #4CAF50;
 color: white;
 font-size: 18px;
 padding: 15px 30px;
 }
 .upgradeBtn {
 background-color: #FF4081;
 color: white;
 }
 .powerBtn {
 background-color: #9C27B0;
 color: white;
 }
 .specialBtn {
 background-color: #FF9800;
 color: white;
 }
 .constructionBtn {
 background-color: #795548;
 color: white;
 }
 .productionBtn {
 background-color: #2196F3;
 color: white;
 }
 .salesBtn {
 background-color: #E91E63;
 color: white;
 }
 .executiveBtn {
 background-color: #9C27B0;
 color: white;
 }
 button:disabled {
 opacity: 0.5;
 cursor: not-allowed;
 }
 .section {
 margin: 20px 0;
 }
 </style>
</head>
<body>

 <h1>MAJESTIC LTD</h1>
 <div id="score">Money: $1000</div>
 
 <div id="stats">
 <h3>Company Overview</h3>
 <div class="stat-line top-stat">Level: <span id="playerLevel">1</span></div>
 <div class="stat-line top-stat">Total Income per Second: $<span id="totalIncome">0</span></div>
 <div class="stat-line top-stat">Total Workers: <span id="totalWorkers">100</span></div>
 <div class="stat-line top-stat">Money per Click: $<span id="clickPower">1</span></div>
 <div class="stat-line">Construction Units: <span id="constructionUnits">0</span></div>
 <div class="stat-line">Total Buildings: <span id="totalBuildings">1</span></div>
 </div>
 
 <button id="clickBtn">Click for Money</button>
 <br>
 
 <div class="section">
 <h3>Level & Upgrades</h3>
 <button class="specialBtn" id="levelUpgradeBtn">Level Up (Unlock Features) - Cost: $<span id="levelCost">1000</span></button>
 </div>

 <div class="section">
 <h3>Basic Upgrades</h3>
 <button class="upgradeBtn" id="clickUpgradeBtn">📻Improve Machine (+$1/click) - Cost: $<span id="clickCost">10</span></button>
 <button class="upgradeBtn" id="autoUpgradeBtn">👨🏻‍💼Hire Worker (+$2/sec) - Cost: $<span id="autoCost">50</span></button>
 <button class="upgradeBtn" id="expWorkerUpgradeBtn">👨🏻‍🔧Hire Experienced Worker (+$8/sec) - Cost: $<span id="expWorkerCost">400</span></button>
 <button class="upgradeBtn" id="managerUpgradeBtn">🤵🏻Add Manager (+$4/sec) - Cost: $<span id="managerCost">250</span></button>
 <button class="upgradeBtn" id="autoHiringUpgradeBtn">🔄Auto Hiring (+$1/sec per second) - Cost: $<span id="autoHiringCost">2000</span></button>
 </div>

 <div class="section">
 <h3>Executive Team (Level 5+ Required)</h3>
 <button class="executiveBtn" id="ceoUpgradeBtn">👔Hire CEO (+$100/sec) - Cost: $<span id="ceoCost">50000</span></button>
 <button class="executiveBtn" id="ctoUpgradeBtn">💻Hire CTO (+$80/sec) - Cost: $<span id="ctoCost">40000</span></button>
 <button class="executiveBtn" id="cfoUpgradeBtn">💰Hire CFO (+$90/sec) - Cost: $<span id="cfoCost">45000</span></button>
 </div>
 
 <div class="section">
 <h3>Construction</h3>
 <button class="constructionBtn" id="constructionUpgradeBtn">🔨Buy Construction Unit - Cost: $<span id="constructionCost">400</span></button>
 <button class="constructionBtn" id="constructionPlantUpgradeBtn">🏗️Build Construction Plant (+$200/sec, +1 unit/40s) - Cost: $<span id="constructionPlantCost">25000</span> | Needs: 5 units</button>
 </div>

 <div class="section">
 <h3>Production Buildings</h3>
 <button class="productionBtn" id="factoryUpgradeBtn">🏭Build Factory (+$100/sec, +500 workers) - Cost: $<span id="factoryCost">5000</span> | Needs: 3 units</button>
 <button class="productionBtn" id="warehouseUpgradeBtn">🏘Build Warehouse (+$350/sec, +1000 workers) - Cost: $<span id="warehouseCost">50000</span> | Needs: 4 units</button>
 <button class="productionBtn" id="farmUpgradeBtn">🚜Build Farm (+$150/sec, +300 workers) - Cost: $<span id="farmCost">20000</span> | Needs: 2 units</button>
 <button class="productionBtn" id="mineUpgradeBtn">⛏️Build Mine (+$400/sec, +600 workers) - Cost: $<span id="mineCost">60000</span> | Needs: 5 units</button>
 <button class="productionBtn" id="powerPlantUpgradeBtn">⚡Build Power Plant (+$800/sec, +400 workers) - Cost: $<span id="powerPlantCost">120000</span> | Needs: 8 units</button>
 <button class="productionBtn" id="oilRigUpgradeBtn">🛢️Build Oil Rig (+$1500/sec, +800 workers) - Cost: $<span id="oilRigCost">250000</span> | Needs: 10 units</button>
 <button class="productionBtn" id="shipyardUpgradeBtn">🚢Build Shipyard (+$2000/sec, +1200 workers) - Cost: $<span id="shipyardCost">400000</span> | Needs: 12 units</button>
 <button class="productionBtn" id="spaceStationUpgradeBtn">🚀Build Space Station (+$5000/sec, +2000 workers) - Cost: $<span id="spaceStationCost">1000000</span> | Needs: 20 units</button>
 </div>

 <div class="section">
 <h3>Sales & Service Buildings</h3>
 <button class="salesBtn" id="storeUpgradeBtn">🏪Open Store (+$500/sec, +20 workers) - Cost: $<span id="storeCost">700</span> | Needs: 1 unit</button>
 <button class="salesBtn" id="officeUpgradeBtn">🏢Open Office (+$1200/sec, +50 workers) - Cost: $<span id="officeCost">15000</span> | Needs: 2 units</button>
 <button class="salesBtn" id="hqUpgradeBtn">🏬Build Headquarters (+$3000/sec, +100 workers) - Cost: $<span id="hqCost">150000</span> | Needs: 8 units</button>
 <button class="salesBtn" id="mallUpgradeBtn">🛍️Build Mall (+$2500/sec, +150 workers) - Cost: $<span id="mallCost">250000</span> | Needs: 6 units</button>
 <button class="salesBtn" id="salesDeptUpgradeBtn">📈Build Sales Department (+$4000/sec, +80 workers) - Cost: $<span id="salesDeptCost">300000</span> | Needs: 7 units</button>
 </div>

 <div class="section">
 <h3>Special Buildings</h3>
 <button class="powerBtn" id="academyUpgradeBtn">🎓Build Academy (+0/sec, +500 workers) - Cost: $<span id="academyCost">30000</span> | Needs: 3 units</button>
 <button class="powerBtn" id="hospitalUpgradeBtn">🏥Build Hospital (+0/sec, +400 workers) - Cost: $<span id="hospitalCost">120000</span> | Needs: 5 units</button>
 <button class="powerBtn" id="universityUpgradeBtn">🎓Build University (+$800/sec, +600 workers) - Cost: $<span id="universityCost">300000</span> | Needs: 6 units</button>
 <button class="powerBtn" id="bankUpgradeBtn">🏦Build Bank (+$3500/sec, +200 workers) - Cost: $<span id="bankCost">200000</span> | Needs: 4 units</button>
 <button class="powerBtn" id="airportUpgradeBtn">✈️Build Airport (+$2800/sec, +800 workers) - Cost: $<span id="airportCost">600000</span> | Needs: 10 units</button>
 </div>

 <div class="section">
 <h3>Advanced Powers</h3>
 <button class="powerBtn" id="corpUpgradeBtn">🌇Start Corporation (+$10000/sec, +1300 workers) - Cost: $<span id="corpCost">500000</span></button>
 <button class="powerBtn" id="cityUpgradeBtn">🏙️Build City (+$8000/sec, +2000 workers) - Cost: $<span id="cityCost">800000</span></button>
 <button class="powerBtn" id="researchLabUpgradeBtn">🔬Build Research Lab (+$1200/sec, +300 workers) - Cost: $<span id="researchLabCost">180000</span></button>
 <button class="powerBtn" id="dataServerUpgradeBtn">💾Build Data Server (+$2200/sec, +100 workers) - Cost: $<span id="dataServerCost">350000</span></button>
 <button class="powerBtn" id="robotFactoryUpgradeBtn">🤖Build Robot Factory (+$3800/sec, +50 workers) - Cost: $<span id="robotFactoryCost">650000</span></button>
 <button class="powerBtn" id="aiCenterUpgradeBtn">🧠Build AI Center (+$6000/sec, +25 workers) - Cost: $<span id="aiCenterCost">1200000</span></button>
 <button class="powerBtn" id="quantumLabUpgradeBtn">⚛️Build Quantum Lab (+$12000/sec, +10 workers) - Cost: $<span id="quantumLabCost">2500000</span></button>
 </div>

 <div class="big-stats">
 <div class="stat-box">
 <h3>Building Stats</h3>
 <div class="stat-line">Stores: <span id="storeCount">1</span></div>
 <div class="stat-line">Factories: <span id="factoryCount">0</span></div>
 <div class="stat-line">Offices: <span id="officeCount">0</span></div>
 <div class="stat-line">Warehouses: <span id="warehouseCount">0</span></div>
 <div class="stat-line">Headquarters: <span id="hqCount">0</span></div>
 <div class="stat-line">Corporations: <span id="corpCount">0</span></div>
 <div class="stat-line">Academies: <span id="academyCount">0</span></div>
 <div class="stat-line">Cities: <span id="cityCount">0</span></div>
 <div class="stat-line">Construction Plants: <span id="constructionPlantCount">0</span></div>
 <div class="stat-line">Farms: <span id="farmCount">0</span></div>
 <div class="stat-line">Banks: <span id="bankCount">0</span></div>
 <div class="stat-line">Hospitals: <span id="hospitalCount">0</span></div>
 <div class="stat-line">Universities: <span id="universityCount">0</span></div>
 <div class="stat-line">Airports: <span id="airportCount">0</span></div>
 <div class="stat-line">Malls: <span id="mallCount">0</span></div>
 <div class="stat-line">Sales Departments: <span id="salesDeptCount">0</span></div>
 <div class="stat-line">Mines: <span id="mineCount">0</span></div>
 <div class="stat-line">Power Plants: <span id="powerPlantCount">0</span></div>
 <div class="stat-line">Oil Rigs: <span id="oilRigCount">0</span></div>
 <div class="stat-line">Shipyards: <span id="shipyardCount">0</span></div>
 <div class="stat-line">Space Stations: <span id="spaceStationCount">0</span></div>
 <div class="stat-line">Research Labs: <span id="researchLabCount">0</span></div>
 <div class="stat-line">Data Servers: <span id="dataServerCount">0</span></div>
 <div class="stat-line">Robot Factories: <span id="robotFactoryCount">0</span></div>
 <div class="stat-line">AI Centers: <span id="aiCenterCount">0</span></div>
 <div class="stat-line">Quantum Labs: <span id="quantumLabCount">0</span></div>
 </div>
 
 <div class="stat-box">
 <h3>Personnel Stats</h3>
 <div class="stat-line">Regular Workers: <span id="workerCount">100</span></div>
 <div class="stat-line">Experienced Workers: <span id="expWorkerCount">0</span></div>
 <div class="stat-line">Managers: <span id="managerCount">1</span></div>
 <div class="stat-line">Auto Hiring Units: <span id="autoHiringCount">0</span></div>
 <div class="stat-line">CEO: <span id="ceoCount">0</span></div>
 <div class="stat-line">CTO: <span id="ctoCount">0</span></div>
 <div class="stat-line">CFO: <span id="cfoCount">0</span></div>
 </div>
 </div>

 <script>
 class ClickerGame {
 constructor() {
 this.score = 1000;
 this.clickPower = 1;
 this.autoPower = 0;
 this.constructionUnits = 0;
 this.playerLevel = 1;
 this.constructionUnitTimer = 0;
 
 // Costs
 this.clickCost = 10;
 this.autoCost = 50;
 this.expWorkerCost = 400;
 this.managerCost = 250;
 this.autoHiringCost = 2000;
 this.ceoCost = 50000;
 this.ctoCost = 40000;
 this.cfoCost = 45000;
 this.levelCost = 1000;
 this.constructionCost = 400;
 this.storeCost = 700;
 this.factoryCost = 5000;
 this.officeCost = 15000;
 this.warehouseCost = 50000;
 this.hqCost = 150000;
 this.corpCost = 500000;
 this.academyCost = 30000;
 this.cityCost = 800000;
 this.constructionPlantCost = 25000;
 this.farmCost = 20000;
 this.bankCost = 200000;
 this.hospitalCost = 120000;
 this.universityCost = 300000;
 this.airportCost = 600000;
 this.mallCost = 250000;
 this.salesDeptCost = 300000;
 this.mineCost = 60000;
 this.powerPlantCost = 120000;
 this.oilRigCost = 250000;
 this.shipyardCost = 400000;
 this.spaceStationCost = 1000000;
 this.researchLabCost = 180000;
 this.dataServerCost = 350000;
 this.robotFactoryCost = 650000;
 this.aiCenterCost = 1200000;
 this.quantumLabCost = 2500000;
 
 // Multipliers
 this.clickCostMultiplier = 1.2;
 this.autoCostMultiplier = 1.3;
 this.expWorkerCostMultiplier = 1.25;
 this.managerCostMultiplier = 1.4;
 this.autoHiringCostMultiplier = 1.3;
 this.levelCostMultiplier = 1.5;
 this.constructionCostMultiplier = 1.15;
 this.storeCostMultiplier = 1.3;
 this.factoryCostMultiplier = 1.2;
 this.officeCostMultiplier = 1.4;
 this.warehouseCostMultiplier = 1.2;
 this.hqCostMultiplier = 1.5;
 this.corpCostMultiplier = 1.7;
 this.academyCostMultiplier = 1.3;
 this.cityCostMultiplier = 1.6;
 this.constructionPlantCostMultiplier = 1.4;
 this.farmCostMultiplier = 1.25;
 this.bankCostMultiplier = 1.5;
 this.hospitalCostMultiplier = 1.3;
 this.universityCostMultiplier = 1.4;
 this.airportCostMultiplier = 1.5;
 this.mallCostMultiplier = 1.35;
 this.salesDeptCostMultiplier = 1.4;
 this.mineCostMultiplier = 1.3;
 this.powerPlantCostMultiplier = 1.4;
 this.oilRigCostMultiplier = 1.5;
 this.shipyardCostMultiplier = 1.6;
 this.spaceStationCostMultiplier = 1.8;
 this.researchLabCostMultiplier = 1.35;
 this.dataServerCostMultiplier = 1.4;
 this.robotFactoryCostMultiplier = 1.5;
 this.aiCenterCostMultiplier = 1.6;
 this.quantumLabCostMultiplier = 1.7;
 
 // Power increments
 this.autoPowerIncrement = 2;
 this.expWorkerPowerIncrement = 8;
 this.managerPowerIncrement = 4;
 this.autoHiringPowerIncrement = 1;
 this.ceoPowerIncrement = 100;
 this.ctoPowerIncrement = 80;
 this.cfoPowerIncrement = 90;
 this.storePowerIncrement = 500;
 this.factoryPowerIncrement = 100;
 this.officePowerIncrement = 1200;
 this.warehousePowerIncrement = 350;
 this.hqPowerIncrement = 3000;
 this.corpPowerIncrement = 10000;
 this.academyPowerIncrement = 0;
 this.hospitalPowerIncrement = 0;
 this.cityPowerIncrement = 8000;
 this.constructionPlantPowerIncrement = 200;
 this.farmPowerIncrement = 150;
 this.bankPowerIncrement = 3500;
 this.universityPowerIncrement = 800;
 this.airportPowerIncrement = 2800;
 this.mallPowerIncrement = 2500;
 this.salesDeptPowerIncrement = 4000;
 this.minePowerIncrement = 400;
 this.powerPlantPowerIncrement = 800;
 this.oilRigPowerIncrement = 1500;
 this.shipyardPowerIncrement = 2000;
 this.spaceStationPowerIncrement = 5000;
 this.researchLabPowerIncrement = 1200;
 this.dataServerPowerIncrement = 2200;
 this.robotFactoryPowerIncrement = 3800;
 this.aiCenterPowerIncrement = 6000;
 this.quantumLabPowerIncrement = 12000;
 
 this.updateInterval = 100;
 
 // Counters
 this.workerCount = 100;
 this.expWorkerCount = 0;
 this.managerCount = 1;
 this.autoHiringCount = 0;
 this.ceoCount = 0;
 this.ctoCount = 0;
 this.cfoCount = 0;
 this.storeCount = 1;
 this.factoryCount = 0;
 this.officeCount = 0;
 this.warehouseCount = 0;
 this.hqCount = 0;
 this.corpCount = 0;
 this.academyCount = 0;
 this.cityCount = 0;
 this.constructionPlantCount = 0;
 this.farmCount = 0;
 this.bankCount = 0;
 this.hospitalCount = 0;
 this.universityCount = 0;
 this.airportCount = 0;
 this.mallCount = 0;
 this.salesDeptCount = 0;
 this.mineCount = 0;
 this.powerPlantCount = 0;
 this.oilRigCount = 0;
 this.shipyardCount = 0;
 this.spaceStationCount = 0;
 this.researchLabCount = 0;
 this.dataServerCount = 0;
 this.robotFactoryCount = 0;
 this.aiCenterCount = 0;
 this.quantumLabCount = 0;

 this.initializeElements();
 this.addEventListeners();
 this.updateDisplay();
 setInterval(this.updateScore.bind(this), this.updateInterval);
 setInterval(this.updateConstructionUnits.bind(this), 1000); // Every second
 }

 initializeElements() {
 this.scoreElement = document.getElementById("score");
 this.clickPowerElement = document.getElementById("clickPower");
 this.constructionUnitsElement = document.getElementById("constructionUnits");
 this.playerLevelElement = document.getElementById("playerLevel");
 this.totalWorkersElement = document.getElementById("totalWorkers");
 this.totalBuildingsElement = document.getElementById("totalBuildings");
 
 // Cost elements
 this.clickCostElement = document.getElementById("clickCost");
 this.autoCostElement = document.getElementById("autoCost");
 this.expWorkerCostElement = document.getElementById("expWorkerCost");
 this.managerCostElement = document.getElementById("managerCost");
 this.autoHiringCostElement = document.getElementById("autoHiringCost");
 this.ceoCostElement = document.getElementById("ceoCost");
 this.ctoCostElement = document.getElementById("ctoCost");
 this.cfoCostElement = document.getElementById("cfoCost");
 this.levelCostElement = document.getElementById("levelCost");
 this.constructionCostElement = document.getElementById("constructionCost");
 this.storeCostElement = document.getElementById("storeCost");
 this.factoryCostElement = document.getElementById("factoryCost");
 this.officeCostElement = document.getElementById("officeCost");
 this.warehouseCostElement = document.getElementById("warehouseCost");
 this.hqCostElement = document.getElementById("hqCost");
 this.corpCostElement = document.getElementById("corpCost");
 this.academyCostElement = document.getElementById("academyCost");
 this.cityCostElement = document.getElementById("cityCost");
 this.constructionPlantCostElement = document.getElementById("constructionPlantCost");
 this.farmCostElement = document.getElementById("farmCost");
 this.bankCostElement = document.getElementById("bankCost");
 this.hospitalCostElement = document.getElementById("hospitalCost");
 this.universityCostElement = document.getElementById("universityCost");
 this.airportCostElement = document.getElementById("airportCost");
 this.mallCostElement = document.getElementById("mallCost");
 this.salesDeptCostElement = document.getElementById("salesDeptCost");
 this.mineCostElement = document.getElementById("mineCost");
 this.powerPlantCostElement = document.getElementById("powerPlantCost");
 this.oilRigCostElement = document.getElementById("oilRigCost");
 this.shipyardCostElement = document.getElementById("shipyardCost");
 this.spaceStationCostElement = document.getElementById("spaceStationCost");
 this.researchLabCostElement = document.getElementById("researchLabCost");
 this.dataServerCostElement = document.getElementById("dataServerCost");
 this.robotFactoryCostElement = document.getElementById("robotFactoryCost");
 this.aiCenterCostElement = document.getElementById("aiCenterCost");
 this.quantumLabCostElement = document.getElementById("quantumLabCost");
 
 // Button elements
 this.clickBtn = document.getElementById("clickBtn");
 this.clickUpgradeBtn = document.getElementById("clickUpgradeBtn");
 this.autoUpgradeBtn = document.getElementById("autoUpgradeBtn");
 this.expWorkerUpgradeBtn = document.getElementById("expWorkerUpgradeBtn");
 this.managerUpgradeBtn = document.getElementById("managerUpgradeBtn");
 this.autoHiringUpgradeBtn = document.getElementById("autoHiringUpgradeBtn");
 this.ceoUpgradeBtn = document.getElementById("ceoUpgradeBtn");
 this.ctoUpgradeBtn = document.getElementById("ctoUpgradeBtn");
 this.cfoUpgradeBtn = document.getElementById("cfoUpgradeBtn");
 this.levelUpgradeBtn = document.getElementById("levelUpgradeBtn");
 this.constructionUpgradeBtn = document.getElementById("constructionUpgradeBtn");
 this.storeUpgradeBtn = document.getElementById("storeUpgradeBtn");
 this.factoryUpgradeBtn = document.getElementById("factoryUpgradeBtn");
 this.officeUpgradeBtn = document.getElementById("officeUpgradeBtn");
 this.warehouseUpgradeBtn = document.getElementById("warehouseUpgradeBtn");
 this.hqUpgradeBtn = document.getElementById("hqUpgradeBtn");
 this.corpUpgradeBtn = document.getElementById("corpUpgradeBtn");
 this.academyUpgradeBtn = document.getElementById("academyUpgradeBtn");
 this.cityUpgradeBtn = document.getElementById("cityUpgradeBtn");
 this.constructionPlantUpgradeBtn = document.getElementById("constructionPlantUpgradeBtn");
 this.farmUpgradeBtn = document.getElementById("farmUpgradeBtn");
 this.bankUpgradeBtn = document.getElementById("bankUpgradeBtn");
 this.hospitalUpgradeBtn = document.getElementById("hospitalUpgradeBtn");
 this.universityUpgradeBtn = document.getElementById("universityUpgradeBtn");
 this.airportUpgradeBtn = document.getElementById("airportUpgradeBtn");
 this.mallUpgradeBtn = document.getElementById("mallUpgradeBtn");
 this.salesDeptUpgradeBtn = document.getElementById("salesDeptUpgradeBtn");
 this.mineUpgradeBtn = document.getElementById("mineUpgradeBtn");
 this.powerPlantUpgradeBtn = document.getElementById("powerPlantUpgradeBtn");
 this.oilRigUpgradeBtn = document.getElementById("oilRigUpgradeBtn");
 this.shipyardUpgradeBtn = document.getElementById("shipyardUpgradeBtn");
 this.spaceStationUpgradeBtn = document.getElementById("spaceStationUpgradeBtn");
 this.researchLabUpgradeBtn = document.getElementById("researchLabUpgradeBtn");
 this.dataServerUpgradeBtn = document.getElementById("dataServerUpgradeBtn");
 this.robotFactoryUpgradeBtn = document.getElementById("robotFactoryUpgradeBtn");
 this.aiCenterUpgradeBtn = document.getElementById("aiCenterUpgradeBtn");
 this.quantumLabUpgradeBtn = document.getElementById("quantumLabUpgradeBtn");
 
 // Stat elements
 this.workerCountElement = document.getElementById("workerCount");
 this.expWorkerCountElement = document.getElementById("expWorkerCount");
 this.managerCountElement = document.getElementById("managerCount");
 this.autoHiringCountElement = document.getElementById("autoHiringCount");
 this.ceoCountElement = document.getElementById("ceoCount");
 this.ctoCountElement =
 this.ctoCountElement = document.getElementById("ctoCount");
 this.cfoCountElement = document.getElementById("cfoCount");
 this.storeCountElement = document.getElementById("storeCount");
 this.factoryCountElement = document.getElementById("factoryCount");
 this.officeCountElement = document.getElementById("officeCount");
 this.warehouseCountElement = document.getElementById("warehouseCount");
 this.hqCountElement = document.getElementById("hqCount");
 this.corpCountElement = document.getElementById("corpCount");
 this.academyCountElement = document.getElementById("academyCount");
 this.cityCountElement = document.getElementById("cityCount");
 this.constructionPlantCountElement = document.getElementById("constructionPlantCount");
 this.farmCountElement = document.getElementById("farmCount");
 this.bankCountElement = document.getElementById("bankCount");
 this.hospitalCountElement = document.getElementById("hospitalCount");
 this.universityCountElement = document.getElementById("universityCount");
 this.airportCountElement = document.getElementById("airportCount");
 this.mallCountElement = document.getElementById("mallCount");
 this.salesDeptCountElement = document.getElementById("salesDeptCount");
 this.mineCountElement = document.getElementById("mineCount");
 this.powerPlantCountElement = document.getElementById("powerPlantCount");
 this.oilRigCountElement = document.getElementById("oilRigCount");
 this.shipyardCountElement = document.getElementById("shipyardCount");
 this.spaceStationCountElement = document.getElementById("spaceStationCount");
 this.researchLabCountElement = document.getElementById("researchLabCount");
 this.dataServerCountElement = document.getElementById("dataServerCount");
 this.robotFactoryCountElement = document.getElementById("robotFactoryCount");
 this.aiCenterCountElement = document.getElementById("aiCenterCount");
 this.quantumLabCountElement = document.getElementById("quantumLabCount");
 this.totalIncomeElement = document.getElementById("totalIncome");
 }

 addEventListeners() {
 this.clickBtn.addEventListener("click", this.handleClick.bind(this));
 this.clickUpgradeBtn.addEventListener("click", this.buyClickUpgrade.bind(this));
 this.autoUpgradeBtn.addEventListener("click", this.buyAutoUpgrade.bind(this));
 this.expWorkerUpgradeBtn.addEventListener("click", this.buyExpWorkerUpgrade.bind(this));
 this.managerUpgradeBtn.addEventListener("click", this.buyManagerUpgrade.bind(this));
 this.autoHiringUpgradeBtn.addEventListener("click", this.buyAutoHiringUpgrade.bind(this));
 this.ceoUpgradeBtn.addEventListener("click", this.buyCeoUpgrade.bind(this));
 this.ctoUpgradeBtn.addEventListener("click", this.buyCtoUpgrade.bind(this));
 this.cfoUpgradeBtn.addEventListener("click", this.buyCfoUpgrade.bind(this));
 this.levelUpgradeBtn.addEventListener("click", this.buyLevelUpgrade.bind(this));
 this.constructionUpgradeBtn.addEventListener("click", this.buyConstructionUpgrade.bind(this));
 this.storeUpgradeBtn.addEventListener("click", this.buyStoreUpgrade.bind(this));
 this.factoryUpgradeBtn.addEventListener("click", this.buyFactoryUpgrade.bind(this));
 this.officeUpgradeBtn.addEventListener("click", this.buyOfficeUpgrade.bind(this));
 this.warehouseUpgradeBtn.addEventListener("click", this.buyWarehouseUpgrade.bind(this));
 this.hqUpgradeBtn.addEventListener("click", this.buyHqUpgrade.bind(this));
 this.corpUpgradeBtn.addEventListener("click", this.buyCorpUpgrade.bind(this));
 this.academyUpgradeBtn.addEventListener("click", this.buyAcademyUpgrade.bind(this));
 this.cityUpgradeBtn.addEventListener("click", this.buyCityUpgrade.bind(this));
 this.constructionPlantUpgradeBtn.addEventListener("click", this.buyConstructionPlantUpgrade.bind(this));
 this.farmUpgradeBtn.addEventListener("click", this.buyFarmUpgrade.bind(this));
 this.bankUpgradeBtn.addEventListener("click", this.buyBankUpgrade.bind(this));
 this.hospitalUpgradeBtn.addEventListener("click", this.buyHospitalUpgrade.bind(this));
 this.universityUpgradeBtn.addEventListener("click", this.buyUniversityUpgrade.bind(this));
 this.airportUpgradeBtn.addEventListener("click", this.buyAirportUpgrade.bind(this));
 this.mallUpgradeBtn.addEventListener("click", this.buyMallUpgrade.bind(this));
 this.salesDeptUpgradeBtn.addEventListener("click", this.buySalesDeptUpgrade.bind(this));
 this.mineUpgradeBtn.addEventListener("click", this.buyMineUpgrade.bind(this));
 this.powerPlantUpgradeBtn.addEventListener("click", this.buyPowerPlantUpgrade.bind(this));
 this.oilRigUpgradeBtn.addEventListener("click", this.buyOilRigUpgrade.bind(this));
 this.shipyardUpgradeBtn.addEventListener("click", this.buyShipyardUpgrade.bind(this));
 this.spaceStationUpgradeBtn.addEventListener("click", this.buySpaceStationUpgrade.bind(this));
 this.researchLabUpgradeBtn.addEventListener("click", this.buyResearchLabUpgrade.bind(this));
 this.dataServerUpgradeBtn.addEventListener("click", this.buyDataServerUpgrade.bind(this));
 this.robotFactoryUpgradeBtn.addEventListener("click", this.buyRobotFactoryUpgrade.bind(this));
 this.aiCenterUpgradeBtn.addEventListener("click", this.buyAiCenterUpgrade.bind(this));
 this.quantumLabUpgradeBtn.addEventListener("click", this.buyQuantumLabUpgrade.bind(this));
 }

 formatMoney(amount) {
 return Math.floor(amount).toLocaleString();
 }

 getTotalBuildings() {
 return this.storeCount + this.factoryCount + this.officeCount + this.warehouseCount + 
        this.hqCount + this.corpCount + this.academyCount + this.cityCount + 
        this.constructionPlantCount + this.farmCount + this.bankCount + this.hospitalCount + 
        this.universityCount + this.airportCount + this.mallCount + this.salesDeptCount +
        this.mineCount + this.powerPlantCount + this.oilRigCount + this.shipyardCount +
        this.spaceStationCount + this.researchLabCount + this.dataServerCount + 
        this.robotFactoryCount + this.aiCenterCount + this.quantumLabCount;
 }

 getTotalWorkers() {
 return this.workerCount + this.expWorkerCount + this.managerCount + this.autoHiringCount + 
        this.ceoCount + this.ctoCount + this.cfoCount;
 }

 updateDisplay() {
 this.scoreElement.textContent = `Money: $${this.formatMoney(this.score)}`;
 this.clickPowerElement.textContent = this.clickPower;
 this.constructionUnitsElement.textContent = this.constructionUnits;
 this.playerLevelElement.textContent = this.playerLevel;
 this.totalWorkersElement.textContent = this.formatMoney(this.getTotalWorkers());
 this.totalBuildingsElement.textContent = this.getTotalBuildings();
 
 // Update all cost displays
 this.clickCostElement.textContent = this.formatMoney(this.clickCost);
 this.autoCostElement.textContent = this.formatMoney(this.autoCost);
 this.expWorkerCostElement.textContent = this.formatMoney(this.expWorkerCost);
 this.managerCostElement.textContent = this.formatMoney(this.managerCost);
 this.autoHiringCostElement.textContent = this.formatMoney(this.autoHiringCost);
 this.ceoCostElement.textContent = this.formatMoney(this.ceoCost);
 this.ctoCostElement.textContent = this.formatMoney(this.ctoCost);
 this.cfoCostElement.textContent = this.formatMoney(this.cfoCost);
 this.levelCostElement.textContent = this.formatMoney(this.levelCost);
 this.constructionCostElement.textContent = this.formatMoney(this.constructionCost);
 this.storeCostElement.textContent = this.formatMoney(this.storeCost);
 this.factoryCostElement.textContent = this.formatMoney(this.factoryCost);
 this.officeCostElement.textContent = this.formatMoney(this.officeCost);
 this.warehouseCostElement.textContent = this.formatMoney(this.warehouseCost);
 this.hqCostElement.textContent = this.formatMoney(this.hqCost);
 this.corpCostElement.textContent = this.formatMoney(this.corpCost);
 this.academyCostElement.textContent = this.formatMoney(this.academyCost);
 this.cityCostElement.textContent = this.formatMoney(this.cityCost);
 this.constructionPlantCostElement.textContent = this.formatMoney(this.constructionPlantCost);
 this.farmCostElement.textContent = this.formatMoney(this.farmCost);
 this.bankCostElement.textContent = this.formatMoney(this.bankCost);
 this.hospitalCostElement.textContent = this.formatMoney(this.hospitalCost);
 this.universityCostElement.textContent = this.formatMoney(this.universityCost);
 this.airportCostElement.textContent = this.formatMoney(this.airportCost);
 this.mallCostElement.textContent = this.formatMoney(this.mallCost);
 this.salesDeptCostElement.textContent = this.formatMoney(this.salesDeptCost);
 this.mineCostElement.textContent = this.formatMoney(this.mineCost);
 this.powerPlantCostElement.textContent = this.formatMoney(this.powerPlantCost);
 this.oilRigCostElement.textContent = this.formatMoney(this.oilRigCost);
 this.shipyardCostElement.textContent = this.formatMoney(this.shipyardCost);
 this.spaceStationCostElement.textContent = this.formatMoney(this.spaceStationCost);
 this.researchLabCostElement.textContent = this.formatMoney(this.researchLabCost);
 this.dataServerCostElement.textContent = this.formatMoney(this.dataServerCost);
 this.robotFactoryCostElement.textContent = this.formatMoney(this.robotFactoryCost);
 this.aiCenterCostElement.textContent = this.formatMoney(this.aiCenterCost);
 this.quantumLabCostElement.textContent = this.formatMoney(this.quantumLabCost);
 
 // Update stats
 this.workerCountElement.textContent = this.formatMoney(this.workerCount);
 this.expWorkerCountElement.textContent = this.formatMoney(this.expWorkerCount);
 this.managerCountElement.textContent = this.formatMoney(this.managerCount);
 this.autoHiringCountElement.textContent = this.formatMoney(this.autoHiringCount);
 this.ceoCountElement.textContent = this.ceoCount;
 this.ctoCountElement.textContent = this.ctoCount;
 this.cfoCountElement.textContent = this.cfoCount;
 this.storeCountElement.textContent = this.storeCount;
 this.factoryCountElement.textContent = this.factoryCount;
 this.officeCountElement.textContent = this.officeCount;
 this.warehouseCountElement.textContent = this.warehouseCount;
 this.hqCountElement.textContent = this.hqCount;
 this.corpCountElement.textContent = this.corpCount;
 this.academyCountElement.textContent = this.academyCount;
 this.cityCountElement.textContent = this.cityCount;
 this.constructionPlantCountElement.textContent = this.constructionPlantCount;
 this.farmCountElement.textContent = this.farmCount;
 this.bankCountElement.textContent = this.bankCount;
 this.hospitalCountElement.textContent = this.hospitalCount;
 this.universityCountElement.textContent = this.universityCount;
 this.airportCountElement.textContent = this.airportCount;
 this.mallCountElement.textContent = this.mallCount;
 this.salesDeptCountElement.textContent = this.salesDeptCount;
 this.mineCountElement.textContent = this.mineCount;
 this.powerPlantCountElement.textContent = this.powerPlantCount;
 this.oilRigCountElement.textContent = this.oilRigCount;
 this.shipyardCountElement.textContent = this.shipyardCount;
 this.spaceStationCountElement.textContent = this.spaceStationCount;
 this.researchLabCountElement.textContent = this.researchLabCount;
 this.dataServerCountElement.textContent = this.dataServerCount;
 this.robotFactoryCountElement.textContent = this.robotFactoryCount;
 this.aiCenterCountElement.textContent = this.aiCenterCount;
 this.quantumLabCountElement.textContent = this.quantumLabCount;
 this.totalIncomeElement.textContent = this.formatMoney(this.autoPower);
 
 // Disable buttons based on requirements
 this.ceoUpgradeBtn.disabled = this.ceoCount >= 1 || this.score < this.ceoCost || this.playerLevel < 5;
 this.ctoUpgradeBtn.disabled = this.ctoCount >= 1 || this.score < this.ctoCost || this.playerLevel < 5;
 this.cfoUpgradeBtn.disabled = this.cfoCount >= 1 || this.score < this.cfoCost || this.playerLevel < 5;
 this.storeUpgradeBtn.disabled = this.constructionUnits < 1 || this.score < this.storeCost;
 this.factoryUpgradeBtn.disabled = this.constructionUnits < 3 || this.score < this.factoryCost;
 this.officeUpgradeBtn.disabled = this.constructionUnits < 2 || this.score < this.officeCost;
 this.warehouseUpgradeBtn.disabled = this.constructionUnits < 4 || this.score < this.warehouseCost;
 this.hqUpgradeBtn.disabled = this.constructionUnits < 8 || this.score < this.hqCost;
 this.constructionPlantUpgradeBtn.disabled = this.constructionUnits < 5 || this.score < this.constructionPlantCost;
 this.farmUpgradeBtn.disabled = this.constructionUnits < 2 || this.score < this.farmCost;
 this.academyUpgradeBtn.disabled = this.constructionUnits < 3 || this.score < this.academyCost;
 this.hospitalUpgradeBtn.disabled = this.constructionUnits < 5 || this.score < this.hospitalCost;
 this.universityUpgradeBtn.disabled = this.constructionUnits < 6 || this.score < this.universityCost;
 this.bankUpgradeBtn.disabled = this.constructionUnits < 4 || this.score < this.bankCost;
 this.airportUpgradeBtn.disabled = this.constructionUnits < 10 || this.score < this.airportCost;
 this.mallUpgradeBtn.disabled = this.constructionUnits < 6 || this.score < this.mallCost;
 this.salesDeptUpgradeBtn.disabled = this.constructionUnits < 7 || this.score < this.salesDeptCost;
 this.mineUpgradeBtn.disabled = this.constructionUnits < 5 || this.score < this.mineCost;
 this.powerPlantUpgradeBtn.disabled = this.constructionUnits < 8 || this.score < this.powerPlantCost;
 this.oilRigUpgradeBtn.disabled = this.constructionUnits < 10 || this.score < this.oilRigCost;
 this.shipyardUpgradeBtn.disabled = this.constructionUnits < 12 || this.score < this.shipyardCost;
 this.spaceStationUpgradeBtn.disabled = this.constructionUnits < 20 || this.score < this.spaceStationCost;
 }

 handleClick() {
 this.score += this.clickPower;
 this.updateDisplay();
 }

 levelUp() {
 this.playerLevel++;
 }

 buyLevelUpgrade() {
 if (this.score >= this.levelCost) {
 this.score -= this.levelCost;
 this.levelUp();
 this.levelCost = Math.floor(this.levelCost * this.levelCostMultiplier);
 this.updateDisplay();
 }
 }

 buyClickUpgrade() {
 if (this.score >= this.clickCost) {
 this.score -= this.clickCost;
 this.clickPower += 1;
 if (this.clickCost < 7000) {
 this.clickCost = Math.floor(this.clickCost * this.clickCostMultiplier);
 if (this.clickCost > 7000) this.clickCost = 7000;
 }
 this.updateDisplay();
 }
 }

 buyAutoUpgrade() {
 if (this.score >= this.autoCost) {
 this.score -= this.autoCost;
 this.autoPower += this.autoPowerIncrement;
 this.workerCount += 1;
 if (this.autoCost < 3000) {
 this.autoCost = Math.floor(this.autoCost * this.autoCostMultiplier);
 if (this.autoCost > 3000) this.autoCost = 3000;
 }
 this.updateDisplay();
 }
 }

 buyExpWorkerUpgrade() {
 if (this.score >= this.expWorkerCost) {
 this.score -= this.expWorkerCost;
 this.autoPower += this.expWorkerPowerIncrement;
 this.expWorkerCount += 1;
 this.expWorkerCost = Math.floor(this.expWorkerCost * this.expWorkerCostMultiplier);
 this.updateDisplay();
 }
 }

 buyManagerUpgrade() {
 if (this.score >= this.managerCost) {
 this.score -= this.managerCost;
 this.autoPower += this.managerPowerIncrement;
 this.managerCount += 1;
 if (this.managerCost < 6000) {
 this.managerCost = Math.floor(this.managerCost * this.managerCostMultiplier);
 if (this.managerCost > 6000) this.managerCost = 6000;
 }
 this.updateDisplay();
 }
 }

 buyAutoHiringUpgrade() {
 if (this.score >= this.autoHiringCost) {
 this.score -= this.autoHiringCost;
 this.autoHiringCount += 1;
 this.autoHiringCost = Math.floor(this.autoHiringCost * this.autoHiringCostMultiplier);
 this.updateDisplay();
 }
 }

 buyCeoUpgrade() {
 if (this.score >= this.ceoCost && this.ceoCount === 0 && this.playerLevel >= 5) {
 this.score -= this.ceoCost;
 this.autoPower += this.ceoPowerIncrement;
 this.ceoCount = 1;
 this.updateDisplay();
 }
 }

 buyCtoUpgrade() {
 if (this.score >= this.ctoCost && this.ctoCount === 0 && this.playerLevel >= 5) {
 this.score -= this.ctoCost;
 this.autoPower += this.ctoPowerIncrement;
 this.ctoCount = 1;
 this.updateDisplay();
 }
 }

 buyCfoUpgrade() {
 if (this.score >= this.cfoCost && this.cfoCount === 0 && this.playerLevel >= 5) {
 this.score -= this.cfoCost;
 this.autoPower += this.cfoPowerIncrement;
 this.cfoCount = 1;
 this.updateDisplay();
 }
 }

 buyConstructionUpgrade() {
 if (this.score >= this.constructionCost) {
 this.score -= this.constructionCost;
 this.constructionUnits += 1;
 this.constructionCost = Math.floor(this.constructionCost * this.constructionCostMultiplier);
 this.updateDisplay();
 }
 }

 buyStoreUpgrade() {
 if (this.score >= this.storeCost && this.constructionUnits >= 1) {
 this.score -= this.storeCost;
 this.constructionUnits -= 1;
 this.autoPower += this.storePowerIncrement;
 this.storeCount += 1;
 this.workerCount += 20;
 this.storeCost = Math.floor(this.storeCost * this.storeCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyFactoryUpgrade() {
 if (this.score >= this.factoryCost && this.constructionUnits >= 3) {
 this.score -= this.factoryCost;
 this.constructionUnits -= 3;
 this.autoPower += this.factoryPowerIncrement;
 this.factoryCount += 1;
 this.workerCount += 500;
 this.factoryCost = Math.floor(this.factoryCost * this.factoryCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyOfficeUpgrade() {
 if (this.score >= this.officeCost && this.constructionUnits >= 2) {
 this.score -= this.officeCost;
 this.constructionUnits -= 2;
 this.autoPower += this.officePowerIncrement;
 this.officeCount += 1;
 this.workerCount += 50;
 this.officeCost = Math.floor(this.officeCost * this.officeCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyWarehouseUpgrade() {
 if (this.score >= this.warehouseCost && this.constructionUnits >= 4) {
 this.score -= this.warehouseCost;
 this.constructionUnits -= 4;
 this.autoPower += this.warehousePowerIncrement;
 this.warehouseCount += 1;
 this.workerCount += 1000;
 this.warehouseCost = Math.floor(this.warehouseCost * this.warehouseCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyHqUpgrade() {
 if (this.score >= this.hqCost && this.constructionUnits >= 8) {
 this.score -= this.hqCost;
 this.constructionUnits -= 8;
 this.autoPower += this.hqPowerIncrement;
 this.hqCount += 1;
 this.workerCount += 100;
 this.hqCost = Math.floor(this.hqCost * this.hqCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyCorpUpgrade() {
 if (this.score >= this.corpCost) {
 this.score -= this.corpCost;
 this.autoPower += this.corpPowerIncrement;
 this.corpCount += 1;
 this.workerCount += 1300;
 this.corpCost = Math.floor(this.corpCost * this.corpCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyAcademyUpgrade() {
 if (this.score >= this.academyCost && this.constructionUnits >= 3) {
 this.score -= this.academyCost;
 this.constructionUnits -= 3;
 this.academyCount += 1;
 this.workerCount += 500;
 this.academyCost = Math.floor(this.academyCost * this.academyCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyHospitalUpgrade() {
 if (this.score >= this.hospitalCost && this.constructionUnits >= 5) {
 this.score -= this.hospitalCost;
 this.constructionUnits -= 5;
 this.hospitalCount += 1;
 this.workerCount += 400;
 this.hospitalCost = Math.floor(this.hospitalCost * this.hospitalCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyCityUpgrade() {
 if (this.score >= this.cityCost) {
 this.score -= this.cityCost;
 this.autoPower += this.cityPowerIncrement;
 this.cityCount += 1;
 this.workerCount += 2000;
 this.cityCost = Math.floor(this.cityCost * this.cityCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyConstructionPlantUpgrade() {
 if (this.score >= this.constructionPlantCost && this.constructionUnits >= 5) {
 this.score -= this.constructionPlantCost;
 this.constructionUnits -= 5;
 this.autoPower += this.constructionPlantPowerIncrement;
 this.constructionPlantCount += 1;
 this.workerCount += 300;
 this.constructionPlantCost = Math.floor(this.constructionPlantCost * this.constructionPlantCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyFarmUpgrade() {
 if (this.score >= this.farmCost && this.constructionUnits >= 2) {
 this.score -= this.farmCost;
 this.constructionUnits -= 2;
 this.autoPower += this.farmPowerIncrement;
 this.farmCount += 1;
 this.workerCount += 300;
 this.farmCost = Math.floor(this.farmCost * this.farmCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyBankUpgrade() {
 if (this.score >= this.bankCost && this.constructionUnits >= 4) {
 this.score -= this.bankCost;
 this.constructionUnits -= 4;
 this.autoPower += this.bankPowerIncrement;
 this.bankCount += 1;
 this.workerCount += 200;
 this.bankCost = Math.floor(this.bankCost * this.bankCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyUniversityUpgrade() {
 if (this.score >= this.universityCost && this.constructionUnits >= 6) {
 this.score -= this.universityCost;
 this.constructionUnits -= 6;
 this.autoPower += this.universityPowerIncrement;
 this.universityCount += 1;
 this.workerCount += 600;
 this.universityCost = Math.floor(this.universityCost * this.universityCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyAirportUpgrade() {
 if (this.score >= this.airportCost && this.constructionUnits >= 10) {
 this.score -= this.airportCost;
 this.constructionUnits -= 10;
 this.autoPower += this.airportPowerIncrement;
 this.airportCount += 1;
 this.workerCount += 800;
 this.airportCost = Math.floor(this.airportCost * this.airportCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyMallUpgrade() {
 if (this.score >= this.mallCost && this.constructionUnits >= 6) {
 this.score -= this.mallCost;
 this.constructionUnits -= 6;
 this.autoPower += this.mallPowerIncrement;
 this.mallCount += 1;
 this.workerCount += 150;
 this.mallCost = Math.floor(this.mallCost * this.mallCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buySalesDeptUpgrade() {
 if (this.score >= this.salesDeptCost && this.constructionUnits >= 7) {
 this.score -= this.salesDeptCost;
 this.constructionUnits -= 7;
 this.autoPower += this.salesDeptPowerIncrement;
 this.salesDeptCount += 1;
 this.workerCount += 80;
 this.salesDeptCost = Math.floor(this.salesDeptCost * this.salesDeptCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyMineUpgrade() {
 if (this.score >= this.mineCost && this.constructionUnits >= 5) {
 this.score -= this.mineCost;
 this.constructionUnits -= 5;
 this.autoPower += this.minePowerIncrement;
 this.mineCount += 1;
 this.workerCount += 600;
 this.mineCost = Math.floor(this.mineCost * this.mineCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyPowerPlantUpgrade() {
 if (this.score >= this.powerPlantCost && this.constructionUnits >= 8) {
 this.score -= this.powerPlantCost;
 this.constructionUnits -= 8;
 this.autoPower += this.powerPlantPowerIncrement;
 this.powerPlantCount += 1;
 this.workerCount += 400;
 this.powerPlantCost = Math.floor(this.powerPlantCost * this.powerPlantCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyOilRigUpgrade() {
 if (this.score >= this.oilRigCost && this.constructionUnits >= 10) {
 this.score -= this.oilRigCost;
 this.constructionUnits -= 10;
  this.autoPower += this.oilRigPowerIncrement;
 this.oilRigCount += 1;
 this.workerCount += 800;
 this.oilRigCost = Math.floor(this.oilRigCost * this.oilRigCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyShipyardUpgrade() {
 if (this.score >= this.shipyardCost && this.constructionUnits >= 12) {
 this.score -= this.shipyardCost;
 this.constructionUnits -= 12;
 this.autoPower += this.shipyardPowerIncrement;
 this.shipyardCount += 1;
 this.workerCount += 1200;
 this.shipyardCost = Math.floor(this.shipyardCost * this.shipyardCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buySpaceStationUpgrade() {
 if (this.score >= this.spaceStationCost && this.constructionUnits >= 20) {
 this.score -= this.spaceStationCost;
 this.constructionUnits -= 20;
 this.autoPower += this.spaceStationPowerIncrement;
 this.spaceStationCount += 1;
 this.workerCount += 2000;
 this.spaceStationCost = Math.floor(this.spaceStationCost * this.spaceStationCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyResearchLabUpgrade() {
 if (this.score >= this.researchLabCost) {
 this.score -= this.researchLabCost;
 this.autoPower += this.researchLabPowerIncrement;
 this.researchLabCount += 1;
 this.workerCount += 300;
 this.researchLabCost = Math.floor(this.researchLabCost * this.researchLabCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyDataServerUpgrade() {
 if (this.score >= this.dataServerCost) {
 this.score -= this.dataServerCost;
 this.autoPower += this.dataServerPowerIncrement;
 this.dataServerCount += 1;
 this.workerCount += 100;
 this.dataServerCost = Math.floor(this.dataServerCost * this.dataServerCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyRobotFactoryUpgrade() {
 if (this.score >= this.robotFactoryCost) {
 this.score -= this.robotFactoryCost;
 this.autoPower += this.robotFactoryPowerIncrement;
 this.robotFactoryCount += 1;
 this.workerCount += 50;
 this.robotFactoryCost = Math.floor(this.robotFactoryCost * this.robotFactoryCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyAiCenterUpgrade() {
 if (this.score >= this.aiCenterCost) {
 this.score -= this.aiCenterCost;
 this.autoPower += this.aiCenterPowerIncrement;
 this.aiCenterCount += 1;
 this.workerCount += 25;
 this.aiCenterCost = Math.floor(this.aiCenterCost * this.aiCenterCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 buyQuantumLabUpgrade() {
 if (this.score >= this.quantumLabCost) {
 this.score -= this.quantumLabCost;
 this.autoPower += this.quantumLabPowerIncrement;
 this.quantumLabCount += 1;
 this.workerCount += 10;
 this.quantumLabCost = Math.floor(this.quantumLabCost * this.quantumLabCostMultiplier);
 this.levelUp();
 this.updateDisplay();
 }
 }

 updateConstructionUnits() {
 // Construction plants produce 1 unit every 40 seconds
 if (this.constructionPlantCount > 0) {
 this.constructionUnitTimer += 1;
 if (this.constructionUnitTimer >= 40) {
 this.constructionUnits += this.constructionPlantCount;
 this.constructionUnitTimer = 0;
 this.updateDisplay();
 }
 }
 
 // Auto hiring adds workers and income
 if (this.autoHiringCount > 0) {
 this.autoPower += this.autoHiringCount;
 this.workerCount += this.autoHiringCount;
 }
 }

 updateScore() {
 // Add money 10 times per second for smooth flow
 this.score += this.autoPower / 10;
 this.updateDisplay();
 }
 }

 new ClickerGame();
 </script>

</body>
</html>


 
