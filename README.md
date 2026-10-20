<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Dimensionamento das especialistas · MKT.B2C Eureca</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
:root{
  --roxo:#261B4B; --menta:#5EF0B0;
  --bg:#F5F4F8; --panel:#FFFFFF; --fg:#241A45; --muted:#5E577A; --line:#E3E0EC; --soft:#EFEDF5;
  --ok:#1E7B5A; --ok-bg:#DDF4E9; --warn:#8A5300; --warn-bg:#FCEBD2; --bad:#B42342; --bad-bg:#FBE1E6;
  --h0:#EAF7F1; --h1:#C9EEDC; --h2:#FCEBD2; --h3:#F8CBA0; --h4:#F3A3B2; --h5:#D94F6B;
  box-sizing:border-box; padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
}
@media (prefers-color-scheme: dark){
  :root:not([data-theme="light"]){
    --bg:#16102C; --panel:#211843; --fg:#EEEBF7; --muted:#B4AECB; --line:#382D63; --soft:#2A2052;
    --ok:#7FE3B6; --ok-bg:#163C31; --warn:#F5C27A; --warn-bg:#3D2C12; --bad:#FF9AAE; --bad-bg:#43182A;
    --h0:#1B3A30; --h1:#1F5A45; --h2:#5A4419; --h3:#7A4A1E; --h4:#7A2A40; --h5:#A3243F;
  }
}
:root[data-theme="dark"]{
  --bg:#16102C; --panel:#211843; --fg:#EEEBF7; --muted:#B4AECB; --line:#382D63; --soft:#2A2052;
  --ok:#7FE3B6; --ok-bg:#163C31; --warn:#F5C27A; --warn-bg:#3D2C12; --bad:#FF9AAE; --bad-bg:#43182A;
  --h0:#1B3A30; --h1:#1F5A45; --h2:#5A4419; --h3:#7A4A1E; --h4:#7A2A40; --h5:#A3243F;
}
*,*::before,*::after{box-sizing:border-box}
html{height:100%}
body{margin:0; background:var(--bg); color:var(--fg); font-family:Poppins,"Segoe UI",Helvetica,Arial,sans-serif; font-size:15px; line-height:1.5}
header{background:var(--roxo); color:#fff}
.hin{max-width:1100px; margin:0 auto; padding:28px 22px 22px}
.marca{display:flex; gap:12px; align-items:baseline; margin-bottom:16px}
.wm{font-weight:700; font-size:24px; color:var(--menta); letter-spacing:-.5px}
.tg{font-size:12px; color:#CFC8E8}
h1{font-size:clamp(22px,3.4vw,32px); margin:0 0 6px; line-height:1.15}
header p{margin:0; color:#E4E0F2; max-width:70ch}
nav{display:flex; gap:6px; margin-top:20px; flex-wrap:wrap}
nav button{font:inherit; font-size:14px; font-weight:600; border:0; border-radius:999px; padding:8px 16px; cursor:pointer; background:rgba(255,255,255,.12); color:#fff}
nav button[aria-selected="true"]{background:var(--menta); color:var(--roxo)}
nav button:focus-visible, button:focus-visible, select:focus-visible, input:focus-visible{outline:3px solid var(--menta); outline-offset:2px}
main{max-width:1100px; margin:0 auto; padding:22px 22px 60px}
section[hidden]{display:none}
h2{font-size:20px; margin:4px 0 6px}
.lead{color:var(--muted); margin:0 0 16px; max-width:75ch}
.panel{background:var(--panel); border-radius:16px; padding:18px; margin-bottom:18px}
.wrap{overflow-x:auto}
table{border-collapse:collapse; width:100%}
th,td{padding:8px 10px; text-align:left; font-size:14px; border-bottom:1px solid var(--line); white-space:nowrap}
th{font-size:12.5px; color:var(--muted); font-weight:600}
.heat td.c{text-align:center; font-weight:600; font-size:13px; border-radius:6px; border:2px solid var(--panel)}
.heat th.c{text-align:center}
.heat tr.esp td:first-child{font-weight:600; cursor:pointer}
.heat tr.esp td:first-child:hover{text-decoration:underline}
.legend{display:flex; gap:10px; flex-wrap:wrap; font-size:12.5px; color:var(--muted); margin-top:12px}
.legend span{display:inline-flex; align-items:center; gap:6px}
.legend i{width:14px; height:14px; border-radius:4px; display:inline-block}
.pill{display:inline-block; font-size:12.5px; font-weight:600; padding:2px 10px; border-radius:999px}
.p-ok{background:var(--ok-bg); color:var(--ok)} .p-warn{background:var(--warn-bg); color:var(--warn)} .p-bad{background:var(--bad-bg); color:var(--bad)}
.fase{font-size:12.5px; padding:2px 8px; border-radius:6px; background:var(--soft)}
.form{display:grid; grid-template-columns:repeat(auto-fit,minmax(200px,1fr)); gap:12px 16px}
label{display:flex; flex-direction:column; gap:4px; font-size:13px; font-weight:600; color:var(--muted)}
select,input{font:inherit; font-size:14px; color:var(--fg); background:var(--bg); border:1px solid var(--line); border-radius:10px; padding:8px 10px; font-weight:400}
.res{display:grid; grid-template-columns:repeat(auto-fit,minmax(170px,1fr)); gap:12px; margin:6px 0 16px}
.kpi{background:var(--soft); border-radius:12px; padding:12px 14px}
.kpi b{display:block; font-size:22px}
.kpi span{font-size:13px; color:var(--muted)}
.note{font-size:13px; color:var(--muted); margin-top:10px}
.rg td input{width:80px}
footer{max-width:1100px; margin:0 auto; padding:0 22px 30px; font-size:12px; color:var(--muted)}
</style>
</head>
<body>
<header><div class="hin">
  <div class="marca"><span class="wm">eureca</span><span class="tg">MKT.B2C</span></div>
  <h1>Dimensionamento das especialistas de comunicação</h1>
  <p>Diagnóstico da carga atual e simulador para o Comercial avaliar quem tem espaço para um programa novo.</p>
  <nav role="tablist">
    <button role="tab" aria-selected="true" data-tab="diag">Diagnóstico</button>
    <button role="tab" aria-selected="false" data-tab="sim">Simular programa</button>
    <button role="tab" aria-selected="false" data-tab="prem">Premissas</button>
  </nav>
</div></header>

<main>
<section id="diag">
  <h2>Ocupação por semana</h2>
  <p class="lead">Retrato da carteira de outubro de 2026, com a carga das próximas semanas conforme a fase de cada projeto. 100% é a jornada da especialista, já descontada a reserva para imprevistos. Clique no nome para ver os projetos.</p>
  <div class="panel"><div class="wrap"><table class="heat" id="heat"></table></div>
    <div class="legend"><span><i style="background:var(--h0)"></i>até 70%</span><span><i style="background:var(--h1)"></i>70 a 100%</span><span><i style="background:var(--h2)"></i>100 a 120%</span><span><i style="background:var(--h3)"></i>120 a 150%</span><span><i style="background:var(--h4)"></i>150 a 200%</span><span><i style="background:var(--h5)"></i>acima de 200%</span></div>
  </div>
  <div class="panel" id="detalhe"></div>
</section>

<section id="sim" hidden>
  <h2>Simular um programa novo</h2>
  <p class="lead">Preencha o programa como ele foi vendido. A calculadora mostra quantas horas ele exige e quantos programas desse perfil uma especialista comporta ao mesmo tempo.</p>
  <div class="panel"><div class="form" id="form"></div></div>
  <div class="panel">
    <div class="res" id="kpis"></div>
    <div class="wrap"><table id="fit"></table></div>
    <h2 style="margin-top:24px">Quem está mais apta a assumir</h2>
    <p class="lead">Com base na carteira de outubro de 2026: a ocupação de cada especialista nas semanas em que o programa acontece, sem ele e com ele. A lista vem ordenada de quem fica menos sobrecarregada para quem fica mais.</p>
    <div class="wrap"><table id="apto"></table></div>
    <p class="note">Cabe: o pico com o programa fica em até 100%. No limite: entre 100% e 120%. Sobrecarga: acima de 120%. Como a carteira é um retrato de outubro, programas que começam muitos meses depois tendem a parecer mais leves, porque ela não inclui os projetos que ainda vão entrar.</p>
    <p class="note">* A duração das fases varia muito de programa para programa. A conta usa as fases tiradas dos cronogramas de 2026: 6 semanas de planejamento, 4 de atração (3 no aprendiz e no operador) e o restante como convocação, com as 2 últimas semanas de encerramento. A duração padrão é de 18 semanas no estágio, 16 no aprendiz e no operador e 22 no trainee. Trainee e aprendiz se baseiam em um cronograma cada.</p>
  </div>
</section>

<section id="prem" hidden>
  <h2>Premissas</h2>
  <p class="lead">Valores usados na conta, calibrados a partir da carteira de outubro de 2026. Se algum valor precisar mudar, altere aqui: o diagnóstico e o simulador se atualizam na hora.</p>
  <div class="panel"><div class="wrap"><table class="rg" id="regua"></table></div>
    <p class="note">O multiplicador vale só para o projeto base. Os adicionais (shooting, hotsite, eventos etc.) entram com as horas do inventário. Teto da soma dos acréscimos: <input type="number" id="teto" min="0" max="200" step="5" value="60" aria-label="Teto da soma dos acréscimos em %">%</p>
  </div>
  <div class="panel"><div class="wrap"><table id="base"></table></div></div>
</section>
</main>
<footer>Fonte: planilha de entregas das especialistas (versão 4), inventário validado e carteira de outubro de 2026. Diárias de shooting, evento e deslocamento consideradas como 8 horas de trabalho. Estudo a ser renovado anualmente.</footer>

<script>
const HOJE=new Date(2026,9,19); // segunda-feira, 19/10/2026
const SEMANAS=16;
const REGUA={
  tipo:{nome:'Tipo de projeto',niv:{'Estágio':0,'Trainee':10,'Operador':10,'Aprendiz':20}},
  crit:{nome:'Criticidade e localidade das vagas',niv:{'Baixo':0,'Médio':10,'Alto':25}},
  mix:{nome:'Tipo e mix de programas',niv:{'Baixo':0,'Médio':15,'Alto':30}},
  vol:{nome:'Volume de vagas',niv:{'Baixo':0,'Médio':10,'Alto':25}},
  perfil:{nome:'Perfil do cliente',niv:{'Baixo':0,'Médio':10,'Alto':20}},
  marca:{nome:'Marca empregadora (Baixo = muito conhecida)',niv:{'Baixo':0,'Médio':5,'Alto':15}},
  novo:{nome:'Cliente novo ou recompra (Baixo = recompra)',niv:{'Baixo':0,'Médio':5,'Alto':15}}
};
const BASE={plan:31.9, atrSem:10, convSem:7.1/5, enc:8.4, trans:5.6, capMes:136,
  shooting:17.2, hotsite:5.2, live:5.8, videocast:13.8, evMap:17.7, evExec:22.9, infMap:2.8, infExec:1.5, emb:1.8,
  apoio:{'Sem apoio':0,'Temporário':20,'Estagiário':20,'Analista':40}};
const ESP={'Bárbara':'Temporário','Brenda':'Sem apoio','Clara':'Sem apoio','Mabi':'Estagiário','Emily':'Sem apoio'};
// e, cliente, tipo, início, semanas, semanas de planejamento, shooting, hotsite, live/videocast, eventos, influenciador, embaixadores, crit, mix, vol, perfil, marca, novo
const RAW=`Clara|Solar Coca-Cola|Trainee|2026-07-24|20|4|S|S|Videocast|Só|Só|N|Médio|Baixo|Baixo|Alto|Alto|Baixo
Clara|Equatorial|Estágio|2026-09-21|21|8|S|S|Live|Não|Não|N|Médio|Baixo|Médio|Alto|Médio|Alto
Clara|PagBank|Estágio|2026-06-30|15|4|S|S|Videocast|Só|Completo|N|Baixo|Baixo|Médio|Alto|Alto|Alto
Clara|Motiva|Estágio|2026-08-30|60|1|N|N|Não|Não|Não|N|Alto|Baixo|Baixo|Alto|Baixo|Alto
Bárbara|PagBank|Trainee|2026-10-01|26|4|S|S|Videocast|Completo|Completo|N|Baixo|Baixo|Baixo|Alto|Alto|Baixo
Bárbara|Unilever|Estágio|2026-06-25|20|4|S|S|Live|Completo|Completo|S|Alto|Baixo|Médio|Alto|Alto|Alto
Bárbara|Thomson Reuters|Estágio|2026-07-24|13|4|N|N|Live|Não|Não|N|Baixo|Baixo|Médio|Baixo|Baixo|Baixo
Bárbara|Grupo Fleury|Estágio|2026-10-05|15|4|S|S|Videocast|Só|Não|S|Baixo|Baixo|Médio|Baixo|Médio|Baixo
Bárbara|Equinor|Estágio|2026-05-13|24|4|S|N|Videocast|Não|Não|N|Baixo|Baixo|Médio|Médio|Médio|Baixo
Bárbara|L'Oréal|Trainee|2026-05-20|23|4|S|S|Videocast|Só|Só|S|Baixo|Baixo|Médio|Alto|Alto|Alto
Bárbara|Stellantis|Estágio|2026-05-21|25|4|N|S|Live|Não|Não|N|Médio|Baixo|Alto|Médio|Médio|Baixo
Bárbara|Subsea7|Estágio|2026-06-03|15|4|N|N|Live|Não|Não|N|Alto|Baixo|Baixo|Médio|Baixo|Baixo
Mabi|MRS|Estágio|2026-05-06|13|4|N|N|Não|Só|Completo|N|Alto|Alto|Alto|Médio|Baixo|Baixo
Mabi|Mondelez|Estágio|2026-06-24|13|4|S|S|Videocast|Completo|Não|N|Médio|Baixo|Baixo|Baixo|Médio|Baixo
Mabi|Natura|Estágio|2026-06-10|10|4|S|N|Videocast|Não|Não|N|Médio|Baixo|Alto|Médio|Alto|Médio
Mabi|MRS|Aprendiz|2026-09-10|10|4|N|N|Não|Não|Completo|N|Médio|Alto|Médio|Médio|Baixo|Alto
Mabi|MRS|Operador|2026-08-07|13|4|N|N|Não|Não|Não|N|Baixo|Alto|Médio|Baixo|Alto|Alto
Mabi|Ardagh|Estágio|2026-08-25|15|4|N|S|Não|Não|Não|N|Alto|Baixo|Baixo|Baixo|Baixo|Baixo
Mabi|Sodexo|Estágio|2026-06-23|15|4|S|N|Live|Não|Não|N|Médio|Baixo|Baixo|Médio|Médio|Alto
Emily|Aché|Aprendiz|2026-06-03|19|4|S|S|Não|Não|Completo|N|Médio|Alto|Alto|Alto|Médio|Alto
Emily|Aché|Estágio|2026-08-25|13|4|S|S|Live|Completo|Não|N|Médio|Alto|Baixo|Médio|Médio|Médio
Emily|Sabesp|Aprendiz|2026-07-15|17|4|N|N|Não|Não|Não|N|Alto|Alto|Alto|Alto|Médio|Médio
Emily|Sabesp|Estágio|2026-08-21|12|4|N|N|Não|Não|Não|N|Alto|Alto|Médio|Alto|Médio|Médio
Emily|Sabesp|Trainee|2026-09-09|14|4|N|N|Não|Completo|Não|N|Baixo|Alto|Baixo|Alto|Médio|Médio
Emily|SLC Agrícola|Estágio|2026-07-09|20|4|S|S|Live|Completo|Completo|S|Alto|Baixo|Alto|Médio|Médio|Médio
Emily|Bayer|Estágio|2026-10-14|15|4|N|N|Não|Não|Não|N|Baixo|Baixo|Baixo|Baixo|Baixo|Baixo
Brenda|Serasa Experian|Estágio|2026-08-28|26|4|S|N|Videocast|Não|Não|N|Baixo|Baixo|Baixo|Médio|Médio|Baixo
Brenda|Nestlé|Trainee|2026-06-03|30|4|N|N|Não|Não|Não|N|Baixo|Baixo|Baixo|Médio|Alto|Baixo
Brenda|Bradesco Seguros|Estágio|2026-05-20|25|4|S|S|Videocast|Não|Não|N|Médio|Baixo|Alto|Alto|Alto|Baixo
Brenda|Vivo|Aprendiz|2025-05-22|50|4|N|S|Não|Não|Não|N|Alto|Médio|Alto|Alto|Alto|Baixo`;
const PROJ=RAW.split('\n').map(l=>{const f=l.split('|');return{continua:f[1]==='Motiva',e:f[0],c:f[1],tipo:f[2],ini:new Date(f[3]+'T00:00:00'),dur:+f[4],plan:(f[1]==='MRS'&&f[2]==='Operador')?2:(+f[5]===4?6:+f[5]),atr:(f[2]==='Aprendiz'||f[2]==='Operador')?3:4,sh:f[6]==='S',ho:f[7]==='S',lv:f[8],ev:f[9],inf:f[10],emb:f[11]==='S',crit:f[12],mix:f[13],vol:f[14],perfil:f[15],marca:f[16],novo:f[17]}});
let TETO=60;

function mult(p){let s=0;for(const k in REGUA){const v=REGUA[k].niv[p[k]];s+=(v||0)}return 1+Math.min(s,TETO)/100}
function atrFim(p){return p.continua?9999:p.plan+p.atr}
function fase(p,k){ // k = semanas desde o início
  if(k<0)return null; if(k<p.plan)return'Planejamento'; const a=atrFim(p);
  if(k<a)return'Atração'; if(k<p.dur-2)return'Convocação'; if(k<p.dur)return'Encerramento';
  if(k<p.dur+8)return'Convocação (prolongada)'; return null}
function horasSemana(p,k){
  const f=fase(p,k); if(!f)return 0; const m=mult(p); const atrW=Math.max(1,atrFim(p)-p.plan);
  if(f==='Planejamento'){const ad=(p.sh?BASE.shooting:0)+(p.ho?BASE.hotsite:0)+(p.ev!=='Não'?BASE.evMap:0)+(p.inf!=='Não'?BASE.infMap:0);return BASE.plan/p.plan*m+ad/p.plan}
  if(f==='Atração'){const ad=(p.lv==='Live'?BASE.live:p.lv==='Videocast'?BASE.videocast:0)+(p.ev==='Completo'?BASE.evExec:0)+(p.inf==='Completo'?BASE.infExec:0)+(p.emb?BASE.emb:0);return BASE.atrSem*m+ad/atrW}
  if(f==='Encerramento')return BASE.enc/2*m;
  return BASE.convSem*m}
function semanaIdx(p,w){const d=new Date(HOJE);d.setDate(d.getDate()+7*w);return Math.floor((d-p.ini)/(7*864e5))}
function capSem(e){return BASE.capMes/4}
function cargaSem(e,w,extra){let h=BASE.trans;for(const p of PROJ)if(p.e===e)h+=horasSemana(p,semanaIdx(p,w));if(extra)h+=extra[w]||0;return h}
function ocup(e,w,extra){return cargaSem(e,w,extra)/capSem(e)*100}
function cor(o){return o<=70?'var(--h0)':o<=100?'var(--h1)':o<=120?'var(--h2)':o<=150?'var(--h3)':o<=200?'var(--h4)':'var(--h5)'}
function txt(o){return o>200?'#fff':'inherit'}
function dd(d){return d.toLocaleDateString('pt-BR',{day:'2-digit',month:'2-digit'})}
function semData(w){const d=new Date(HOJE);d.setDate(d.getDate()+7*w);return d}
function pct(o){return Math.round(o)+'%'}

function renderHeat(){
  const W=12; let h='<thead><tr><th>Especialista</th>';
  for(let w=0;w<W;w++)h+=`<th class="c">${dd(semData(w))}</th>`; h+='</tr></thead><tbody>';
  for(const e in ESP){h+=`<tr class="esp"><td tabindex="0" data-e="${e}">${e}</td>`;
    for(let w=0;w<W;w++){const o=ocup(e,w);h+=`<td class="c" style="background:${cor(o)};color:${txt(o)}">${pct(o)}</td>`}h+='</tr>'}
  document.getElementById('heat').innerHTML=h+'</tbody>';
  document.querySelectorAll('#heat td[data-e]').forEach(td=>{td.onclick=()=>renderDet(td.dataset.e);td.onkeydown=ev=>{if(ev.key==='Enter')renderDet(td.dataset.e)}});
}
function renderDet(e){
  const ps=PROJ.filter(p=>p.e===e);
  let h=`<h2>${e}</h2><p class="lead">Ocupação nesta semana: <b>${pct(ocup(e,0))}</b>. Capacidade de ${Math.round(capSem(e)*4)} horas por mês, com ${String(BASE.trans).replace('.',',')} horas por semana de rotinas fora de projeto.</p><div class="wrap"><table><thead><tr><th>Cliente</th><th>Programa</th><th>Fase nesta semana</th><th>Multiplicador</th><th>Horas nesta semana</th></tr></thead><tbody>`;
  ps.map(p=>({p,f:fase(p,semanaIdx(p,0)),hs:horasSemana(p,semanaIdx(p,0))})).sort((a,b)=>b.hs-a.hs).forEach(({p,f,hs})=>{
    h+=`<tr><td>${p.c}</td><td>${p.tipo}</td><td><span class="fase">${f||'Encerrado'}</span></td><td>${mult(p).toFixed(2).replace('.',',')}x</td><td>${hs.toFixed(1).replace('.',',')} h</td></tr>`});
  document.getElementById('detalhe').innerHTML=h+'</tbody></table></div>';
}

const CAMPOS=[['tipo','Tipo de programa',['Estágio','Trainee','Aprendiz','Operador']],['crit','Criticidade e localidade das vagas',['Baixo','Médio','Alto']],['mix','Tipo e mix de programas',['Baixo','Médio','Alto']],['vol','Volume de vagas',['Baixo','Médio','Alto']],['perfil','Perfil do cliente',['Baixo','Médio','Alto']],['marca','Marca empregadora',['Baixo','Médio','Alto']],['novo','Cliente novo ou recompra',['Baixo','Médio','Alto']],['sh','Shooting',['Não','Sim']],['ho','Hotsite',['Não','Sim']],['lv','Live ou videocast',['Não','Live','Videocast']],['ev','Eventos em universidades',['Não','Só','Completo']],['inf','Influenciador',['Não','Só','Completo']],['emb','Embaixadores',['Não','Sim']]];
const ROT={Só:'Só mapeamento',Baixo:'Baixo',Médio:'Médio',Alto:'Alto'};
const DESC={marca:{Baixo:'Muito conhecida',Médio:'Média',Alto:'Pouco conhecida'},novo:{Baixo:'Recompra',Médio:'Outro tipo ou há muito tempo',Alto:'Cliente novo'},perfil:{Baixo:'Aprova rápido',Médio:'Revisões pontuais',Alto:'Vários aprovadores'}};
const DUR={'Estágio':18,'Trainee':22,'Aprendiz':16,'Operador':16};
function renderForm(){
  let h='';CAMPOS.forEach(([k,n,ops])=>{h+=`<label>${n}<select id="f_${k}">${ops.map(o=>`<option value="${o}">${(DESC[k]&&DESC[k][o])||ROT[o]||o}</option>`).join('')}</select></label>`});
  const d=new Date(HOJE);d.setDate(d.getDate()+14);
  h+=`<label>Início do projeto<input type="date" id="f_ini" value="${d.toISOString().slice(0,10)}"></label><label>Duração (semanas)<input type="number" id="f_dur" min="8" max="52" value="18"></label>`;
  document.getElementById('form').innerHTML=h;document.querySelectorAll('#form select,#form input').forEach(x=>x.oninput=renderSim);document.getElementById('f_tipo').addEventListener('input',e=>{document.getElementById('f_dur').value=DUR[e.target.value]||18;renderSim()});
}
function lerForm(){const g=k=>document.getElementById('f_'+k).value;return{e:'novo',c:'Novo programa',tipo:g('tipo'),crit:g('crit'),mix:g('mix'),vol:g('vol'),perfil:g('perfil'),marca:g('marca'),novo:g('novo'),sh:g('sh')==='Sim',ho:g('ho')==='Sim',lv:g('lv'),ev:g('ev'),inf:g('inf'),emb:g('emb')==='Sim',ini:new Date(g('ini')+'T00:00:00'),dur:Math.max(8,+g('dur')||18),plan:6,atr:(g('tipo')==='Aprendiz'||g('tipo')==='Operador')?3:4}}
function renderSim(){
  const p=lerForm(); let tot=0; const meses=[];
  for(let k=0;k<p.dur;k++){const h=horasSemana(p,k);tot+=h;const m=Math.floor(k/4);meses[m]=(meses[m]||0)+h}
  const disp=BASE.capMes-BASE.trans*4; const media=tot/p.dur*4; const pico=Math.max(...meses);
  const nMed=disp/media, nPico=disp/pico;
  const f=n=>n.toFixed(1).replace('.',',');
  document.getElementById('kpis').innerHTML=`<div class="kpi"><b>${mult(p).toFixed(2).replace('.',',')}x</b><span>multiplicador da régua</span></div><div class="kpi"><b>${Math.round(tot)} h</b><span>horas totais do programa</span></div><div class="kpi"><b>${Math.round(media)} h/mês</b><span>média por mês</span></div><div class="kpi"><b>${Math.round(pico)} h</b><span>mês mais pesado</span></div>`;
  let h='<thead><tr><th>Cenário</th><th>Programas desse perfil por especialista</th><th>Como ler</th></tr></thead><tbody>';
  h+=`<tr><td><b>Programas em fases diferentes</b></td><td><b>${f(nMed)}</b></td><td style="white-space:normal">Quando os programas começam em datas espaçadas, a especialista comporta em média esse número ao mesmo tempo.</td></tr>`;
  h+=`<tr><td><b>Programas começando juntos</b></td><td><b>${f(nPico)}</b></td><td style="white-space:normal">Se os programas começarem na mesma época, o limite é dado pelo mês mais pesado (planejamento ou atração).</td></tr>`;
  h+='</tbody>';
  h+=`<tbody><tr><td colspan="3" style="white-space:normal;color:var(--muted)">Horas por mês do programa: ${meses.map((v,i)=>`mês ${i+1}: ${Math.round(v)} h`).join(' · ')}. Capacidade disponível para projetos: ${Math.round(disp)} h por mês por especialista.</td></tr></tbody>`;
  document.getElementById('fit').innerHTML=h;
  const extra=[],jan=[];
  for(let w=0;w<60;w++){const k=semanaIdx(p,w);const hh=(k>=0&&k<p.dur)?horasSemana(p,k):0;extra[w]=hh;if(hh>0)jan.push(w)}
  const res=Object.keys(ESP).map(e=>{let mx=0,wm=0,s=0,a=0;jan.forEach(w=>{const o=ocup(e,w,extra);s+=o;a+=ocup(e,w);if(o>mx){mx=o;wm=w}});const n=Math.max(1,jan.length);return{e,atual:a/n,med:s/n,mx,wm}}).sort((x,y)=>x.med-y.med);
  let t='<thead><tr><th>#</th><th>Especialista</th><th>Ocupação no período, sem o programa</th><th>Com o programa</th><th>Pico com o programa</th><th>Semana do pico</th><th>Resultado</th></tr></thead><tbody>';
  if(!jan.length){t+='<tr><td colspan="7">O programa começa antes desta semana. Ajuste a data de início.</td></tr>'}
  res.forEach((r,i)=>{if(!jan.length)return;const st=r.mx<=100?'<span class="pill p-ok">Cabe</span>':r.mx<=120?'<span class="pill p-warn">No limite</span>':'<span class="pill p-bad">Sobrecarga</span>';t+=`<tr><td>${i+1}</td><td><b>${r.e}</b></td><td>${pct(r.atual)}</td><td>${pct(r.med)}</td><td>${pct(r.mx)}</td><td>${dd(semData(r.wm))}</td><td>${st}</td></tr>`});
  document.getElementById('apto').innerHTML=t+'</tbody>';
}
function renderPrem(){
  let h='<thead><tr><th>Variável</th><th>Nível</th><th>Acréscimo (%)</th></tr></thead><tbody>';
  for(const k in REGUA)for(const n in REGUA[k].niv)h+=`<tr><td>${REGUA[k].nome}</td><td>${(DESC[k]&&DESC[k][n])||n}</td><td><input type="number" step="5" min="0" max="200" value="${REGUA[k].niv[n]}" data-k="${k}" data-n="${n}" aria-label="${REGUA[k].nome}, ${n}"></td></tr>`;
  document.getElementById('regua').innerHTML=h+'</tbody>';
  document.querySelectorAll('#regua input').forEach(i=>i.oninput=()=>{REGUA[i.dataset.k].niv[i.dataset.n]=+i.value||0;tudo()});
  document.getElementById('teto').oninput=e=>{TETO=+e.target.value||0;tudo()};
  const linhas=[['Projeto padrão: planejamento',BASE.plan+' h no total da fase'],['Projeto padrão: atração',BASE.atrSem+' h por semana'],['Projeto padrão: convocação',(BASE.convSem).toFixed(1).replace('.',',')+' h por semana'],['Projeto padrão: encerramento',BASE.enc.toString().replace('.',',')+' h no total da fase'],['Shooting (no planejamento)',BASE.shooting.toString().replace('.',',')+' h'],['Hotsite (no planejamento)',BASE.hotsite.toString().replace('.',',')+' h'],['Live / videocast (na atração)',BASE.live.toString().replace('.',',')+' h / '+BASE.videocast.toString().replace('.',',')+' h'],['Eventos: mapeamento / execução',BASE.evMap.toString().replace('.',',')+' h / '+BASE.evExec.toString().replace('.',',')+' h'],['Influenciador: mapeamento / execução',BASE.infMap.toString().replace('.',',')+' h / '+BASE.infExec.toString().replace('.',',')+' h'],['Rotinas fora de projeto',BASE.trans.toString().replace('.',',')+' h por semana'],['Capacidade por especialista','136 h por mês (160 h menos 15% de imprevistos)'],['Fases de um programa *','Tiradas dos cronogramas de 2026 (Mondelez, Sodexo, Ardagh, Equatorial, MRS, Alcoa e Solar Coca-Cola): 6 semanas de planejamento e 4 de atração (3 no aprendiz e no operador). O restante da duração é convocação, com as 2 últimas semanas de encerramento. Duração padrão: estágio 18, aprendiz e operador 16, trainee 22 semanas. Trainee e aprendiz se baseiam em um cronograma cada. Exceções na carteira: Equatorial com 8 semanas de planejamento, MRS Operador com 2 (cliente recorrente) e Motiva como atração contínua (hunting). Projetos além da duração prevista contam como convocação prolongada por até 8 semanas'],['Apoio (temporário, estagiário)','Ainda não considerado. Será medido depois'],['Validade do estudo','Base de outubro de 2026. Renovar uma vez por ano']];
  document.getElementById('base').innerHTML='<thead><tr><th>Premissa</th><th>Valor</th></tr></thead><tbody>'+linhas.map(l=>`<tr><td>${l[0]}</td><td style="white-space:normal">${l[1]}</td></tr>`).join('')+'</tbody>';
}
function tudo(){renderHeat();renderDet(document.querySelector('#detalhe h2')?.textContent||'Bárbara');renderSim()}
document.querySelectorAll('nav button').forEach(b=>b.onclick=()=>{document.querySelectorAll('nav button').forEach(x=>x.setAttribute('aria-selected',x===b));document.querySelectorAll('main section').forEach(s=>s.hidden=s.id!==b.dataset.tab)});
renderForm();renderPrem();tudo();
</script>
</body>
</html>
