# ozon-analytic<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no">
<meta name="theme-color" content="#07111d">
<title>SNIPER ULTIMATE AI 2.6.1 MULTI-ASSET FIXED</title>
<style>
:root{--bg:#07111d;--p:#101e2d;--p2:#15283a;--line:#263b50;--txt:#e8f1fa;--muted:#8da3b7;--green:#20d69a;--red:#ff6478;--yellow:#ffc857}
*{box-sizing:border-box}body{margin:0;background:var(--bg);color:var(--txt);font:14px Arial,sans-serif}
header{padding:16px;background:#0b1927;border-bottom:1px solid var(--line)}h1{font-size:19px;margin:0 0 5px;letter-spacing:1px}
.sub{font-size:10px;color:var(--muted);letter-spacing:1px}main{max-width:900px;margin:auto;padding:11px}
.panel{background:var(--p);border:1px solid var(--line);border-radius:13px;padding:13px;margin-bottom:11px}
.row{display:flex;align-items:center;justify-content:space-between;gap:8px;flex-wrap:wrap}
.tabs,.tfbar{display:flex;gap:5px;flex-wrap:wrap}
button,select{background:var(--p2);border:1px solid var(--line);color:var(--txt);border-radius:8px;padding:10px 11px;font-size:13px}
button.active{border-color:var(--green);color:var(--green)}button:disabled{opacity:.4}select{min-width:100px}
.small{font-size:11px}.muted{color:var(--muted)}.price{font-size:29px;font-weight:bold;margin:9px 0}
.signal{font-size:21px;font-weight:bold;margin:12px 0}.green{color:var(--green)}.red{color:var(--red)}.yellow{color:var(--yellow)}
.badge{font-size:10px;padding:5px 8px;border-radius:6px;background:#1b3042}
.grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:8px}
.metric{background:#0b1927;padding:10px;border-radius:9px;min-width:0}.metric b{display:block;font-size:16px;margin-top:5px;overflow-wrap:anywhere}
canvas{display:block;width:100%;height:260px;background:#091522;border-radius:9px}#renkoChart{height:370px}#equity{height:145px}
iframe{width:100%;height:330px;border:0;border-radius:9px;background:#091522}
table{width:100%;border-collapse:collapse;font-size:11px}th,td{text-align:left;padding:9px 5px;border-bottom:1px solid var(--line)}
th{color:var(--muted);font-weight:normal}.check{accent-color:var(--green);width:17px;height:17px;vertical-align:middle}
.wide{width:100%;margin-top:8px}.tradeButtons{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-top:12px}
.tradeButtons button{min-height:48px;font-weight:bold;font-size:13px}.buyButton{background:#103a32;border-color:var(--green);color:var(--green)}
.sellButton{background:#3a202b;border-color:var(--red);color:var(--red)}
.footer{text-align:center;color:var(--muted);font-size:10px;padding:12px}input[type=range]{accent-color:var(--green)}
.legend{display:flex;gap:12px;flex-wrap:wrap;margin-top:9px;font-size:10px;color:var(--muted)}
.legend span{display:flex;align-items:center;gap:5px}.dot{width:9px;height:9px;border-radius:50%;display:inline-block}
.assetBtn{display:flex;flex-direction:column;align-items:center;gap:5px;min-width:65px}
.assetLamp{display:block;width:9px;height:9px;border-radius:50%;background:#718096;box-shadow:0 0 5px #718096}
.assetName{font-weight:bold;font-size:12px}.assetDesc{font-size:9px;color:var(--muted)}
.autoGrid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:7px;margin-top:12px}
.autoItem{background:#0b1927;padding:8px;border-radius:8px;font-size:11px}
.autoItem label{display:flex;align-items:center;gap:5px}.autoItem b{margin-right:auto}
@media(min-width:600px){.grid{grid-template-columns:repeat(4,minmax(0,1fr))}.autoGrid{grid-template-columns:repeat(5,minmax(0,1fr))}}
@media(max-width:360px){.tradeButtons{grid-template-columns:1fr}.assetBtn{min-width:56px;padding:9px 7px}}
</style>
</head>
<body>
<header>
<h1>SNIPER ULTIMATE AI <span class="green">2.6.1</span></h1>
<div class="sub" id="headerSub">MULTI-ASSET AUTO RENKO · MOEX · VIRTUAL ONLY</div>
</header>
<main>
<section class="panel">
 <div class="row"><div><b>СИСТЕМА</b><div class="small muted" id="status">Запуск...</div></div><span class="badge">ТОЛЬКО ВИРТУАЛЬНО</span></div>
 <div class="row" style="margin-top:12px">
  <div class="tabs" id="assetTabs">
   <button class="assetBtn active" data-asset="OZON" onclick="selectAsset('OZON')"><i class="assetLamp" id="lamp-OZON"></i><span class="assetName">OZON</span><span class="assetDesc">ОЗОН</span></button>
   <button class="assetBtn" data-asset="TGLD" onclick="selectAsset('TGLD')"><i class="assetLamp" id="lamp-TGLD"></i><span class="assetName">TGLD</span><span class="assetDesc">ЗОЛОТО</span></button>
   <button class="assetBtn" data-asset="LKOH" onclick="selectAsset('LKOH')"><i class="assetLamp" id="lamp-LKOH"></i><span class="assetName">LKOH</span><span class="assetDesc">ЛУКОЙЛ</span></button>
   <button class="assetBtn" data-asset="ROSN" onclick="selectAsset('ROSN')"><i class="assetLamp" id="lamp-ROSN"></i><span class="assetName">ROSN</span><span class="assetDesc">РОСНЕФТЬ</span></button>
   <button class="assetBtn" data-asset="PLZL" onclick="selectAsset('PLZL')"><i class="assetLamp" id="lamp-PLZL"></i><span class="assetName">PLZL</span><span class="assetDesc">ПОЛЮС</span></button>
  </div>
  <button onclick="refreshAll()">↻ Обновить все</button>
 </div>
 <div class="autoGrid" id="autoGrid">
  <div class="autoItem"><label><b>OZON</b><input class="check" type="checkbox" id="auto-OZON" checked onchange="toggleAuto('OZON')"> Авто</label></div>
  <div class="autoItem"><label><b>TGLD</b><input class="check" type="checkbox" id="auto-TGLD" checked onchange="toggleAuto('TGLD')"> Авто</label></div>
  <div class="autoItem"><label><b>LKOH</b><input class="check" type="checkbox" id="auto-LKOH" checked onchange="toggleAuto('LKOH')"> Авто</label></div>
  <div class="autoItem"><label><b>ROSN</b><input class="check" type="checkbox" id="auto-ROSN" checked onchange="toggleAuto('ROSN')"> Авто</label></div>
  <div class="autoItem"><label><b>PLZL</b><input class="check" type="checkbox" id="auto-PLZL" checked onchange="toggleAuto('PLZL')"> Авто</label></div>
 </div>
 <div class="small muted" style="margin-top:9px">Каждый инструмент анализируется независимо. Выключение «Авто» запрещает новые покупки, но уже открытая позиция продолжает сопровождаться и может автоматически закрыться по сигналу Renko.</div>
 <div class="small muted" style="margin-top:5px">Лампочка показывает направление последнего завершённого кирпича Renko: зелёный — вверх, красный — вниз, серый — нет надёжных данных.</div>
</section>

<section class="panel">
 <div class="row"><span class="muted">ПОСЛЕДНЯЯ ЦЕНА MOEX · ЗАВЕРШЁННАЯ МИНУТНАЯ СВЕЧА</span><span id="fresh" class="badge yellow">ОЖИДАНИЕ</span></div>
 <div class="price" id="price">—</div>
 <div class="row small muted"><span>Время данных: <b id="tradeTime">—</b></span><span>Возраст данных: <b id="candleTime">—</b></span></div>
 <div class="small muted" id="priceSource" style="margin-top:8px">Ожидание минутных свечей MOEX.</div>
</section>

<section class="panel">
 <b>ЕДИНЫЙ ПЕРЕКЛЮЧАТЕЛЬ ИНТЕРВАЛОВ</b>
 <div class="tfbar" style="margin-top:10px">
  <button data-tf="1" onclick="changeTF(1)">1 мин</button><button data-tf="5" onclick="changeTF(5)">5 мин</button>
  <button data-tf="15" onclick="changeTF(15)">15 мин</button><button data-tf="30" onclick="changeTF(30)">30 мин</button>
  <button data-tf="60" onclick="changeTF(60)">1 час</button><button data-tf="120" onclick="changeTF(120)">2 часа</button>
  <button data-tf="240" onclick="changeTF(240)">4 часа</button><button data-tf="1440" onclick="changeTF(1440)">1 день</button>
 </div>
 <div class="small muted" style="margin-top:8px">Интервал TradingView, Renko, расчётов и индикаторов переключается одновременно. Счета и открытые позиции при смене интервала сохраняются.</div>
</section>

<section class="panel">
 <div class="row"><b>ГРАФИК TRADINGVIEW</b><span class="badge" id="tvTf">5 МИН</span></div>
 <div style="margin-top:10px"><iframe id="tv" title="TradingView" loading="lazy" allowfullscreen></iframe></div>
 <div class="small muted" style="margin-top:7px">TradingView показывает обычные свечи. Renko ниже строится независимо по данным MOEX.</div>
</section>

<section class="panel">
 <div class="row"><b>ГРАФИК РЕНКО · ФИКСИРОВАННЫЙ ATR</b><span class="badge green" id="renkoState">ЗАГРУЗКА</span></div>
 <canvas id="renkoChart"></canvas>
 <div class="legend">
  <span><i class="dot" style="background:#20d69a"></i>Зелёный блок / BUY</span>
  <span><i class="dot" style="background:#ff6478"></i>Красный блок / SELL</span>
  <span><i class="dot" style="background:#ffc857"></i>Текущая цена MOEX</span>
  <span><i class="dot" style="background:#65a9ff"></i>Цена входа</span>
 </div>
 <div class="grid" style="margin-top:10px">
  <div class="metric"><span class="muted small">Размер коробки</span><b id="boxSize">—</b></div>
  <div class="metric"><span class="muted small">Блоков Ренко</span><b id="brickCount">0</b></div>
  <div class="metric"><span class="muted small">Направление</span><b id="brickTrend">—</b></div>
  <div class="metric"><span class="muted small">Последний блок</span><b id="brickLast">—</b></div>
 </div>
 <div class="grid" style="margin-top:8px">
  <div class="metric"><span class="muted small">ATR по OHLC</span><b id="atrActual">—</b></div>
  <div class="metric"><span class="muted small">Коробка до округления</span><b id="boxRaw">—</b></div>
 </div>
 <div class="small muted" id="renkoInfo" style="margin-top:9px">Ожидание данных.</div>
 <div class="small muted" id="chartTradeInfo" style="margin-top:7px">Пунктирная линия цены и сделки появятся после загрузки данных.</div>
</section>

<section class="panel">
 <b id="signalTitle">СИГНАЛ РЕНКО FIXED ATR</b>
 <div class="signal yellow" id="renkoSignal">WAIT · ОЖИДАНИЕ</div>
 <div class="small muted" id="renkoReason">Загрузка истории.</div>
 <div class="grid" style="margin-top:12px">
  <div class="metric"><span class="muted small">Таймфрейм</span><b id="signalTF">5 мин</b></div>
  <div class="metric"><span class="muted small">Последний разворот</span><b id="reversal">—</b></div>
 </div>
 <div class="small muted" style="margin-top:10px">Покупка — подтверждённый разворот вверх. Продажа — подтверждённый разворот вниз. Шорт не используется. Автоматическая продажа закрывает только имеющуюся виртуальную позицию.</div>
</section>

<section class="panel">
 <div class="row"><b>ПАРАМЕТРЫ RENKO</b><span class="badge">НАСТРОЙКИ</span></div>
 <div class="row" style="margin-top:12px">
  <div><b>Длина ATR</b><div class="small muted">Период расчёта фиксированного размера</div></div>
  <select id="atrSelect" onchange="changeATR(this.value)">
   <option value="14">ATR 14</option><option value="10">ATR 10</option><option value="7">ATR 7</option><option value="5">ATR 5 · БОЛЬШЕ БЛОКОВ</option>
  </select>
 </div>
 <div class="grid" style="margin-top:10px">
  <div class="metric"><span class="muted small">Метод</span><b>ATR Уайлдера</b></div>
  <div class="metric"><span class="muted small">Период ATR</span><b id="atrValue">5</b></div>
  <div class="metric"><span class="muted small">Цена Renko</span><b>Закрытие</b></div>
  <div class="metric"><span class="muted small">Коробка</span><b>½ среднего ATR</b></div>
 </div>
 <div class="small muted" style="margin-top:9px">Коробка калибруется по первым 20 доступным значениям ATR после прогрева. В историческом тесте сделки начинаются только после калибровки. При смене периода ATR Renko полностью перестраивается, но виртуальный счёт и позиция сохраняются.</div>
 <button class="wide" onclick="runBacktest()">ЗАПУСТИТЬ ИСТОРИЧЕСКИЙ ТЕСТ</button>
 <div id="backtestStatus" class="small muted" style="margin-top:9px">Исторический тест ещё не запускался.</div>
 <div style="overflow-x:auto;margin-top:9px"><table><thead><tr><th>Метод</th><th>Сделок</th><th>Прибыль</th><th>Успешность</th><th>Просадка</th></tr></thead><tbody id="backtest"><tr><td colspan="5">Ожидание теста</td></tr></tbody></table></div>
 <div class="grid" style="margin-top:9px">
  <div class="metric"><span class="muted small">Открытый результат теста</span><b id="btOpen">—</b></div>
  <div class="metric"><span class="muted small">Итоговый капитал теста</span><b id="btEquity">—</b></div>
  <div class="metric"><span class="muted small">Открытая позиция теста</span><b id="btPosition">—</b></div>
  <div class="metric"><span class="muted small">Ожидающий сигнал</span><b id="btPending">—</b></div>
 </div>
</section>

<section class="panel">
 <div class="row"><b>ВИРТУАЛЬНЫЙ СЧЁТ · <span id="accountAsset">OZON</span></b><span class="badge green">АВТОРЕЖИМ</span></div>
 <div class="grid" style="margin-top:10px">
  <div class="metric"><span class="muted small">Капитал</span><b id="capital">—</b></div>
  <div class="metric"><span class="muted small">Свободные средства</span><b id="cash">—</b></div>
  <div class="metric"><span class="muted small">Реализованный результат</span><b id="profit">—</b></div>
  <div class="metric"><span class="muted small">Закрытые сделки</span><b id="trades">0</b></div>
  <div class="metric"><span class="muted small">Успешность</span><b id="winrate">—</b></div>
  <div class="metric"><span class="muted small">Открытый результат</span><b id="floating">—</b></div>
  <div class="metric"><span class="muted small">Макс. просадка</span><b id="drawdown">—</b></div>
  <div class="metric"><span class="muted small">Последняя сделка</span><b id="lastDeal">—</b></div>
 </div>
 <div class="tradeButtons">
  <button class="buyButton" id="manualBuy" onclick="manualBuy()">▲ КУПИТЬ ВИРТУАЛЬНО</button>
  <button class="sellButton" id="manualSell" onclick="manualSell()">▼ ПРОДАТЬ ВИРТУАЛЬНО</button>
 </div>
 <div class="small muted" id="manualStatus" style="margin-top:9px">Ручное управление доступно при наличии свежей цены MOEX.</div>
 <div class="small muted" style="margin-top:8px">Стартовый виртуальный капитал каждого инструмента: 1 000 000 ₽. На покупку — до 75% свободных средств. Комиссии и налоги временно не учитываются.</div>
 <button class="wide" onclick="resetCurrent()" style="border-color:var(--red);color:var(--red)">СБРОСИТЬ СЧЁТ ЭТОГО ИНСТРУМЕНТА</button>
</section>

<section class="panel">
 <div class="row"><b>ГОЛОСОВОЙ ПОМОЩНИК</b><label><input type="checkbox" class="check" id="voiceOn" checked onchange="save()"> Голос включён</label></div>
 <div class="row" style="margin-top:10px"><span class="small muted">Громкость</span><input id="volume" type="range" min="0" max="1" step=".1" value=".8" onchange="save()"><button onclick="testVoice()">Проверить голос</button></div>
 <div class="small muted" style="margin-top:8px">Объявляет приближение к развороту, подтверждённые развороты и виртуальные сделки по всем пяти инструментам. Объявления ставятся в общую очередь, не перебивая друг друга. Работа в фоне зависит от ограничений Android и браузера.</div>
</section>

<section class="panel"><b>ОТКРЫТАЯ ПОЗИЦИЯ</b><div id="position" class="small muted" style="margin-top:9px">Открытой позиции нет.</div></section>
<section class="panel">
 <div class="row"><b>КРИВАЯ КАПИТАЛА</b><span class="small muted">Реализованный результат</span></div>
 <canvas id="equity"></canvas><div class="small muted" id="equityInfo" style="margin-top:6px">Ожидание сделок.</div>
</section>
<section class="panel">
 <b>ЖУРНАЛ ВИРТУАЛЬНЫХ СДЕЛОК · <span id="journalAsset">OZON</span></b>
 <div style="overflow-x:auto;margin-top:8px"><table><thead><tr><th>Время</th><th>Операция</th><th>Цена</th><th>Количество</th><th>Результат</th></tr></thead><tbody id="journal"><tr><td colspan="5">Сделок пока нет</td></tr></tbody></table></div>
</section>
<section class="panel">
 <div class="row"><b>ДИАГНОСТИКА MOEX ISS</b><span id="sourceBadge" class="badge yellow">ОЖИДАНИЕ</span></div>
 <div class="grid" style="margin-top:10px">
  <div class="metric"><span class="muted small">Режим</span><b id="board">—</b></div>
  <div class="metric"><span class="muted small">Минутных свечей</span><b id="count">0</b></div>
  <div class="metric"><span class="muted small">Страниц</span><b id="pages">0</b></div>
  <div class="metric"><span class="muted small">Последняя свеча</span><b id="lastBar">—</b></div>
  <div class="metric"><span class="muted small">Свежесть</span><b id="freshness">—</b></div>
  <div class="metric"><span class="muted small">Вход разрешён</span><b id="allowed">НЕТ</b></div>
 </div>
 <div class="small muted" id="diagnostic" style="margin-top:10px;line-height:1.6">Ожидание источника.</div>
</section>
<div class="footer">SNIPER ULTIMATE AI 2.6.1 · MULTI-ASSET AUTO RENKO · VIRTUAL TEST<br>Реальные заявки брокеру не отправляются.</div>
</main>
<script>
"use strict";
const CFG={
 OZON:{ticker:"OZON",market:"shares",boards:["TQBR"],tv:"MOEX:OZON",name:"ОЗОН"},
 TGLD:{ticker:"TGLD",market:"shares",boards:["TQTF","TQBR","TQIF"],tv:"MOEX:TGLD",name:"ЗОЛОТО"},
 LKOH:{ticker:"LKOH",market:"shares",boards:["TQBR"],tv:"MOEX:LKOH",name:"ЛУКОЙЛ"},
 ROSN:{ticker:"ROSN",market:"shares",boards:["TQBR"],tv:"MOEX:ROSN",name:"РОСНЕФТЬ"},
 PLZL:{ticker:"PLZL",market:"shares",boards:["TQBR"],tv:"MOEX:PLZL",name:"ПОЛЮС"}
};
const CAPITAL=1000000,ALLOC=.75,UPDATE=60000,PAGE=500,MAXPAGES=100;
const HISTORY=45,DAILY_HISTORY=365,OFFSET=10800000,MAX_DELAY=20*60000;
const TFS=[1,5,15,30,60,120,240,1440],ATR_OPTIONS=[14,10,7,5],BOX_FACTOR=.5,BOX_SAMPLE=20;
const assets=Object.keys(CFG),$=id=>document.getElementById(id),last=a=>a&&a.length?a[a.length-1]:null;
const money=n=>(Number(n)||0).toLocaleString("ru-RU",{maximumFractionDigits:2})+" ₽";
const fmt=n=>Number.isFinite(Number(n))?Number(n).toLocaleString("ru-RU",{maximumFractionDigits:4}):"—";
const now=()=>Date.now(),key=(a,t,p)=>a+"_"+t+"_ATR"+p+"_FIXED";
function emptyData(){return{bars:[],dailyBars:[],quote:null,price:null,board:"—",pages:0,error:"",updated:0,complete:false,dailyComplete:false,dailyError:"",dailyUpdated:0}}
function emptyBook(){return{cash:CAPITAL,realized:0,position:null,closed:[],events:[],marks:[],bricks:[],box:0,boxRaw:0,atrNow:0,initialized:false,cursor:0,lastReversal:"—",pending:null,renkoState:null,peak:CAPITAL,maxDD:0,equity:CAPITAL,calibrationEnd:0,preWarn:{}}}
let S={asset:"OZON",tf:5,atrPeriod:5,auto:Object.fromEntries(assets.map(a=>[a,true])),loading:Object.fromEntries(assets.map(a=>[a,false])),voice:true,volume:.8,data:Object.fromEntries(assets.map(a=>[a,emptyData()])),books:{}};
function book(asset=S.asset){if(!S.books[asset])S.books[asset]=emptyBook();let b=S.books[asset];["bricks","closed","events","marks"].forEach(k=>{if(!Array.isArray(b[k]))b[k]=[]});if(!b.preWarn)b.preWarn={};return b}
function save(){
 try{
  if($("voiceOn"))S.voice=$("voiceOn").checked;if($("volume"))S.volume=Number($("volume").value);
  assets.forEach(a=>{const e=$("auto-"+a);if(e)S.auto[a]=e.checked});
  localStorage.setItem("sniper_ultimate_260",JSON.stringify({asset:S.asset,tf:S.tf,atrPeriod:S.atrPeriod,auto:S.auto,voice:S.voice,volume:S.volume,books:S.books}));
 }catch(e){console.warn("Сохранение",e)}
}
function restore(){
 try{
  const x=JSON.parse(localStorage.getItem("sniper_ultimate_260")||"null");if(!x)return;
  S.asset=CFG[x.asset]?x.asset:"OZON";S.tf=TFS.includes(+x.tf)?+x.tf:5;S.atrPeriod=ATR_OPTIONS.includes(+x.atrPeriod)?+x.atrPeriod:5;
  S.auto=Object.fromEntries(assets.map(a=>[a,x.auto&&typeof x.auto[a]==="boolean"?x.auto[a]:true]));
  S.voice=x.voice!==false;S.volume=Number.isFinite(+x.volume)?Math.max(0,Math.min(1,+x.volume)):.8;
  S.books=x.books&&typeof x.books==="object"?x.books:{};
 }catch(e){console.warn("Восстановление",e)}
}
restore();
function moscowDate(d){return new Date(d.getTime()+OFFSET).toISOString().slice(0,10)}
function parseDate(v){
 if(!v)return NaN;let s=String(v).trim();if(!s)return NaN;
 if(/^\d{4}-\d\d-\d\d$/.test(s))s+="T00:00:00+03:00";
 else{s=s.replace(" ","T");if(!/[zZ]|[+-]\d\d:\d\d$/.test(s))s+="+03:00"}
 const n=new Date(s).getTime();return Number.isFinite(n)?n:NaN;
}
function age(ms){
 if(!Number.isFinite(ms)||ms<0)return"—";const m=Math.floor(ms/60000);
 if(m<1)return"меньше минуты";if(m<60)return m+" мин.";const h=Math.floor(m/60);
 return h<48?h+" ч. "+m%60+" мин.":Math.floor(h/24)+" дн.";
}
async function json(url){
 const c=new AbortController(),timer=setTimeout(()=>c.abort(),15000);
 try{const r=await fetch(url,{cache:"no-store",signal:c.signal});if(!r.ok)throw Error("HTTP "+r.status);return await r.json()}
 finally{clearTimeout(timer)}
}
function rows(j,k){
 let t=j&&j[k];if(!t&&j&&k.includes(".")){const p=k.split(".");t=j[p[0]]&&j[p[0]][p[1]]}
 if(!t||!Array.isArray(t.columns)||!Array.isArray(t.data))return[];
 return t.data.map(row=>{const o={};t.columns.forEach((c,i)=>o[String(c).toLowerCase()]=row[i]);return o});
}
function cursorTotal(j){
 let t=j&&j["candles.cursor"];if(!t&&j&&j.candles)t=j.candles.cursor;
 if(!t||!t.columns||!t.data||!t.data.length)return null;
 const o={};t.columns.forEach((c,i)=>o[String(c).toLowerCase()]=t.data[0][i]);return Number.isFinite(+o.total)?+o.total:null;
}
function valid(b){return Number.isFinite(b.time)&&b.time>0&&[b.open,b.high,b.low,b.close].every(Number.isFinite)&&b.open>0&&b.high>=Math.max(b.open,b.close)&&b.low<=Math.min(b.open,b.close)&&b.low>0}
async function loadCandles(asset,interval,days){
 const c=CFG[asset],from=moscowDate(new Date(now()-days*86400000)),till=moscowDate(new Date());let error=null;
 for(const board of c.boards){
  try{
   let all=[],start=0,pages=0,total=null,complete=false;
   for(let i=0;i<MAXPAGES;i++){
    const url=`https://iss.moex.com/iss/engines/stock/markets/${c.market}/boards/${board}/securities/${c.ticker}/candles.json?from=${from}&till=${till}&interval=${interval}&start=${start}&limit=${PAGE}&iss.meta=on`;
    const j=await json(url),batch=rows(j,"candles");pages++;const ct=cursorTotal(j);if(ct!==null)total=ct;
    if(!batch.length){complete=true;break}
    for(const r of batch){const b={time:parseDate(r.begin),open:+r.open,high:+r.high,low:+r.low,close:+r.close,volume:+r.volume||0};if(valid(b))all.push(b)}
    start+=batch.length;if(total!==null&&start>=total){complete=true;break}if(batch.length<PAGE){complete=true;break}
    if(i===MAXPAGES-1)complete=false;
   }
   const m=new Map();all.forEach(b=>m.set(b.time,b));const bars=[...m.values()].sort((a,b)=>a.time-b.time);
   if(bars.length)return{bars,pages,board,total,complete};error=Error("Свечи не найдены на "+board);
  }catch(e){error=e}
 }
 throw error||Error("Не удалось загрузить историю MOEX");
}
function bucketStart(time,tf){const unit=tf*60000;return Math.floor((time+OFFSET)/unit)*unit-OFFSET}
function aggregate(bars,tf){
 if(tf===1)return bars.slice();const out=[];
 for(const b of bars){const t=bucketStart(b.time,tf);let x=last(out);
  if(!x||x.time!==t)out.push({time:t,open:b.open,high:b.high,low:b.low,close:b.close,volume:b.volume});
  else{x.high=Math.max(x.high,b.high);x.low=Math.min(x.low,b.low);x.close=b.close;x.volume+=b.volume}
 }return out;
}
function closedBars(bars,tf){const t=now();return bars.filter(b=>b.time+tf*60000<=t)}
function freshness(bars,tf=1){
 const x=last(bars);if(!x)return{stale:true,age:Infinity,bar:null};
 const ms=now()-(x.time+tf*60000);return{stale:ms>MAX_DELAY,age:ms,bar:x};
}
function addATR(bars,period=S.atrPeriod){
 let prev=null,seed=[],atr=null;const out=[];
 for(const b of bars){
  const tr=prev===null?b.high-b.low:Math.max(b.high-b.low,Math.abs(b.high-prev),Math.abs(b.low-prev));
  if(seed.length<period){seed.push(tr);if(seed.length===period)atr=seed.reduce((a,v)=>a+v,0)/period}
  else atr=(atr*(period-1)+tr)/period;
  out.push({...b,atr:atr!==null&&Number.isFinite(atr)&&atr>0?atr:null});prev=b.close;
 }return out;
}
function sourceBars(d,tf=S.tf){return tf===1440?closedBars(d.dailyBars,1440):closedBars(aggregate(d.bars,tf),tf)}
function tickRound(v){return Math.max(.01,Math.round(v*100)/100)}
function calculateFixedBox(bars){
 const vals=bars.map(x=>x.atr).filter(x=>Number.isFinite(x)&&x>0).slice(0,BOX_SAMPLE);
 if(vals.length<BOX_SAMPLE)return{box:0,raw:0,atr:0,count:vals.length};
 const atr=vals.reduce((a,v)=>a+v,0)/vals.length,raw=atr*BOX_FACTOR;
 return{box:tickRound(raw),raw,atr,count:vals.length};
}
function applyRenkoBar(state,bar,out,box){
 const cl=bar.close;if(!(box>0)||!Number.isFinite(cl))return;
 if(!Number.isFinite(state.anchor)){state.anchor=cl;state.dir=0;return}
 let a=state.anchor,d=state.dir,guard=0;
 if(!d){
  if(cl>=a+box){while(cl>=a+box&&guard++<100){out.push({open:a,close:a+box,dir:1,time:bar.time,box});a+=box;d=1}}
  else if(cl<=a-box){while(cl<=a-box&&guard++<100){out.push({open:a,close:a-box,dir:-1,time:bar.time,box});a-=box;d=-1}}
 }else if(d===1){
  while(cl>=a+box&&guard++<100){out.push({open:a,close:a+box,dir:1,time:bar.time,box});a+=box}
  if(cl<=a-2*box&&guard++<100){
   out.push({open:a-box,close:a-2*box,dir:-1,time:bar.time,box});a-=2*box;d=-1;
   while(cl<=a-box&&guard++<100){out.push({open:a,close:a-box,dir:-1,time:bar.time,box});a-=box}
  }
 }else{
  while(cl<=a-box&&guard++<100){out.push({open:a,close:a-box,dir:-1,time:bar.time,box});a-=box}
  if(cl>=a+2*box&&guard++<100){
   out.push({open:a+box,close:a+2*box,dir:1,time:bar.time,box});a+=2*box;d=1;
   while(cl>=a+box&&guard++<100){out.push({open:a,close:a+box,dir:1,time:bar.time,box});a+=box}
  }
 }
 state.anchor=a;state.dir=d;
}
function buildRenko(bars,box){
 const out=[];if(!bars.length||!(box>0))return{bricks:out,state:{anchor:NaN,dir:0}};
 const first=bars.find(x=>Number.isFinite(x.atr));const state={anchor:first?first.close:bars[0].close,dir:0};
 for(const bar of bars)if(Number.isFinite(bar.atr))applyRenkoBar(state,bar,out,box);
 return{bricks:out,state};
}
 function findCalibrationIndex(bars){
 let count=0;
 for(let i=0;i<bars.length;i++){
  if(Number.isFinite(bars[i].atr)&&bars[i].atr>0){
   count++;
   if(count===BOX_SAMPLE)return i;
  }
 }
 return-1;
}

const speechQueue=[];let speaking=false;
function speak(text){
 if(!S.voice||!$("voiceOn")?.checked||!("speechSynthesis"in window))return;
 speechQueue.push(text);if(speechQueue.length>100)speechQueue.shift();runSpeechQueue();
}
function runSpeechQueue(){
 if(speaking||!speechQueue.length||!("speechSynthesis"in window))return;
 speaking=true;const text=speechQueue.shift();
 try{
  const u=new SpeechSynthesisUtterance(text);u.lang="ru-RU";u.rate=.92;u.volume=S.volume;
  u.onend=u.onerror=()=>{speaking=false;setTimeout(runSpeechQueue,180)};
  speechSynthesis.speak(u);
 }catch(e){speaking=false;setTimeout(runSpeechQueue,300)}
}
function announce(type,asset,price,qty,pnl,source="AUTO"){
 const name=CFG[asset].name,method=source==="MANUAL"?"Ручная виртуальная":"Автоматическая виртуальная";
 const text=type==="BUY"
  ?`${name}. ${method} покупка. ${qty} штук. Цена ${fmt(price)} рублей.`
  :`${name}. ${method} продажа. ${qty} штук. Цена ${fmt(price)} рублей. Результат ${pnl>=0?"прибыль":"убыток"} ${money(Math.abs(pnl))}.`;
 speak(text);
}
function announceReversal(asset,dir){
 speak(`${CFG[asset].name}. Подтверждённый разворот Renko ${dir===1?"вверх":"вниз"}.`);
}
function beep(type){
 try{
  const C=window.AudioContext||window.webkitAudioContext;if(!C)return;
  const c=new C(),o=c.createOscillator(),g=c.createGain();
  o.type="sine";o.frequency.value=type==="BUY"?880:440;g.gain.value=.06*S.volume;
  o.connect(g);g.connect(c.destination);o.start();o.stop(c.currentTime+.18);o.onended=()=>c.close();
 }catch(e){}
}
function testVoice(){
 speak("Снайпер. Голосовой помощник работает.");beep("BUY");
}
function logEvent(b,asset,type,price,pnl=0,time=now(),qty=0,source="AUTO"){
 const e={type,price,pnl,time,qty,asset,tf:S.tf,atr:S.atrPeriod,box:b.box,source};
 b.events.unshift(e);b.events=b.events.slice(0,300);b.marks.push(e);b.marks=b.marks.slice(-400);save();
}
function updateEquity(b,price){
 const mark=Number.isFinite(price)&&price>0?price:(b.position?b.position.entry:0);
 const equity=b.cash+(b.position&&mark?b.position.qty*mark:0);if(!Number.isFinite(equity))return;
 b.equity=equity;b.peak=Math.max(Number(b.peak)||CAPITAL,equity);b.maxDD=Math.max(Number(b.maxDD)||0,b.peak-equity);
}
function openRenko(b,asset,price,time,source="AUTO"){
 if(source==="AUTO"&&!S.auto[asset])return false;
 if(b.position||!(price>0)||b.cash<=0)return false;
 const qty=Math.floor(b.cash*ALLOC/price);if(qty<1)return false;
 const cost=qty*price;if(cost>b.cash)return false;
 b.cash-=cost;b.position={entry:price,qty,opened:time,source};
 logEvent(b,asset,"BUY",price,0,time,qty,source);updateEquity(b,price);
 beep("BUY");announce("BUY",asset,price,qty,0,source);save();return true;
}
function closeRenko(b,asset,price,time,source="AUTO"){
 if(!b.position||!(price>0))return false;
 const p=b.position,pnl=(price-p.entry)*p.qty;b.cash+=p.qty*price;b.realized+=pnl;
 b.closed.unshift({entry:p.entry,exit:price,qty:p.qty,pnl,time,source:p.source||"AUTO",exitSource:source,opened:p.opened});
 b.closed=b.closed.slice(0,500);logEvent(b,asset,"SELL",price,pnl,time,p.qty,source);
 b.position=null;updateEquity(b,price);beep("SELL");announce("SELL",asset,price,p.qty,pnl,source);save();return true;
}
function executePending(b,asset,minuteBars){
 if(!b.pending)return;
 const p=b.pending;
 if(p.type==="BUY"&&!S.auto[asset]){b.pending=null;save();return}
 const next=minuteBars.find(x=>x.time>=p.afterTime);if(!next)return;
 if(p.type==="BUY"&&!b.position)openRenko(b,asset,next.open,next.time,"AUTO");
 if(p.type==="SELL"&&b.position)closeRenko(b,asset,next.open,next.time,"AUTO");
 b.pending=null;save();
}
function checkPreWarning(b,asset,price){
 if(!b.initialized||!b.renkoState||!(b.box>0)||!Number.isFinite(price))return;
 const st=b.renkoState,dir=st.dir;if(!dir||!Number.isFinite(st.anchor))return;
 const level=dir===1?st.anchor-2*b.box:st.anchor+2*b.box;
 const distance=dir===1?price-level:level-price;
 const id=dir===1?"down":"up";
 if(distance>0&&distance<=b.box){
  if(!b.preWarn[id]){
   b.preWarn[id]=true;
   speak(`${CFG[asset].name}. Внимание. Цена приближается к возможному развороту Renko ${dir===1?"вниз":"вверх"}.`);
  }
 }else if(distance>b.box||distance<0)b.preWarn[id]=false;
}

function processAsset(asset){
 const d=S.data[asset],minuteBars=closedBars(d.bars,1),f=freshness(minuteBars,1);
 const price=d.quote?.price>0?d.quote.price:null;
 const priceFresh=!!price&&!f.stale&&!d.error;
 const historyOK=S.tf===1440?d.dailyComplete:d.complete;
 const historyError=S.tf===1440?d.dailyError:d.error;
 const source=addATR(sourceBars(d,S.tf),S.atrPeriod);
 const usable=source.filter(x=>Number.isFinite(x.atr)&&x.atr>0);
 const b=book(asset);

 if(b.renkoVersion!==2){
  b.bricks=[];b.box=0;b.boxRaw=0;b.atrNow=0;
  b.initialized=false;b.cursor=0;b.renkoState=null;b.pending=null;
  b.lastReversal="—";b.preWarn={};b.calibrationEnd=0;b.renkoVersion=2;
  save();
 }

 if(price)updateEquity(b,price);
 if(!historyOK||!source.length)return;
 if(usable.length<BOX_SAMPLE)return;

 b.atrNow=last(usable).atr;

 if(!b.initialized){
  const cal=calculateFixedBox(source),ci=findCalibrationIndex(source);
  if(!(cal.box>0)||ci<0)return;

  const calibrationBar=source[ci];
  b.box=cal.box;b.boxRaw=cal.raw;
  b.bricks=[];
  b.renkoState={anchor:calibrationBar.close,dir:0};

  // До завершения калибровки кирпичи и торговые сигналы не строятся.
  // После неё обрабатываются только последующие свечи.
  for(let i=ci+1;i<source.length;i++){
   applyRenkoBar(b.renkoState,source[i],b.bricks,b.box);
  }

  b.cursor=last(source).time;
  b.initialized=true;b.pending=null;
  b.calibrationEnd=calibrationBar.time;
  b.preWarn={};updateEquity(b,price||0);save();return;
 }

 if(!(b.box>0)||!b.renkoState)return;

 // Даже при выключенном Auto открытая позиция продолжает сопровождаться.
 // Исполнение отложенных сигналов разрешено только при свежих минутных данных.
 if(priceFresh)executePending(b,asset,minuteBars);

 const start=source.findIndex(x=>x.time>b.cursor);
 if(start>=0){
  for(let i=start;i<source.length;i++){
   const bar=source[i],before=b.bricks.length;
   applyRenkoBar(b.renkoState,bar,b.bricks,b.box);

   for(let j=before;j<b.bricks.length;j++){
    const prev=b.bricks[j-1],brick=b.bricks[j];
    if(!prev||prev.dir===brick.dir)continue;

    b.lastReversal=brick.dir===1?"ВВЕРХ":"ВНИЗ";
    announceReversal(asset,brick.dir);

    if(brick.dir===1&&!b.position&&S.auto[asset]){
     b.pending={type:"BUY",afterTime:bar.time+S.tf*60000};
    }else if(brick.dir===-1&&b.position){
     b.pending={type:"SELL",afterTime:bar.time+S.tf*60000};
    }
   }

   b.cursor=bar.time;
   if(priceFresh)executePending(b,asset,minuteBars);
  }
 }

 if(priceFresh)checkPreWarning(b,asset,price);
 updateEquity(b,price||0);save();
}

function resetRenkoAll(){
 assets.forEach(a=>{
  const b=book(a);b.bricks=[];b.box=0;b.boxRaw=0;b.atrNow=0;
  b.initialized=false;b.cursor=0;b.renkoState=null;b.pending=null;
  b.lastReversal="—";b.preWarn={};b.calibrationEnd=0;b.renkoVersion=2;
 });
}

async function updateAsset(asset){
 const d=S.data[asset];
 try{
  const x=await loadCandles(asset,1,HISTORY),minuteBars=closedBars(x.bars,1),latest=last(minuteBars);
  d.bars=x.bars;d.pages=x.pages;d.board=x.board;d.complete=x.complete;
  d.error=x.complete?"":"История минутных свечей неполная.";
  if(latest){d.price=latest.close;d.quote={price:latest.close,time:latest.time+60000,board:x.board,candleTime:latest.time}}
  else{d.price=null;d.quote=null;d.error="MOEX не вернула завершённую минутную свечу."}
  d.updated=now();
 }catch(e){d.error="Минутные свечи: "+(e?.message||"ошибка загрузки");d.updated=now()}

 const retryDaily=!d.dailyComplete&&now()-(d.dailyUpdated||0)>10*60000;
 if(!d.dailyBars.length||retryDaily||now()-(d.dailyUpdated||0)>6*3600000){
  try{
   const day=await loadCandles(asset,24,DAILY_HISTORY);
   d.dailyBars=day.bars;d.dailyComplete=day.complete;d.dailyError="";d.dailyUpdated=now();
  }catch(e){
   if(!d.dailyBars.length)d.dailyComplete=false;
   d.dailyError="Дневная история: "+(e?.message||"ошибка");
   d.dailyUpdated=now();
  }
 }
}

async function refreshAsset(asset){
 if(S.loading[asset])return;S.loading[asset]=true;
 try{await updateAsset(asset);processAsset(asset)}
 catch(e){console.warn("Обновление "+asset,e)}
 finally{
  S.loading[asset]=false;updateLamps();
  if(S.asset===asset)render();
 }
}
let refreshBusy=false;
async function refreshAll(){
 if(refreshBusy)return;refreshBusy=true;$("status").textContent="Обновление пяти инструментов MOEX...";
 try{
  await Promise.all(assets.map(a=>refreshAsset(a)));
 }finally{
  refreshBusy=false;updateLamps();render();
  const bad=assets.filter(a=>S.tf===1440?!!S.data[a].dailyError:!!S.data[a].error).length;
  $("status").textContent=bad?`Обновление завершено. Ошибок инструментов: ${bad}`:"Все пять инструментов обновлены";
 }
}

function renkoDirection(asset){
 const d=S.data[asset],b=book(asset);
 const historyOK=S.tf===1440?d.dailyComplete:d.complete;
 const historyError=S.tf===1440?d.dailyError:d.error;
 if(historyError||!historyOK||!b.initialized||!b.bricks.length)return"neutral";
 if(S.tf!==1440){
  const minute=closedBars(d.bars,1),f=freshness(minute,1);
  if(f.stale)return"neutral";
 }
 const q=last(b.bricks);return q.dir===1?"up":q.dir===-1?"down":"neutral";
}
function updateLamps(){
 assets.forEach(a=>{
  const el=$("lamp-"+a);if(!el)return;const dir=renkoDirection(a);
  el.style.background=dir==="up"?"#20d69a":dir==="down"?"#ff6478":"#718096";
  el.style.boxShadow=dir==="neutral"?"0 0 4px #718096":dir==="up"?"0 0 7px #20d69a":"0 0 7px #ff6478";
  el.title=dir==="up"?"Последний кирпич Renko — вверх":dir==="down"?"Последний кирпич Renko — вниз":"Нет свежего подтверждённого кирпича Renko";
 });
}
function tvUpdate(){
 const symbol=CFG[S.asset].tv,interval={1:"1",5:"5",15:"15",30:"30",60:"60",120:"120",240:"240",1440:"D"}[S.tf];
 const names={1:"1 МИН",5:"5 МИН",15:"15 МИН",30:"30 МИН",60:"1 ЧАС",120:"2 ЧАСА",240:"4 ЧАСА",1440:"1 ДЕНЬ"};
 $("tvTf").textContent=names[S.tf]||"5 МИН";
 $("tv").src="https://www.tradingview.com/widgetembed/?frameElementId=tv_widget&symbol="+encodeURIComponent(symbol)+"&interval="+interval+"&hidesidetoolbar=1&symboledit=1&saveimage=0&toolbarbg=%2307111d&theme=dark&style=1&timezone=Europe%2FMoscow&withdateranges=1&hideideas=1";
}
function canvas(id,height){
 const c=$(id),w=c.clientWidth||320,d=window.devicePixelRatio||1;
 c.width=Math.round(w*d);c.height=Math.round(height*d);
 const x=c.getContext("2d");x.setTransform(d,0,0,d,0,0);return{ctx:x,w,h:height};
}

function drawRenko(){
 const {ctx,w,h}=canvas("renkoChart",370);ctx.clearRect(0,0,w,h);
 const d=S.data[S.asset],b=book(),all=b.bricks||[],bricks=all.slice(-60);
 const marks=(b.marks||[]).filter(x=>x.asset===S.asset).slice(-100);
 const current=d.quote?.price>0?d.quote.price:null;
 const minuteBars=closedBars(d.bars,1);
 const L=55,R=12,T=20,B=25,CW=w-L-R,CH=h-T-B;

 if(!bricks.length){
  ctx.fillStyle="#8da3b7";ctx.font="13px Arial";ctx.fillText("Ожидание формирования Renko",15,35);
  if(current){
   ctx.save();ctx.setLineDash([4,3]);ctx.strokeStyle="#ffc857";
   ctx.beginPath();ctx.moveTo(L,75);ctx.lineTo(w-R,75);ctx.stroke();
   ctx.setLineDash([]);ctx.fillStyle="#ffc857";ctx.fillText("РЫНОК "+fmt(current),L+5,68);ctx.restore();
  }
  $("chartTradeInfo").textContent="Жёлтый пунктир — текущая цена MOEX. Ожидание первых кирпичей Renko.";
  return;
 }

 const groups=[];
 bricks.forEach((q,i)=>{
  let g=last(groups);
  if(!g||g.time!==q.time)groups.push({time:q.time,first:i,last:i});
  else g.last=i;
 });

 function indexAt(t){
  if(t<=groups[0].time)return groups[0].first;
  if(t>=last(groups).time)return last(groups).last;
  let lo=0,hi=groups.length-1;
  while(hi-lo>1){
   const m=(lo+hi)>>1;
   if(groups[m].time<=t)lo=m;else hi=m;
  }
  const a=groups[lo],z=groups[hi];
  const f=(t-a.time)/Math.max(1,z.time-a.time);
  return a.last+(z.first-a.last)*f;
 }

 const start=groups[0].time,end=last(groups).time;
 const visibleMarks=marks.filter(q=>q.time>=start&&q.time<=end+S.tf*60000);
 const priceLine=minuteBars.filter(q=>q.time>=start&&q.time<=end+S.tf*60000);
 const values=[];
 bricks.forEach(q=>values.push(q.open,q.close));
 visibleMarks.forEach(q=>values.push(q.price));
 priceLine.forEach(q=>values.push(q.close));
 if(current)values.push(current);
 if(b.position)values.push(b.position.entry);

 let min=Infinity,max=-Infinity;
 values.forEach(v=>{if(Number.isFinite(v)){min=Math.min(min,v);max=Math.max(max,v)}});
 if(!Number.isFinite(min)||!Number.isFinite(max)){min=0;max=1}
 const padding=Math.max((max-min)*.15,(b.box||1)*2);
 min-=padding;max+=padding;
 const range=max-min||1,Y=v=>T+(max-v)/range*CH;
 const step=CW/bricks.length,X=i=>L+(i+.5)*step;
 const Xtime=t=>L+(Math.max(0,Math.min(bricks.length-1,indexAt(t)))+.5)*step;
 const brickW=Math.max(4,Math.min(19,step*.78));

 ctx.font="10px Arial";
 for(let i=0;i<=6;i++){
  const v=max-(max-min)*i/6,y=Y(v);
  ctx.strokeStyle="#203447";ctx.beginPath();ctx.moveTo(L,y);ctx.lineTo(w-R,y);ctx.stroke();
  ctx.fillStyle="#a5b8c9";ctx.fillText(fmt(v),2,y+3);
 }

 bricks.forEach((q,i)=>{
  const x=X(i),y1=Y(q.open),y2=Y(q.close);
  const top=Math.min(y1,y2),height=Math.max(2,Math.abs(y2-y1)),up=q.dir===1;
  ctx.fillStyle=up?"#20d69a":"#ff6478";
  ctx.fillRect(x-brickW/2,top,brickW,height);
  ctx.strokeStyle=up?"#65f0c0":"#ff9aa7";
  ctx.strokeRect(x-brickW/2,top,brickW,height);
 });

 // Непрерывная линия реальной цены по минутным свечам MOEX.
 if(priceLine.length>1){
  ctx.save();ctx.strokeStyle="#ffc857";ctx.lineWidth=1.8;
  ctx.lineJoin="round";ctx.lineCap="round";ctx.beginPath();
  priceLine.forEach((q,i)=>{
   const x=Xtime(q.time),y=Y(q.close);
   if(i===0)ctx.moveTo(x,y);else ctx.lineTo(x,y);
  });
  ctx.stroke();ctx.restore();
 }

 if(b.position){
  const y=Y(b.position.entry);
  ctx.save();ctx.setLineDash([6,4]);ctx.strokeStyle="#65a9ff";ctx.lineWidth=1.8;
  ctx.beginPath();ctx.moveTo(L,y);ctx.lineTo(w-R,y);ctx.stroke();
  ctx.setLineDash([]);ctx.fillStyle="#65a9ff";ctx.font="bold 11px Arial";
  ctx.fillText("ВХОД "+fmt(b.position.entry),L+5,y-7);ctx.restore();
 }

 visibleMarks.forEach(q=>{
  const x=Xtime(q.time),y=Y(q.price),buy=q.type==="BUY";
  ctx.fillStyle=buy?"#20d69a":"#ff6478";ctx.beginPath();
  if(buy){ctx.moveTo(x,y-13);ctx.lineTo(x-7,y-3);ctx.lineTo(x+7,y-3)}
  else{ctx.moveTo(x,y+13);ctx.lineTo(x-7,y+3);ctx.lineTo(x+7,y+3)}
  ctx.closePath();ctx.fill();ctx.font="bold 10px Arial";ctx.textAlign="center";
  ctx.fillText(buy?"BUY":"SELL",x,buy?y-17:y+25);ctx.textAlign="left";
 });

 if(current){
  const y=Y(current);
  ctx.save();ctx.setLineDash([4,3]);ctx.strokeStyle="#ff9b42";ctx.lineWidth=1.5;
  ctx.beginPath();ctx.moveTo(L,y);ctx.lineTo(w-R,y);ctx.stroke();
  ctx.setLineDash([]);ctx.fillStyle="#ffc857";ctx.font="bold 11px Arial";
  ctx.fillText("ТЕКУЩАЯ "+fmt(current),L+5,Math.max(12,y-7));ctx.restore();
 }

 ctx.fillStyle="#8da3b7";ctx.font="10px Arial";
 ctx.fillText("RENKO · "+bricks.length+" БЛОКОВ",L,h-7);
 $("chartTradeInfo").textContent="60 последних кирпичей Renko · жёлтая сплошная линия — история реальной цены MOEX · оранжевый пунктир — текущая цена · синий пунктир — вход · BUY/SELL — виртуальные сделки · меток: "+visibleMarks.length;
}

function drawEquity(){
 const {ctx,w,h}=canvas("equity",145);ctx.clearRect(0,0,w,h);
 const b=book(),a=b.closed.slice().reverse(),v=[0];let sum=0;
 a.forEach(x=>{sum+=x.pnl;v.push(sum)});
 const min=Math.min(0,...v),max=Math.max(0,...v),r=max-min||1,y=n=>10+(max-n)/r*(h-20),zero=y(0);
 ctx.strokeStyle="#43586c";ctx.setLineDash([4,4]);ctx.beginPath();ctx.moveTo(0,zero);ctx.lineTo(w,zero);ctx.stroke();ctx.setLineDash([]);
 if(a.length){
  ctx.strokeStyle="#20d69a";ctx.lineWidth=2;ctx.beginPath();
  v.forEach((n,i)=>{const x=8+i*(w-16)/Math.max(1,v.length-1);i?ctx.lineTo(x,y(n)):ctx.moveTo(x,y(n))});ctx.stroke();
  $("equityInfo").textContent="Закрытых сделок: "+a.length+" · Реализованный итог: "+money(sum);
 }else{
  ctx.fillStyle="#8da3b7";ctx.font="11px Arial";ctx.fillText("Нет закрытых сделок · нулевая линия",10,Math.max(15,zero-8));
  $("equityInfo").textContent="Результат появится после закрытия первой сделки.";
 }
}

function simulate(source){
 const cal=calculateFixedBox(source),fixedBox=cal.box;
 const ci=findCalibrationIndex(source);
 if(!(fixedBox>0)||ci<0||source.length<=ci+2){
  return{count:0,pnl:0,win:0,dd:0,box:fixedBox,raw:cal.raw,atr:cal.atr,open:0,equity:CAPITAL,pos:null,pending:null,calibration:0,tested:0};
 }
 let cash=CAPITAL,pos=null,pending=null;
 const closed=[],bricks=[];
 let peak=CAPITAL,maxDD=0;
 const calibrationBar=source[ci],state={anchor:calibrationBar.close,dir:0};

 for(let i=ci+1;i<source.length;i++){
  const bar=source[i];

  if(pending==="BUY"&&!pos){
   const qty=Math.floor(cash*ALLOC/bar.open);
   if(qty>0){cash-=qty*bar.open;pos={entry:bar.open,qty,opened:bar.time}}
  }else if(pending==="SELL"&&pos){
   const pnl=(bar.open-pos.entry)*pos.qty;
   cash+=pos.qty*bar.open;closed.push(pnl);pos=null;
  }

  pending=null;
  const before=bricks.length;
  applyRenkoBar(state,bar,bricks,fixedBox);

  for(let j=before;j<bricks.length;j++){
   const prev=bricks[j-1],q=bricks[j];
   if(prev&&prev.dir!==q.dir){
    if(q.dir===1&&!pos)pending="BUY";
    if(q.dir===-1&&pos)pending="SELL";
   }
  }

  const equity=cash+(pos?pos.qty*bar.close:0);
  peak=Math.max(peak,equity);maxDD=Math.max(maxDD,peak-equity);
 }

 const lastPrice=last(source).close;
 const open=pos?(lastPrice-pos.entry)*pos.qty:0;
 const equity=cash+(pos?pos.qty*lastPrice:0);
 peak=Math.max(peak,equity);maxDD=Math.max(maxDD,peak-equity);
 const wins=closed.filter(x=>x>0).length;

 return{
  count:closed.length,pnl:closed.reduce((a,v)=>a+v,0),
  win:closed.length?wins/closed.length*100:0,dd:maxDD,
  box:fixedBox,raw:cal.raw,atr:cal.atr,open,equity,
  pos:pos?{entry:pos.entry,qty:pos.qty}:null,
  pending:pending||null,calibration:calibrationBar.time,
  tested:source.length-ci-1
 };
}

function runBacktest(){
 const d=S.data[S.asset];
 const source=addATR(sourceBars(d,S.tf),S.atrPeriod).filter(x=>Number.isFinite(x.atr)&&x.atr>0);
 if(source.length<BOX_SAMPLE+3){
  $("backtestStatus").textContent="Недостаточно истории. Нужно не менее 20 значений ATR после прогрева и ещё несколько свечей.";return;
 }
 $("backtestStatus").textContent="Выполняется исторический тест...";
 const r=simulate(source),body=$("backtest");body.textContent="";
 const tr=document.createElement("tr");
 ["ATR "+S.atrPeriod+" FIXED",r.count,money(r.pnl),r.count?r.win.toFixed(1)+"%":"—",money(r.dd)].forEach(v=>{
  const td=document.createElement("td");td.textContent=v;tr.append(td);
 });
 body.append(tr);$("btOpen").textContent=money(r.open);$("btEquity").textContent=money(r.equity);
 $("btPosition").textContent=r.pos?r.pos.qty+" шт. · вход "+fmt(r.pos.entry)+" ₽":"Нет";
 $("btPending").textContent=r.pending||"Нет";
 $("backtestStatus").textContent=`Тест: ${S.asset} · ${$("signalTF").textContent} · ATR ${S.atrPeriod} · ATR калибровки ${fmt(r.atr)} ₽ · коробка до округления ${fmt(r.raw)} ₽ · фактическая коробка ${fmt(r.box)} ₽ · калибровка по 20 значениям · дата начала теста ${r.calibration?new Date(r.calibration).toLocaleString("ru-RU"):"—"} · свечей после калибровки ${r.tested} · без комиссий и налогов.`;
}

function manualMarketCheck(){
 const d=S.data[S.asset],minute=closedBars(d.bars,1),f=freshness(minute,1);
 const historyOK=S.tf===1440?d.dailyComplete:d.complete,price=d.quote?.price||0;
 if(d.error)return{ok:false,reason:d.error};
 if(!historyOK)return{ok:false,reason:S.tf===1440?(d.dailyError||"Дневная история MOEX ещё не загружена полностью."):"История MOEX ещё не загружена полностью."};
 if(f.stale)return{ok:false,reason:"Последняя минутная свеча устарела. Обнови данные."};
 if(!(price>0))return{ok:false,reason:"Нет подтверждённой цены MOEX."};
 return{ok:true,price,time:d.quote.time};
}
function manualBuy(){
 const b=book(),m=manualMarketCheck();
 if(!m.ok){alert("Покупка не выполнена.\n"+m.reason);return}
 if(b.position){alert("Покупка невозможна: виртуальная позиция уже открыта.");return}
 if(b.cash<=0){alert("Нет свободных виртуальных средств.");return}
 const qty=Math.floor(b.cash*ALLOC/m.price),cost=qty*m.price;
 if(qty<1){alert("Недостаточно виртуальных средств для покупки.");return}
 const msg=`Подтверди РУЧНУЮ ВИРТУАЛЬНУЮ ПОКУПКУ\n\nИнструмент: ${S.asset}\nЦена: ${fmt(m.price)} ₽\nКоличество: ${qty} шт.\nСумма: ${money(cost)}\nОстаток: ${money(b.cash-cost)}\n\nРеальная заявка не отправляется.`;
 if(!confirm(msg))return;
 const check=manualMarketCheck();
 if(!check.ok){alert("Покупка отменена: "+check.reason);return}
 if(b.position){alert("Позиция уже открыта.");return}
 if(openRenko(b,S.asset,check.price,check.time,"MANUAL")){
  $("manualStatus").textContent="Ручная виртуальная покупка выполнена по "+fmt(check.price)+" ₽.";render();
 }else alert("Не удалось выполнить виртуальную покупку.");
}
function manualSell(){
 const b=book(),m=manualMarketCheck();
 if(!m.ok){alert("Продажа не выполнена.\n"+m.reason);return}
 if(!b.position){alert("Нет открытой виртуальной позиции для продажи.");return}
 const p=b.position,pnl=(m.price-p.entry)*p.qty;
 const msg=`Подтверди РУЧНУЮ ВИРТУАЛЬНУЮ ПРОДАЖУ\n\nИнструмент: ${S.asset}\nЦена: ${fmt(m.price)} ₽\nКоличество: ${p.qty} шт.\nПредварительный результат: ${money(pnl)}\n\nРеальная заявка не отправляется.`;
 if(!confirm(msg))return;
 const check=manualMarketCheck();
 if(!check.ok){alert("Продажа отменена: "+check.reason);return}
 if(!b.position){alert("Открытая позиция уже отсутствует.");return}
 if(closeRenko(b,S.asset,check.price,check.time,"MANUAL")){
  $("manualStatus").textContent="Ручная виртуальная продажа выполнена по "+fmt(check.price)+" ₽.";render();
 }else alert("Не удалось закрыть виртуальную позицию.");
}

function renderJournal(b){
 const body=$("journal");body.textContent="";
 if(!b.events.length){
  const tr=document.createElement("tr"),td=document.createElement("td");
  td.colSpan=5;td.textContent="Сделок пока нет";tr.append(td);body.append(tr);return;
 }
 b.events.slice(0,60).forEach(e=>{
  const tr=document.createElement("tr"),operation=e.type+" · "+(e.source==="MANUAL"?"РУЧНАЯ":"АВТО");
  [new Date(e.time).toLocaleString("ru-RU"),operation,fmt(e.price),e.qty||"—",e.type==="SELL"?money(e.pnl):"—"].forEach(v=>{
   const td=document.createElement("td");td.textContent=v;tr.append(td);
  });body.append(tr);
 });
}

function render(){
 const d=S.data[S.asset],minute=closedBars(d.bars,1),f=freshness(minute,1);
 const source=addATR(sourceBars(d,S.tf),S.atrPeriod).filter(x=>Number.isFinite(x.atr)&&x.atr>0);
 const b=book(),price=d.quote?.price>0?d.quote.price:null;
 const historyOK=S.tf===1440?d.dailyComplete:d.complete;
 const historyError=S.tf===1440?d.dailyError:d.error;
 const stale=!!d.error||!historyOK||f.stale||!price;
 const renkoStale=!historyOK||!!historyError;
 if(price)updateEquity(b,price);

 $("accountAsset").textContent=S.asset;$("journalAsset").textContent=S.asset;
 $("price").textContent=price?fmt(price):"—";
 $("tradeTime").textContent=d.quote?new Date(d.quote.time).toLocaleString("ru-RU"):"Время не подтверждено";
 $("candleTime").textContent=f.bar?age(f.age):"—";
 $("fresh").textContent=d.error?"ОШИБКА":!historyOK?"ИСТОРИЯ НЕПОЛНАЯ":!price?"НЕТ ЦЕНЫ":f.stale?"ДАННЫЕ УСТАРЕЛИ":"КОТИРОВКА ДОСТУПНА";
 $("fresh").className="badge "+(stale?"red":"green");
 $("priceSource").textContent=d.quote?"Цена — close последней завершённой минутной свечи MOEX. Возраст: "+age(f.age)+".":"Нет подтверждённой минутной цены MOEX.";
 $("sourceBadge").textContent=stale?"НЕТ ДОПУСКА":"ДАННЫЕ ДОСТУПНЫ";
 $("sourceBadge").className="badge "+(stale?"red":"green");
 $("board").textContent=d.board;$("count").textContent=d.bars.length;$("pages").textContent=d.pages||0;
 $("lastBar").textContent=f.bar?new Date(f.bar.time).toLocaleString("ru-RU"):"—";
 $("freshness").textContent=f.bar?age(f.age):"—";

 const allowed=!stale&&source.length>=BOX_SAMPLE&&S.auto[S.asset];
 $("allowed").textContent=allowed?"ДА":"НЕТ";$("allowed").className=allowed?"green":"red";

 $("diagnostic").textContent=historyError||
  (d.error?"Минутные котировки недоступны. Новые виртуальные сделки заблокированы. Renko дневного интервала может продолжать обновляться по дневной истории.":!historyOK?"История MOEX неполная.":!price?"Нет подтверждённой цены минутной свечи.":f.stale?"Последняя завершённая минутная свеча старше 20 минут. Новые сделки заблокированы.":"Данные MOEX доступны. Все пять активов обрабатываются независимо, пока страница активна.");
 $("status").textContent=historyError?"Ошибка источника":!historyOK?"История неполная":stale?"Ожидание свежих минутных данных":"Данные получены";

 const tfName=({1:"1 мин",5:"5 мин",15:"15 мин",30:"30 мин",60:"1 час",120:"2 часа",240:"4 часа",1440:"1 день"})[S.tf];
 $("signalTF").textContent=tfName;
 const br=last(b.bricks),box=b.box||calculateFixedBox(source).box,raw=b.boxRaw||calculateFixedBox(source).raw;
 $("boxSize").textContent=box?fmt(box)+" ₽":"—";
 $("boxRaw").textContent=raw?fmt(raw)+" ₽":"—";
 $("atrActual").textContent=b.atrNow?fmt(b.atrNow)+" ₽":"—";
 $("brickCount").textContent=b.bricks.length;
 $("brickTrend").textContent=br?(br.dir===1?"ВВЕРХ":"ВНИЗ"):"—";
 $("brickLast").textContent=br?(br.dir===1?"ЗЕЛЁНЫЙ":"КРАСНЫЙ"):"—";
 $("reversal").textContent=b.lastReversal;
 $("renkoState").textContent=renkoStale?"НЕТ ИСТОРИИ":b.initialized?"FIXED ATR "+S.atrPeriod:"КАЛИБРОВКА";
 $("renkoInfo").textContent=`Фиксированный блок ${fmt(box)} ₽ · до округления ${fmt(raw)} ₽ · текущий ATR ${fmt(b.atrNow)} ₽ · период ${S.atrPeriod} · ${S.asset} · ${tfName} · кирпичи по Close · ATR по OHLC.`;
 $("signalTitle").textContent="СИГНАЛ RENKO FIXED ATR "+S.atrPeriod;
 $("headerSub").textContent="MULTI-ASSET AUTO RENKO ATR "+S.atrPeriod+" · MOEX · VIRTUAL ONLY";
 $("atrValue").textContent=S.atrPeriod;$("atrSelect").value=String(S.atrPeriod);

 if(renkoStale){
  $("renkoSignal").textContent="WAIT · НЕТ ИСТОРИИ";
  $("renkoSignal").className="signal yellow";
  $("renkoReason").textContent=historyError||"История для выбранного таймфрейма ещё не загружена.";
 }else if(!br){
  $("renkoSignal").textContent="WAIT · ОЖИДАНИЕ";
  $("renkoSignal").className="signal yellow";
  $("renkoReason").textContent="Renko ещё не сформировал направление.";
 }else{
  $("renkoSignal").textContent=br.dir===1?"ТРЕНД ВВЕРХ · ОЖИДАНИЕ СИГНАЛА":"ТРЕНД ВНИЗ · ОЖИДАНИЕ СИГНАЛА";
  $("renkoSignal").className="signal "+(br.dir===1?"green":"red");
  $("renkoReason").textContent="Последний кирпич "+(br.dir===1?"зелёный.":"красный.")+
   " Это направление тренда, а не команда немедленной сделки. Вход/выход выполняется после подтверждённого разворота и на следующей доступной минутной свече."+
   (stale?" Минутная котировка устарела: исполнение новых виртуальных сделок заблокировано.":"");
 }

 const market=price||0,pl=b.position?(market-b.position.entry)*b.position.qty:0;
 const equity=b.cash+(b.position?b.position.qty*market:0);
 $("capital").textContent=money(equity);$("cash").textContent=money(b.cash);
 $("profit").textContent=money(b.realized);$("trades").textContent=b.closed.length;
 const wins=b.closed.filter(x=>x.pnl>0).length;
 $("winrate").textContent=b.closed.length?(wins/b.closed.length*100).toFixed(1)+"%":"—";
 $("floating").textContent=money(pl);$("drawdown").textContent=money(b.maxDD);
 const ev=b.events[0];
 $("lastDeal").textContent=ev?ev.type+" · "+(ev.source==="MANUAL"?"РУЧНАЯ":"АВТО")+" · "+fmt(ev.price)+" ₽":"—";

 assets.forEach(a=>{const e=$("auto-"+a);if(e)e.checked=!!S.auto[a]});
 $("position").textContent=b.position
  ?`ВИРТУАЛЬНАЯ ПОКУПКА · ${b.position.qty} шт. · Вход ${fmt(b.position.entry)} ₽ · Текущая цена ${fmt(market)} ₽ · Открытый результат ${money(pl)} · Вход: ${b.position.source==="MANUAL"?"РУЧНОЙ":"АВТОМАТИЧЕСКИЙ"}`
  :"Открытой позиции нет.";

 const manualOK=!stale&&price>0;
 $("manualBuy").disabled=!manualOK||!!b.position||b.cash<=0;
 $("manualSell").disabled=!manualOK||!b.position;
 $("manualStatus").textContent=!manualOK?"Ручные действия заблокированы: нужна свежая подтверждённая цена MOEX.":b.position?"Позиция открыта. Можно закрыть её кнопкой «Продать виртуально».":"Можно открыть виртуальную позицию независимо от автоматического режима и направления Renko.";

 drawRenko();drawEquity();renderJournal(b);updateLamps();
}

function selectAsset(a){
 if(!CFG[a])return;S.asset=a;
 document.querySelectorAll("[data-asset]").forEach(x=>x.classList.toggle("active",x.dataset.asset===a));
 tvUpdate();save();render();refreshAsset(a);
}
function changeTF(tf){
 tf=Number(tf);if(!TFS.includes(tf)||tf===S.tf)return;
 S.tf=tf;resetRenkoAll();
 document.querySelectorAll("[data-tf]").forEach(x=>x.classList.toggle("active",Number(x.dataset.tf)===S.tf));
 tvUpdate();save();render();refreshAll();
}
function changeATR(value){
 const p=Number(value);if(!ATR_OPTIONS.includes(p)||p===S.atrPeriod)return;
 S.atrPeriod=p;resetRenkoAll();save();render();refreshAll();
}
function toggleAuto(asset){
 S.auto[asset]=$("auto-"+asset).checked;save();render();
}
function resetCurrent(){
 if(!confirm("Сбросить виртуальный счёт "+S.asset+" целиком? Будут удалены позиция, журнал и статистика только этого инструмента."))return;
 S.books[S.asset]=emptyBook();save();render();
}
function restoreControls(){
 $("voiceOn").checked=S.voice;$("volume").value=S.volume;
 assets.forEach(a=>{const e=$("auto-"+a);if(e)e.checked=!!S.auto[a]});
 $("atrSelect").value=String(S.atrPeriod);
 document.querySelectorAll("[data-tf]").forEach(x=>x.classList.toggle("active",Number(x.dataset.tf)===S.tf));
 document.querySelectorAll("[data-asset]").forEach(x=>x.classList.toggle("active",x.dataset.asset===S.asset));
}
restoreControls();tvUpdate();render();refreshAll();
setInterval(refreshAll,UPDATE);
window.addEventListener("resize",()=>{drawRenko();drawEquity()});
document.addEventListener("visibilitychange",()=>{
 if(!document.hidden){refreshAll();runSpeechQueue()}
});
</script>
</body>
</html>
