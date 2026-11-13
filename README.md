# unidad2frances
Vocabulario unidad 2 francés

<!DOCTYPE html>
<html lang="es"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Repaso de francés · Unité 2 · Alonso Arroyo Onieva</title>
<style>
:root{--bg:#fbf8f1;--card:#fff;--tx:#1d2540;--mu:#6a7090;--ac:#2c4a9a;--acs:#e6ecff;--ok:#2e8b57;--ko:#d0453b;--bd:#e3dccb;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media(prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#161a2b;--card:#222842;--tx:#eef0fa;--mu:#9aa1c4;--ac:#8fb0ff;--acs:#2d3558;--ok:#5cc98a;--ko:#ff7d72;--bd:#343b5e;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#161a2b;--card:#222842;--tx:#eef0fa;--mu:#9aa1c4;--ac:#8fb0ff;--acs:#2d3558;--ok:#5cc98a;--ko:#ff7d72;--bd:#343b5e;color-scheme:dark}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--tx);font:16px/1.4 system-ui,-apple-system,"Segoe UI",Roboto,sans-serif}
main{max-width:640px;margin:0 auto;padding:16px}
h1{font-size:1.4rem;margin:0 0 2px}
.sub{color:var(--mu);margin:0 0 14px;font-size:.9rem}
.row{display:flex;flex-wrap:wrap;gap:8px;margin:10px 0}
button{font:inherit;color:var(--tx);background:var(--card);border:1.5px solid var(--bd);border-radius:12px;padding:9px 14px;cursor:pointer}
button.on{background:var(--ac);border-color:var(--ac);color:#fff}
@media(prefers-color-scheme:dark){:root:not([data-theme="light"]) button.on{color:#10142a}}
button.big{flex:1;padding:14px;font-weight:600}
.ok{border-color:var(--ok);color:var(--ok)}.ko{border-color:var(--ko);color:var(--ko)}
.tabs button{flex:1}
.card{background:var(--card);border:2px solid var(--bd);border-radius:20px;min-height:200px;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:24px;cursor:pointer;user-select:none}
.card .big{font-size:1.7rem;font-weight:700;overflow-wrap:anywhere}
.card .hint{color:var(--mu);font-size:.85rem;margin-top:10px}
.cat{font-size:.75rem;text-transform:uppercase;letter-spacing:.06em;color:var(--mu);margin-bottom:10px}
.bar{height:8px;background:var(--acs);border-radius:8px;overflow:hidden;margin:6px 0}
.bar i{display:block;height:100%;background:var(--ac);transition:width .2s}
.opt{display:block;width:100%;text-align:left;margin:8px 0;padding:13px 14px}
input[type=text]{width:100%;font:inherit;padding:13px;border-radius:12px;border:2px solid var(--bd);background:var(--card);color:var(--tx)}
.msg{margin:10px 0;font-weight:600}
.small{font-size:.85rem;color:var(--mu)}
.speak{border-radius:999px;padding:9px 18px;margin-top:12px;font-weight:600;color:var(--ac);border-color:var(--ac);background:var(--acs)}
</style></head>
<body><main>
<h1>🇫🇷 C’est la rentrée !</h1>
<p class="sub">Unité 2 · 1º ESO · Repaso de todo el léxico de la lámina</p>
<p class="sub"><strong>Alonso Arroyo Onieva</strong></p>
<div class="row tabs" id="tabs"></div>
<div class="row" id="cats"></div>
<div class="row" id="opts"></div>
<div id="view"></div>
</main>
<script>
const D=[];const add=(c,fr,es)=>D.push({c,fr,es});
[["Très bien.","Muy bien."],["Bien.","Bien."],["Assez bien.","Bastante bien."],["Mal.","Mal."],["Très mal.","Muy mal."]].forEach(x=>add("Sensations",...x));
[["Allemand / allemande","Alemán / alemana"],["Américain / américaine","Estadounidense"],["Anglais / anglaise","Inglés / inglesa"],["Canadien / canadienne","Canadiense"],["Chinois / chinoise","Chino / china"],["Espagnol / espagnole","Español / española"],["Français / française","Francés / francesa"],["Italien / italienne","Italiano / italiana"],["Marocain / marocaine","Marroquí"],["Roumain / roumaine","Rumano / rumana"],["Russe (invariable)","Ruso / rusa (no cambia)"],["Suédois / suédoise","Sueco / sueca"]].forEach(x=>add("Nationalités",...x));
const U="zéro un deux trois quatre cinq six sept huit neuf dix onze douze treize quatorze quinze seize dix-sept dix-huit dix-neuf".split(" ");
const T={2:"vingt",3:"trente",4:"quarante",5:"cinquante"};
for(let n=0;n<60;n++){let w;if(n<20)w=U[n];else{const t=T[Math.floor(n/10)],u=n%10;w=u==0?t:u==1?t+" et un":t+"-"+U[u]}add("Nombres",w,String(n))}
[["Je suis Matthieu.","Soy Matthieu."],["Moi, c’est Alex.","Yo soy Alex."],["Tu t’appelles comment ?","¿Cómo te llamas?"],["Quel est ton nom ?","¿Cuál es tu nombre?"],["Je m’appelle Camille Morel.","Me llamo Camille Morel."],["Enchanté !","¡Encantado!"],
["Comment ça va ? / Ça va ?","¿Cómo estás? / ¿Qué tal?"],["Ça va bien, merci. Et toi ?","Bien, gracias. ¿Y tú?"],["Assez bien.","Bastante bien."],["Comment vas-tu ?","¿Cómo estás?"],["Pas mal, merci.","No está mal, gracias."],["Bof… plus ou moins.","Pues… más o menos."],
["Quelle est ta nationalité ?","¿Cuál es tu nacionalidad?"],["Je suis allemand et toi ?","Soy alemán, ¿y tú?"],["Moi, je suis anglais.","Yo soy inglés."],["Ils sont français ?","¿Son franceses?"],["Non, ils sont canadiens.","No, son canadienses."],["Et vous ?","¿Y vosotros / usted?"],["Nous sommes suédois.","Somos suecos."],["Est-ce que tu es russe ?","¿Eres ruso?"],["Non, je suis roumain.","No, soy rumano."],
["Tu as quel âge ?","¿Cuántos años tienes?"],["Et Juliette ?","¿Y Juliette?"],["Moi, j’ai treize ans et Juliette a seize ans.","Yo tengo trece años y Juliette tiene dieciséis."],["Quel âge a David ?","¿Cuántos años tiene David?"],["Il a dix ans.","Tiene diez años."],["Vous avez quel âge les enfants ?","¿Cuántos años tenéis, niños?"],["Nous avons dix ans.","Tenemos diez años."],["Tu as douze ans Noëlle ?","¿Tienes doce años, Noëlle?"],["Non, j’ai onze ans.","No, tengo once años."]].forEach(x=>add("Communication",...x));

const CATS=["Todo","Sensations","Nationalités","Nombres","Communication"];
const S={tab:"cards",cat:"Todo",dir:"fr",shuf:true,known:new Set(),deck:[],i:0,flip:false,q:null};
const $=id=>document.getElementById(id);
const norm=s=>s.toLowerCase().normalize("NFD").replace(/[\u0300-\u036f]/g,"").replace(/[’'\-]/g," ").replace(/[^a-z0-9 ]/g," ").replace(/\s+/g," ").trim();
const shuffle=a=>{a=a.slice();for(let i=a.length-1;i>0;i--){const j=Math.floor(Math.random()*(i+1));[a[i],a[j]]=[a[j],a[i]]}return a};
const pool=()=>D.filter(d=>S.cat=="Todo"||d.c==S.cat);
const speak=t=>{try{if(!window.speechSynthesis)throw 0;speechSynthesis.cancel();const u=new SpeechSynthesisUtterance(t);u.lang="fr-FR";u.rate=.85;const v=speechSynthesis.getVoices().find(x=>x.lang&&x.lang.toLowerCase().startsWith("fr"));if(v)u.voice=v;speechSynthesis.speak(u)}catch(e){alert("Este navegador no puede reproducir la voz.")}};
const spk=t=>`<button class="speak" data-say="${t.replace(/"/g,"&quot;")}" title="Escuchar">🔊 Escuchar</button>`;

function head(){
  $("tabs").innerHTML=[["cards","🃏 Tarjetas"],["quiz","✅ Test"],["write","✍️ Escribir"]].map(([k,l])=>`<button class="${S.tab==k?"on":""}" data-tab="${k}">${l}</button>`).join("");
  $("cats").innerHTML=CATS.map(c=>`<button class="${S.cat==c?"on":""}" data-cat="${c}">${c}</button>`).join("");
  $("opts").innerHTML=S.tab=="write"?"":`<button data-dir="fr">${S.dir=="fr"?"Francés → Español":"Español → Francés"} ⇄</button>`+(S.tab=="cards"?`<button data-shuf="1">Orden: ${S.shuf?"aleatorio":"lámina"}</button>`:"");
}
function start(){
  head();S.i=0;S.flip=false;S.q=null;
  if(S.tab=="cards"){S.deck=S.shuf?shuffle(pool()):pool();S.known=new Set();}
  else{S.deck=shuffle(pool()).slice(0,10);S.q={score:0,done:false,ans:null}}
  render();
}
const front=d=>S.dir=="fr"?d.fr:d.es, back=d=>S.dir=="fr"?d.es:d.fr;

function render(){
  const v=$("view");
  if(S.i>=S.deck.length){
    if(S.tab=="cards"){
      const rep=S.deck.filter(d=>!S.known.has(d));
      v.innerHTML=`<div class="card" style="cursor:default"><div class="big">🎉 ¡Ronda terminada!</div><p>Sabías ${S.known.size} de ${S.deck.length}.</p></div><div class="row">${rep.length?`<button class="big" data-again="1">Repasar las ${rep.length} que fallé</button>`:""}<button class="big" data-restart="1">Empezar de nuevo</button></div>`;
    }else{
      const n=S.deck.length,s=S.q.score;
      v.innerHTML=`<div class="card" style="cursor:default"><div class="big">${s>=n*.9?"🏆":s>=n*.6?"👍":"💪"} ${s} / ${n}</div><p>${s>=n*.9?"¡Excelente!":s>=n*.6?"¡Bien! Sigue practicando.":"Repasa las tarjetas y vuelve a intentarlo."}</p></div><div class="row"><button class="big" data-restart="1">Otra ronda</button></div>`;
    }
    return;
  }
  const d=S.deck[S.i],pct=Math.round(S.i/S.deck.length*100);
  const prog=`<div class="small">${S.i+1} / ${S.deck.length}${S.tab=="cards"?` · ✓ ${S.known.size}`:` · puntos: ${S.q.score}`}</div><div class="bar"><i style="width:${pct}%"></i></div>`;
  if(S.tab=="cards"){
    v.innerHTML=prog+`<div class="card" data-flip="1"><div class="cat">${d.c}</div><div class="big">${S.flip?back(d):front(d)}</div>${S.flip||S.dir=="fr"?spk(d.fr):""}<div class="hint">${S.flip?"":"Toca para ver la respuesta"}</div></div>`+(S.flip?`<div class="row"><button class="big ko" data-know="0">↻ Repasar</button><button class="big ok" data-know="1">✓ Me la sé</button></div>`:"");
  }else if(S.tab=="quiz"){
    if(!S.q.opts){const others=shuffle(D.filter(x=>x.c==d.c&&x!==d)).slice(0,3);S.q.opts=shuffle([d,...others])}
    v.innerHTML=prog+`<div class="card" style="cursor:default"><div class="cat">${d.c}</div><div class="big">${front(d)}</div>${S.dir=="fr"||S.q.ans!=null?spk(d.fr):""}</div>`+
      S.q.opts.map((o,k)=>{let cl="";if(S.q.ans!=null){if(o===d)cl="ok";else if(k==S.q.ans)cl="ko"}return `<button class="opt ${cl}" data-opt="${k}" ${S.q.ans!=null?"disabled":""}>${back(o)}</button>`}).join("")+
      (S.q.ans!=null?`<div class="row"><button class="big on" data-next="1">Siguiente →</button></div>`:"");
  }else{
    const hint=d.c=="Nombres"?"Escribe el número en francés":"Escribe la frase/palabra en francés";
    v.innerHTML=prog+`<div class="card" style="cursor:default"><div class="cat">${d.c} · ${hint}</div><div class="big">${d.es}</div></div><div style="margin-top:12px"><input type="text" id="inp" autocomplete="off" autocapitalize="off" spellcheck="false" placeholder="en français…" ${S.q.ans!=null?"disabled":""} value="${S.q.val||""}"></div>`+
      (S.q.ans==null?`<div class="row"><button class="big on" data-check="1">Comprobar</button></div><p class="small">Los acentos y mayúsculas no importan; sí las palabras.</p>`:
      `<div class="msg" style="color:var(--${S.q.ans?"ok":"ko"})">${S.q.ans?"✓ ¡Correcto!":"✗ Respuesta: "+d.fr}</div>${spk(d.fr)}<div class="row"><button class="big on" data-next="1">Siguiente →</button></div>`);
    const i=$("inp");if(i&&S.q.ans==null)i.focus();
  }
}
function check(){
  const d=S.deck[S.i],val=$("inp").value;S.q.val=val;
  const ok=[d.fr,...d.fr.split("/")].map(x=>norm(x.replace(/\(.*?\)/g,""))).includes(norm(val));
  S.q.ans=ok;if(ok)S.q.score++;render();
}
document.addEventListener("click",e=>{
  const b=e.target.closest("[data-tab],[data-cat],[data-dir],[data-shuf],[data-flip],[data-know],[data-opt],[data-next],[data-check],[data-again],[data-restart],[data-say]");if(!b)return;
  const a=b.dataset;
  if(a.say!==undefined){e.stopPropagation();speak(a.say);return}
  if(a.tab){S.tab=a.tab;start()}
  else if(a.cat){S.cat=a.cat;start()}
  else if(a.dir){S.dir=S.dir=="fr"?"es":"fr";start()}
  else if(a.shuf){S.shuf=!S.shuf;start()}
  else if(a.flip!==undefined){S.flip=!S.flip;render()}
  else if(a.know!==undefined){if(a.know=="1")S.known.add(S.deck[S.i]);S.i++;S.flip=false;render()}
  else if(a.opt!==undefined){const k=+a.opt;S.q.ans=k;if(S.q.opts[k]===S.deck[S.i])S.q.score++;render()}
  else if(a.next!==undefined){S.i++;S.q.ans=null;S.q.opts=null;S.q.val="";render()}
  else if(a.check!==undefined)check();
  else if(a.again!==undefined){S.deck=S.deck.filter(d=>!S.known.has(d));S.known=new Set();S.i=0;S.flip=false;render()}
  else if(a.restart!==undefined)start();
});
document.addEventListener("keydown",e=>{if(e.key=="Enter"&&S.tab=="write"&&S.i<S.deck.length){S.q.ans==null?check():(S.i++,S.q.ans=null,S.q.val="",render())}});
start();
</script></body></html>
