<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Hobbies, Personality & Present Perfect — B2</title>
<style>
:root{--p:#7650b5;--d:#4e337e;--l:#eee5ff;--bg:#f8f5ff;--ink:#30263f;--line:#e5daf5}
*{box-sizing:border-box}
html{scroll-behavior:smooth;scroll-padding-top:82px}
body{margin:0;background:var(--bg);color:var(--ink);font:16px/1.55 system-ui,Arial}
header{background:linear-gradient(120deg,#50317e,#956bc8);color:white;text-align:center;padding:42px 16px}
h1{font-size:clamp(2rem,5vw,3rem);line-height:1.12;margin:8px}
header p{max-width:750px;margin:auto;color:#f2eaff}
nav{position:sticky;top:0;background:#fffF;backdrop-filter:blur(10px);display:flex;gap:6px;overflow-x:auto;overflow-y:hidden;padding:10px;z-index:1000;border-bottom:1px solid var(--line);isolation:isolate}
nav a{display:inline-flex;align-items:center;white-space:nowrap;color:var(--d);font-weight:700;text-decoration:none;padding:8px 12px;border-radius:18px;cursor:pointer;touch-action:manipulation;flex:0 0 auto}
nav a:hover,nav a:focus-visible{background:var(--l);outline:2px solid #aa8bd4;outline-offset:2px}
main{max-width:1100px;margin:24px auto;padding:0 15px 50px}
section{background:white;border:1px solid var(--line);border-radius:20px;padding:23px;margin:20px 0;box-shadow:0 10px 28px #55318b12;scroll-margin-top:90px}
h2,h3{color:var(--d)}
h2{margin:0 0 8px}
.muted,.small{color:#766b86}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:10px}
.card{height:105px;perspective:800px;cursor:pointer}
.inner{height:100%;position:relative;transform-style:preserve-3d;transition:.4s}
.card.flip .inner{transform:rotateY(180deg)}
.face{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;text-align:center;padding:12px;border:1px solid var(--line);border-radius:13px;background:linear-gradient(140deg,#fff,#f3ebff);backface-visibility:hidden;font-weight:700;color:var(--d)}
.back{transform:rotateY(180deg);background:#f0e7ff}
.toolbar{display:flex;gap:8px;align-items:center;flex-wrap:wrap;margin:12px 0}
button{border:0;border-radius:10px;background:var(--p);color:white;font-weight:700;padding:9px 14px;cursor:pointer}
button.alt{background:var(--l);color:var(--d)}
select,input,textarea{font:inherit;border:1px solid #d8c9ec;border-radius:8px;padding:8px;max-width:100%}
.task{border:1px solid var(--line);border-radius:14px;padding:15px;margin:14px 0;background:#fdfbff}
.q{padding:8px;margin:7px 0;background:#f7f2ff;border-radius:9px}
.q select,.q input[type=text]{margin:5px 0}
.feedback{font-weight:700;margin:8px 0}
.good{color:#24764d}
.bad{color:#b33b58}
.bank{display:flex;flex-wrap:wrap;gap:7px;margin:12px 0}
.chip{padding:6px 10px;background:var(--l);color:var(--d);border:1px solid #d9c8ef;border-radius:20px;cursor:grab;user-select:none}
.chip.sel{outline:3px solid #aa8bd4}
.zones{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:10px}
.zone{min-height:115px;padding:10px;border:2px dashed #cbb8e6;border-radius:13px;background:#fcfaff}
.zone h4{margin:0 0 8px;color:var(--d)}
.zone.over{background:#eee4ff}
.key{background:#f5efff;padding:10px;border-radius:10px;margin-top:10px}
.key summary{cursor:pointer;color:var(--d);font-weight:bold}
.rule{background:#f4edff;border-left:5px solid var(--p);padding:13px;border-radius:9px;margin:10px 0}
table{border-collapse:collapse;width:100%;margin:10px 0}
td,th{border:1px solid var(--line);padding:9px;text-align:left}
th{background:#eee5ff;color:var(--d)}
textarea{width:100%;min-height:85px}
.progress{position:sticky;bottom:8px;background:#4e337eee;color:white;padding:10px 14px;border-radius:12px;display:flex;justify-content:space-between}
footer{text-align:center;color:#766b86;padding:20px}
@media(max-width:600px){section{padding:16px}}
</style>
</head>
<body>

<header>
<div>B1–B2 VOCABULARY & GRAMMAR</div>
<h1>Hobbies, Personality<br>& Present Perfect</h1>
<p>Interactive vocabulary revision, sorting activities, personality idioms and grammar practice.</p>
</header>

<nav id="topNav">
<a href="#cards">Flashcards</a>
<a href="#dpg">Do/Play/Go</a>
<a href="#hobbies">Hobbies</a>
<a href="#personality">Personality</a>
<a href="#idioms">Idioms</a>
<a href="#guide">Grammar guide</a>
<a href="#grammar">Grammar tasks</a>
<a href="#speaking">Speaking</a>
</nav>

<main>
<section id="cards">
<h2>1. Vocabulary flashcards</h2>
<p class="muted">Click a card to see the Russian translation. Filter the vocabulary by group.</p>
<div class="toolbar">
<label>Group
<select id="filter">
<option value="all">All words</option>
<option value="hobbies">Hobbies</option>
<option value="personality">Personality</option>
<option value="idioms">Idioms</option>
<option value="extra">Additional B2</option>
</select>
</label>
<button class="alt" onclick="shuffle()">Shuffle</button>
<span id="count" class="small"></span>
</div>
<div class="grid" id="cardsGrid"></div>
</section>

<section id="dpg">
<h2>2. Sort: DO, PLAY or GO?</h2>
<p class="muted">Drag words into a category. On a phone, tap a word and then tap the target category.</p>
<div class="bank" id="dpgBank"></div>
<div class="zones">
<div class="zone" data-group="dpg" data-cat="do"><h4>🔵 DO</h4><div class="placed"></div></div>
<div class="zone" data-group="dpg" data-cat="play"><h4>🟣 PLAY</h4><div class="placed"></div></div>
<div class="zone" data-group="dpg" data-cat="go"><h4>🟢 GO</h4><div class="placed"></div></div>
</div>
<div class="toolbar">
<button onclick="checkSort('dpg')">Check</button>
<button class="alt" onclick="resetSort('dpg')">Reset</button>
</div>
<div id="dpgResult" class="feedback"></div>
<details class="key">
<summary>Teacher's answer key</summary>
<b>DO:</b> ballet, ballroom dancing, gymnastics, martial arts, drama, yoga, aerobics, athletics, weight training, pottery, DIY projects, gardening, embroidery, origami, meditation, Pilates, tai chi, parkour, kickboxing, judo.<br>
<b>PLAY:</b> basketball, board games, cards, chess, ice hockey, table tennis, volleyball, a musical instrument, video games, badminton, rugby, poker, darts, the piano, the guitar, the drums, squash, snooker.<br>
<b>GO:</b> camping, cycling, horse riding, ice skating, rollerblading, running, shopping, skateboarding, bowling, fishing, hiking, sailing, skiing, snowboarding, scuba diving, rock climbing, mountain biking, kayaking, windsurfing, birdwatching, trekking, bouldering.
</details>
</section>

<section id="hobbies">
<h2>3. Introverts’ and Extraverts’ hobbies</h2>
<p class="muted">Sort the hobbies into INTROVERTS, EXTRAVERTS or BOTH. There can be more than one reasonable classification: be ready to explain your choices.</p>
<div class="bank" id="hobbyBank"></div>
<div class="zones">
<div class="zone" data-group="hobby" data-cat="intro"><h4>🩵 INTROVERTS</h4><div class="placed"></div></div>
<div class="zone" data-group="hobby" data-cat="extro"><h4>🧡 EXTRAVERTS</h4><div class="placed"></div></div>
<div class="zone" data-group="hobby" data-cat="both"><h4>💜 BOTH</h4><div class="placed"></div></div>
</div>
<div class="toolbar">
<button onclick="checkSort('hobby')">Check placement</button>
<button class="alt" onclick="resetSort('hobby')">Reset</button>
</div>
<div id="hobbyResult" class="feedback"></div>
<details class="key">
<summary>Suggested classification</summary>
<b>Introverts:</b> read books/magazines, draw, bake cakes, collect figures/cards/stamps, make clothes, journaling, creative writing, calligraphy, knitting, solving puzzles, birdwatching, learning languages, chess, crosswords, model building, genealogy, stargazing, composing music, digital illustration, philosophy, embroidery, pottery, scrapbooking.<br>
<b>Extraverts:</b> hang out with friends, text friends, ballroom dancing, team sports, drama, karaoke, volunteering, music festivals, networking events, debate clubs, amateur theatre, social gatherings, escape rooms, salsa dancing, comedy shows, group travel, book clubs, charity events, live concerts, hosting dinner parties.<br>
<b>Both:</b> photography, cycling, hiking, video blogging, cooking, travelling, gardening, learning languages, playing musical instruments, gaming, dancing, volunteering, cinema, workshops, shopping, camping, film-making, podcasting.
</details>
</section>

<section id="personality">
<h2>4. Personality adjectives</h2>
<div class="task">
<h3>4.1 Sort the adjectives</h3>
<p>Sort by the usual meaning. Some traits depend on context.</p>
<div class="bank" id="persBank"></div>
<div class="zones">
<div class="zone" data-group="pers" data-cat="positive"><h4>🌟 POSITIVE</h4><div class="placed"></div></div>
<div class="zone" data-group="pers" data-cat="negative"><h4>⚠️ NEGATIVE</h4><div class="placed"></div></div>
<div class="zone" data-group="pers" data-cat="depends"><h4>🔄 DEPENDS</h4><div class="placed"></div></div>
</div>
<button onclick="checkSort('pers')">Check</button>
<button class="alt" onclick="resetSort('pers')">Reset</button>
<div id="persResult" class="feedback"></div>
<details class="key">
<summary>Suggested answers</summary>
<b>Positive:</b> considerate, resilient, self-confident, tactful, broad-minded, down-to-earth, resourceful, loyal, cheerful, humble, easy-going, sociable, energetic.<br>
<b>Negative:</b> selfish, untrustworthy, big-headed, narrow-minded, tactless.<br>
<b>Depends:</b> insecure, moody, impetuous, laid-back, outgoing, reserved, loud, sensitive, shy, introverted.
</details>
</div>

<div class="task">
<h3>4.2 Match the opposites</h3>
<div id="opposites"></div>
<button onclick="checkSelect('opposites')">Check</button>
<div id="oppositesResult" class="feedback"></div>
<details class="key"><summary>Answers</summary>considerate–selfish; self-confident–insecure; tactful–tactless; broad-minded–narrow-minded; humble–big-headed; outgoing–reserved; cheerful–moody; easy-going–uptight; trustworthy–untrustworthy.</details>
</div>

<div class="task">
<h3>4.3 Guess the adjective</h3>
<div id="guessAdj"></div>
<button onclick="checkSelect('guessAdj')">Check</button>
<div id="guessAdjResult" class="feedback"></div>
<details class="key"><summary>Answers</summary>1 considerate; 2 big-headed; 3 insecure; 4 resourceful; 5 resilient; 6 tactless; 7 outgoing; 8 reserved; 9 energetic; 10 laid-back.</details>
</div>

<div class="task">
<h3>4.4 Complete the sentences</h3>
<div id="adjFill"></div>
<button onclick="checkInputs('adjFill')">Check</button>
<div id="adjFillResult" class="feedback"></div>
<details class="key"><summary>Answers</summary>1 considerate; 2 outgoing/sociable; 3 big-headed; 4 resilient; 5 untrustworthy; 6 resourceful; 7 moody; 8 broad-minded.</details>
</div>
</section>

<section id="idioms">
<h2>5. Idioms connected with personality</h2>
<div class="grid" id="idiomCards"></div>
<div class="task">
<h3>5.1 Match idioms with definitions</h3>
<div id="idiomMatch"></div>
<button onclick="checkSelect('idiomMatch')">Check</button>
<div id="idiomMatchResult" class="feedback"></div>
<details class="key"><summary>Answers</summary>1 a bright spark; 2 a party animal; 3 a pain in the neck; 4 a big mouth; 5 a live wire; 6 a wallflower; 7 a great laugh; 8 a social butterfly.</details>
</div>
<div class="task">
<h3>5.2 Guess the idiom</h3>
<div id="guessIdiom"></div>
<button onclick="checkSelect('guessIdiom')">Check</button>
<div id="guessIdiomResult" class="feedback"></div>
<details class="key"><summary>Answers</summary>1 a big mouth; 2 a social butterfly; 3 a live wire; 4 a wallflower; 5 a great laugh; 6 a pain in the neck; 7 a bright spark; 8 a party animal.</details>
</div>
<div class="task">
<h3>5.3 Complete the descriptions</h3>
<div id="idiomFill"></div>
<button onclick="checkInputs('idiomFill')">Check</button>
<div id="idiomFillResult" class="feedback"></div>
<details class="key"><summary>Answers</summary>1 a big mouth; 2 a great laugh; 3 a social butterfly; 4 a live wire; 5 a pain in the neck; 6 a wallflower; 7 a bright spark; 8 a party animal.</details>
</div>
</section>

<section id="guide">
<h2>6. Grammar guide: Present Perfect Simple & Continuous</h2>
<div class="two">
<div class="rule">
<h3>Present Perfect Simple</h3>
<b>Form:</b> have/has + V3 (past participle)<br>
<b>Focus:</b> result, experience, completed amount or number.<br>
<i>I've read three books this month.</i><br>
<i>She has made five dresses.</i><br>
<i>Have you ever tried rock climbing?</i>
</div>
<div class="rule">
<h3>Present Perfect Continuous</h3>
<b>Form:</b> have/has + been + verb-ing<br>
<b>Focus:</b> duration, process, ongoing or recently finished activity.<br>
<i>I've been reading all afternoon.</i><br>
<i>She has been making clothes for hours.</i><br>
<i>Have you been running?</i>
</div>
</div>
<table>
<tr><th>Use</th><th>Simple</th><th>Continuous</th></tr>
<tr><td>Result vs process</td><td>I've painted three pictures. (three finished results)</td><td>I've been painting all afternoon. (activity/duration)</td></tr>
<tr><td>Number / amount</td><td>How many books have you read?</td><td>Usually not used for a completed number.</td></tr>
<tr><td>Duration</td><td>How long have you known her? (state verb)</td><td>How long have you been learning English?</td></tr>
<tr><td>Recent activity</td><td>I've cleaned my room. (result)</td><td>I've been cleaning my room. (activity; perhaps unfinished)</td></tr>
</table>
<div class="rule"><b>FOR</b> + period: for two hours, for five years. <b>SINCE</b> + starting point: since Monday, since 2021, since I was a child.</div>
<div class="rule"><b>Stative verbs:</b> know, believe, understand, love, like, hate, own, belong are not normally used in continuous forms when describing a state. Say <i>I've known her for years</i>, not <i>I've been knowing her</i>.</div>
<div class="rule"><b>Time expressions:</b> already, yet, just, ever, never, so far, recently, lately, for, since, all morning, all week, how long, how many times. They are clues, not automatic tense rules: choose the tense according to the meaning.</div>
</section>

<section id="grammar">
<h2>7. Present Perfect practice</h2>
<div class="task">
<h3>7.1 Choose the correct tense</h3>
<div id="tenseChoice"></div>
<button onclick="checkSelect('tenseChoice')">Check</button>
<div id="tenseChoiceResult" class="feedback"></div>
<details class="key"><summary>Answers</summary>1 have been reading; 2 has baked; 3 have known; 4 has been playing; 5 have watched; 6 have been collecting; 7 have you been working; 8 has written; 9 has been learning; 10 have visited; 11 has been running; 12 have been trying.</details>
</div>
<div class="task">
<h3>7.2 Complete the sentences</h3>
<div id="tenseFill"></div>
<button onclick="checkInputs('tenseFill')">Check</button>
<div id="tenseFillResult" class="feedback"></div>
<details class="key"><summary>Answers</summary>1 has been practising; 2 have read; 3 have you been learning; 4 hasn't finished; 5 have been playing; 6 has made; 7 have you been crying; 8 have known; 9 has been writing; 10 haven't seen; 11 have you gone; 12 has been trying.</details>
</div>
<div class="task">
<h3>7.3 Spot the mistake</h3>
<p>Choose Correct or Incorrect. If incorrect, type the corrected sentence.</p>
<div id="mistakes"></div>
<button onclick="checkMistakes()">Check</button>
<div id="mistakesResult" class="feedback"></div>
<details class="key"><summary>Corrections</summary>1 I've known my best friend for ten years. 2 She has written three blog posts today. 3 How long have you had this hobby? 4 He's been playing basketball for five years. 5 I have been reading this book all evening. 6 Correct. 7 Correct. 8 Have you ever tried rock climbing? 9 Correct. 10 He has finished his homework.</details>
</div>
<div class="task">
<h3>7.4 Complete the dialogue</h3>
<div id="dialogue"></div>
<button onclick="checkInputs('dialogue')">Check</button>
<div id="dialogueResult" class="feedback"></div>
<details class="key"><summary>Answers</summary>have you been doing; have been preparing; have been learning; have you learned/learnt; have learned/learnt; have been practising; Have you ever performed; have never done.</details>
</div>
<div class="task">
<h3>7.5 FOR or SINCE?</h3>
<div id="forSince"></div>
<button onclick="checkSelect('forSince')">Check</button>
<div id="forSinceResult" class="feedback"></div>
<details class="key"><summary>Answers</summary>1 since; 2 for; 3 since; 4 since; 5 for; 6 for; 7 since; 8 for; 9 since; 10 since.</details>
</div>
<div class="task">
<h3>7.6 Rewrite the sentences</h3>
<div id="rewrite"></div>
<button onclick="checkInputs('rewrite')">Check</button>
<div id="rewriteResult" class="feedback"></div>
<details class="key"><summary>Sample answers</summary>1 I've been learning Spanish for three years. 2 She's been collecting vintage postcards since 2021. 3 I've never tried rock climbing before. 4 He's been practising the piano since 5 p.m. 5 I've read four books this month. 6 They've been renovating their house for two months. 7 I haven't been to a music festival since 2024. 8 I've been following this video blogger for a year.</details>
</div>
<div class="task">
<h3>7.7 What's the difference?</h3>
<p>Explain the meaning difference in each pair.</p>
<div id="pairs"></div>
<details class="key"><summary>Teacher's notes</summary>1a focuses on three completed pictures; 1b on the activity/duration. 2a highlights the number of completed posts; 2b the writing activity. 3a counts completed matches; 3b emphasises ongoing play. 4a means the whole book is finished; 4b focuses on the reading process. 5a focuses on the result; 5b on the activity, perhaps unfinished.</details>
</div>
<div class="task">
<h3>7.8 Find someone who…</h3>
<p>Ask a partner. Write their name and a follow-up note.</p>
<div id="findSomeone"></div>
</div>
<div class="task">
<h3>7.9 Choose the best explanation</h3>
<div id="explain"></div>
<button onclick="checkSelect('explain')">Check</button>
<div id="explainResult" class="feedback"></div>
<details class="key"><summary>Answers</summary>1 A; 2 B; 3 A; 4 A; 5 A.</details>
</div>
</section>

<section id="speaking">
<h2>8. Speaking & writing challenge</h2>
<div class="task">
<h3>8.1 Recommend hobbies for different personalities</h3>
<div class="two">
<div class="rule"><b>Person A</b><br>introverted · reserved · sensitive · enjoys spending time alone</div>
<div class="rule"><b>Person B</b><br>outgoing · energetic · sociable · loves meeting new people</div>
<div class="rule"><b>Person C</b><br>resourceful · broad-minded · adventurous · enjoys challenges</div>
<div class="rule"><b>Person D</b><br>laid-back · easy-going · down-to-earth · prefers relaxing activities</div>
</div>
<p>Recommend three hobbies for each person. Explain your choices using: I'd recommend… because… / This would suit them because… / It would give them an opportunity to…</p>
<textarea placeholder="Write your recommendations here…"></textarea>
</div>
<div class="task">
<h3>8.2 Discussion questions</h3>
<ol>
<li>Can a shy person be a party animal?</li>
<li>Can someone be both introverted and sociable?</li>
<li>Which personality traits make someone a good friend?</li>
<li>Is it better to be laid-back or energetic?</li>
<li>Do hobbies reflect our personalities?</li>
<li>Which personality traits are difficult to deal with?</li>
<li>Do you prefer hobbies that help you unwind or activities that challenge you?</li>
<li>Can an introvert be a successful video blogger?</li>
</ol>
</div>
<div class="task">
<h3>8.3 Present Perfect speaking challenge</h3>
<ol>
<li>What hobbies have you taken up recently?</li>
<li>How long have you been interested in your favourite hobby?</li>
<li>What skills have you developed over the last few years?</li>
<li>Have you ever tried a hobby that surprised you?</li>
<li>What have you been doing to improve your English?</li>
<li>How many books have you read this year?</li>
<li>Have you been spending enough time with your friends recently?</li>
<li>What have you been thinking about learning?</li>
<li>Have you ever given up a hobby? Why?</li>
<li>What activities have helped you recharge your batteries recently?</li>
</ol>
</div>
<div class="task">
<h3>8.4 How have you changed? — Blog post</h3>
<p>Write about how your personality, interests and hobbies have changed over the last five years. Include at least 3 personality adjectives, 2 idioms, 4 hobbies, 3 examples of Present Perfect Simple and 3 examples of Present Perfect Continuous.</p>
<textarea placeholder="Over the last few years, I've become more self-confident and outgoing…"></textarea>
</div>
</section>

<div class="progress">
<span>Interactive checks completed</span>
<b id="done">0</b>
<button class="alt" onclick="scrollTo({top:0,behavior:'smooth'})">↑ Top</button>
</div>
</main>
<footer>B1–B2 English lesson · Purple edition</footer>

<script>
const $=id=>document.getElementById(id),
esc=s=>String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c])),
norm=s=>String(s||'').toLowerCase().replace(/[’']/g,"'").replace(/[.,!?]/g,'').replace(/\s+/g,' ').trim(),
done=new Set();

/* FIXED TOP NAVIGATION */
document.getElementById('topNav').addEventListener('click',function(event){
  const link=event.target.closest('a[href^="#"]');
  if(!link)return;
  const id=link.getAttribute('href').substring(1);
  const target=document.getElementById(id);
  if(!target)return;
  event.preventDefault();
  target.scrollIntoView({behavior:'smooth',block:'start'});
  history.replaceState(null,'','#'+id);
});

function mark(k){done.add(k);$('done').textContent=done.size}

const words=[
['bake cakes','печь торты','hobbies'],
['collect figures, cards, stamps, etc.','коллекционировать фигурки, карточки, марки и т. д.','hobbies'],
['draw','рисовать','hobbies'],
['hang out with friends','проводить время с друзьями','hobbies'],
['make clothes','шить одежду','hobbies'],
['read books','читать книги','hobbies'],
['read magazines','читать журналы','hobbies'],
['text your friends','переписываться с друзьями','hobbies'],
['use social media','пользоваться соцсетями','hobbies'],
['video blog / vlog','вести видеоблог','hobbies'],
['watch videos online','смотреть видео онлайн','hobbies'],
...Object.entries({
'ballet':'балет','ballroom dancing':'бальные танцы','basketball':'баскетбол','board games':'настольные игры','bowling':'боулинг','camping':'кемпинг','cards':'карточные игры','chess':'шахматы','cycling':'езда на велосипеде','drama':'театральное искусство','gymnastics':'гимнастика','horse riding':'верховая езда','ice hockey':'хоккей с шайбой','ice skating':'катание на коньках','martial arts':'боевые искусства','a musical instrument':'музыкальный инструмент','photography':'фотография','rollerblading':'катание на роликах','running':'бег','shopping':'шопинг','skateboarding':'скейтбординг','table tennis':'настольный теннис','volleyball':'волейбол','weights / weight training':'силовые тренировки','yoga':'йога','aerobics':'аэробика','athletics':'лёгкая атлетика','pottery':'гончарное дело','DIY projects':'проекты «сделай сам»','gardening':'садоводство','embroidery':'вышивание','origami':'оригами','meditation':'медитация','Pilates':'пилатес','tai chi':'тайцзи','parkour':'паркур','kickboxing':'кикбоксинг','judo':'дзюдо','video games':'видеоигры','badminton':'бадминтон','rugby':'регби','poker':'покер','darts':'дартс','the piano':'фортепиано','the guitar':'гитара','the drums':'барабаны','squash':'сквош','snooker':'снукер','fishing':'рыбалка','hiking':'пешие походы','sailing':'парусный спорт','skiing':'лыжи','snowboarding':'сноубординг','scuba diving':'дайвинг с аквалангом','rock climbing':'скалолазание','mountain biking':'горный велосипед','kayaking':'катание на каяке','windsurfing':'виндсёрфинг','birdwatching':'наблюдение за птицами','trekking':'треккинг','bouldering':'боулдеринг'
}).map(([a,b])=>[a,b,'hobbies']),
...Object.entries({
'considerate':'внимательный к чувствам других','insecure':'неуверенный в себе','moody':'с переменчивым настроением','resilient':'стойкий','self-confident':'уверенный в себе','selfish':'эгоистичный','tactful':'тактичный','untrustworthy':'ненадёжный','broad-minded':'с широкими взглядами','down-to-earth':'практичный, здравомыслящий','impetuous':'импульсивный','laid-back':'расслабленный, невозмутимый','outgoing':'общительный, открытый','reserved':'сдержанный','resourceful':'находчивый','big-headed':'самодовольный, заносчивый','energetic':'энергичный','loud':'громкий, шумный','loyal':'преданный','sensitive':'чувствительный','shy':'застенчивый','cheerful':'жизнерадостный','easy-going':'покладистый','humble':'скромный','introverted':'интровертированный','narrow-minded':'ограниченный во взглядах','sociable':'общительный','tactless':'бестактный','trustworthy':'заслуживающий доверия','uptight':'напряжённый, скованный'
}).map(([a,b])=>[a,b,'personality']),
...Object.entries({
'a big mouth':'болтун, не умеющий хранить секреты','a bright spark':'очень сообразительный человек','a great laugh':'весёлый человек, с которым приятно проводить время','a live wire':'очень энергичный человек','a pain in the neck':'человек, который раздражает','a party animal':'любитель вечеринок','a social butterfly':'общительный человек, легко заводящий знакомства','a wallflower':'застенчивый человек в стороне на вечеринке'
}).map(([a,b])=>[a,b,'idioms']),
...Object.entries({
'journaling':'ведение дневника','creative writing':'литературное творчество','calligraphy':'каллиграфия','knitting':'вязание','solving puzzles':'решение головоломок','crosswords':'кроссворды','genealogy':'генеалогия','stargazing':'наблюдение за звёздами','composing music':'сочинение музыки','digital illustration':'цифровая иллюстрация','philosophy':'философия','woodworking':'работа по дереву','scrapbooking':'альбомы из фотографий и памятных вещей','film-making':'создание фильмов','podcasting':'создание подкастов','DJing':'диджеинг','antique collecting':'коллекционирование антиквариата','furniture restoration':'реставрация мебели','volunteering':'волонтёрство','public speaking':'публичные выступления','debating':'дебаты','community gardening':'совместное садоводство','tea tasting':'дегустация чая','coffee tasting':'дегустация кофе','archery':'стрельба из лука','fencing':'фехтование','figure skating':'фигурное катание','mountaineering':'альпинизм','urban exploration':'исследование необычных городских мест','trail running':'бег по пересечённой местности'
}).map(([a,b])=>[a,b,'extra'])
];

let cardList=[...new Map(words.map(x=>[x[0],x])).values()];

function renderCards(){
let f=$('filter').value,
arr=cardList.filter(x=>f==='all'||x[2]===f);
$('count').textContent=arr.length+' cards';
$('cardsGrid').innerHTML=arr.map(x=>`<div class="card" tabindex="0" onclick="this.classList.toggle('flip')" onkeydown="if(event.key==='Enter'||event.key===' '){event.preventDefault();this.classList.toggle('flip')}"><div class="inner"><div class="face">${esc(x[0])}</div><div class="face back">${esc(x[1])}</div></div></div>`).join('');
}
$('filter').onchange=renderCards;
function shuffle(){cardList.sort(()=>Math.random()-.5);renderCards()}
renderCards();

const sorts={
dpg:['dpgBank',[
...'ballet|ballroom dancing|gymnastics|martial arts|drama|yoga|aerobics|athletics|weight training|pottery|DIY projects|gardening|embroidery|origami|meditation|Pilates|tai chi|parkour|kickboxing|judo'.split('|').map(x=>[x,'do']),
...'basketball|board games|cards|chess|ice hockey|table tennis|volleyball|a musical instrument|video games|badminton|rugby|poker|darts|the piano|the guitar|the drums|squash|snooker'.split('|').map(x=>[x,'play']),
...'camping|cycling|horse riding|ice skating|rollerblading|running|shopping|skateboarding|bowling|fishing|hiking|sailing|skiing|snowboarding|scuba diving|rock climbing|mountain biking|kayaking|windsurfing|birdwatching|trekking|bouldering'.split('|').map(x=>[x,'go'])
]],
hobby:['hobbyBank',[
...'read books|read magazines|draw|bake cakes|collect figures and stamps|make clothes|journaling|creative writing|calligraphy|knitting|solving puzzles|birdwatching|learning languages|playing chess|crosswords|model building|genealogy|stargazing|composing music|digital illustration|philosophy|embroidery|pottery|scrapbooking'.split('|').map(x=>[x,'intro']),
...'hang out with friends|text your friends|ballroom dancing|team sports|drama|karaoke|volunteering|music festivals|networking events|debate clubs|amateur theatre|social gatherings|escape rooms|salsa dancing|comedy shows|group travel|book clubs|charity events|live concerts|hosting dinner parties'.split('|').map(x=>[x,'extro']),
...'photography|cycling|hiking|video blogging|cooking|travelling|gardening|learning languages|playing musical instruments|gaming|dancing|volunteering|going to the cinema|workshops|shopping|camping|film-making|podcasting'.split('|').map(x=>[x,'both'])
]],
pers:['persBank',[
...'considerate|resilient|self-confident|tactful|broad-minded|down-to-earth|resourceful|loyal|cheerful|humble|easy-going|sociable|energetic'.split('|').map(x=>[x,'positive']),
...'selfish|untrustworthy|big-headed|narrow-minded|tactless'.split('|').map(x=>[x,'negative']),
...'insecure|moody|impetuous|laid-back|outgoing|reserved|loud|sensitive|shy|introverted'.split('|').map(x=>[x,'depends'])
]]
};

let selected=null;
function initSort(k){
let [bank,items]=sorts[k];
$(bank).innerHTML='';
items.forEach(([w,a],i)=>{
let c=document.createElement('span');
c.className='chip';
c.textContent=w;
c.draggable=true;
c.dataset.group=k;
c.dataset.answer=a;
c.dataset.id=k+i;
c.ondragstart=e=>e.dataTransfer.setData('text',c.dataset.id);
c.onclick=()=>{
document.querySelectorAll('.chip.sel').forEach(x=>x.classList.remove('sel'));
selected=c;
c.classList.add('sel');
};
$(bank).append(c);
});
}
Object.keys(sorts).forEach(initSort);

document.querySelectorAll('.zone').forEach(z=>{
z.ondragover=e=>{e.preventDefault();z.classList.add('over')};
z.ondragleave=()=>z.classList.remove('over');
z.ondrop=e=>{
e.preventDefault();
z.classList.remove('over');
let el=document.querySelector(`[data-id="${e.dataTransfer.getData('text')}"]`);
if(el&&el.dataset.group===z.dataset.group)z.querySelector('.placed').append(el);
};
z.onclick=()=>{
if(selected&&selected.dataset.group===z.dataset.group){
z.querySelector('.placed').append(selected);
selected.classList.remove('sel');
selected=null;
}
};
});

function checkSort(k){
let [bank,items]=sorts[k],
section=k==='dpg'?'dpg':k==='hobby'?'hobbies':'personality',
els=document.querySelectorAll('#'+bank+' .chip, #'+section+' .zone .chip'),
n=0;
els.forEach(e=>{
let ok=e.closest('.zone')?.dataset.cat===e.dataset.answer;
e.style.borderColor=ok?'#31945e':'#c55b70';
if(ok)n++;
});
$(k+'Result').textContent=`${n} / ${items.length} placed in the suggested category.`;
$(k+'Result').className='feedback '+(n===items.length?'good':'bad');
mark(k);
}
function resetSort(k){
let [bank]=sorts[k],
section=k==='dpg'?'dpg':k==='hobby'?'hobbies':'personality';
document.querySelectorAll('#'+section+' .zone .chip').forEach(e=>{
$(bank).append(e);
e.style.borderColor='';
});
$(k+'Result').textContent='';
}

function renderSelect(id,qs){
$(id).innerHTML=qs.map((q,i)=>`<div class="q">${i+1}. ${q.q}<br><select data-a="${esc(q.a)}"><option value="">Choose…</option>${q.o.map(x=>`<option>${esc(x)}</option>`).join('')}</select></div>`).join('');
}
function checkSelect(id){
let es=$(id).querySelectorAll('select'),n=0;
es.forEach(e=>{
let ok=norm(e.value)===norm(e.dataset.a);
e.style.borderColor=ok?'#31945e':'#c55b70';
if(ok)n++;
});
$(id+'Result').textContent=`${n} / ${es.length} correct.`;
$(id+'Result').className='feedback '+(n===es.length?'good':'bad');
mark(id);
}
function renderInputs(id,qs){
$(id).innerHTML=qs.map((q,i)=>`<div class="q">${i+1}. ${q.q}<br><input type="text" data-a="${esc(q.a)}" placeholder="Your answer" style="width:min(100%,600px)"></div>`).join('');
}
function checkInputs(id){
let es=$(id).querySelectorAll('input'),n=0;
es.forEach(e=>{
let ok=e.dataset.a.split('|').map(norm).includes(norm(e.value));
e.style.borderColor=ok?'#31945e':'#c55b70';
if(ok)n++;
});
$(id+'Result').textContent=`${n} / ${es.length} correct. See the answer key for alternatives.`;
$(id+'Result').className='feedback '+(n===es.length?'good':'bad');
mark(id);
}

renderSelect('opposites',[
{q:'considerate',a:'selfish',o:['selfish','tactful','loyal']},
{q:'self-confident',a:'insecure',o:['resilient','insecure','reserved']},
{q:'tactful',a:'tactless',o:['tactless','humble','sensitive']},
{q:'broad-minded',a:'narrow-minded',o:['down-to-earth','narrow-minded','resourceful']},
{q:'humble',a:'big-headed',o:['big-headed','cheerful','easy-going']},
{q:'outgoing',a:'reserved',o:['sociable','reserved','energetic']},
{q:'cheerful',a:'moody',o:['moody','loyal','considerate']},
{q:'easy-going',a:'uptight',o:['uptight','laid-back','shy']},
{q:'trustworthy',a:'untrustworthy',o:['untrustworthy','selfish','impetuous']}
]);

renderSelect('guessAdj',[
{q:'Emma considers other people’s feelings before speaking.',a:'considerate',o:['considerate','selfish','loud']},
{q:'Jack thinks he is more important and talented than everyone else.',a:'big-headed',o:['humble','big-headed','shy']},
{q:'Sarah doubts herself and feels uncomfortable speaking in a group.',a:'insecure',o:['self-confident','insecure','resilient']},
{q:'Tom finds solutions even when he has few resources.',a:'resourceful',o:['resourceful','moody','tactless']},
{q:'Anna keeps going when life becomes difficult.',a:'resilient',o:['impetuous','resilient','untrustworthy']},
{q:'Mark says things without considering whether they might hurt someone.',a:'tactless',o:['tactful','tactless','considerate']},
{q:'Sophie enjoys meeting new people.',a:'outgoing',o:['reserved','outgoing','insecure']},
{q:'Ben is quiet and does not talk much about himself.',a:'reserved',o:['loud','reserved','big-headed']},
{q:'Lucy has lots of energy and enthusiasm.',a:'energetic',o:['energetic','laid-back','moody']},
{q:'Peter stays relaxed and does not worry about small problems.',a:'laid-back',o:['uptight','laid-back','impetuous']}
]);

renderInputs('adjFill',[
{q:'You should be more ______ and think about how your words affect others.',a:'considerate'},
{q:'My sister is very ______. She can talk to almost anyone.',a:'outgoing|sociable'},
{q:'He is too ______ to admit that he has made a mistake.',a:'big-headed'},
{q:'Although she is quite ______, she never gives up.',a:'resilient'},
{q:'I do not think he is ______. He often breaks promises.',a:'untrustworthy'},
{q:'My best friend is very ______. She solves unexpected problems.',a:'resourceful'},
{q:'He is a little ______, so his mood changes often.',a:'moody'},
{q:'I admire people who are ______ enough to accept different opinions.',a:'broad-minded'}
]);

const idioms=['a big mouth','a bright spark','a great laugh','a live wire','a pain in the neck','a party animal','a social butterfly','a wallflower'];
const iru=['болтун, не умеющий хранить секреты','очень сообразительный человек','весёлый человек, с которым приятно проводить время','очень энергичный человек','человек или ситуация, которые раздражают','любитель вечеринок','общительный человек, легко заводящий знакомства','застенчивый человек, который держится в стороне на вечеринках'];

$('idiomCards').innerHTML=idioms.map((x,i)=>`<div class="card" onclick="this.classList.toggle('flip')"><div class="inner"><div class="face">${x}</div><div class="face back">${iru[i]}</div></div></div>`).join('');

renderSelect('idiomMatch',[
{q:'Someone very intelligent and quick to understand things.',a:idioms[1],o:idioms},
{q:'Someone who enjoys parties and social events.',a:idioms[5],o:idioms},
{q:'Someone annoying and difficult to deal with.',a:idioms[4],o:idioms},
{q:'Someone who talks too much and reveals secrets.',a:idioms[0],o:idioms},
{q:'Someone extremely energetic and enthusiastic.',a:idioms[3],o:idioms},
{q:'Someone shy who does not participate much at social events.',a:idioms[7],o:idioms},
{q:'Someone fun to be around and who makes people laugh.',a:idioms[2],o:idioms},
{q:'Someone who enjoys meeting people and socialising.',a:idioms[6],o:idioms}
]);

renderSelect('guessIdiom',[
{q:'Do not tell Mark the secret; he will tell everyone.',a:idioms[0],o:idioms},
{q:'Lisa knows everyone at the party and moves from group to group.',a:idioms[6],o:idioms},
{q:'Tom dances, talks and organises activities; he never runs out of energy.',a:idioms[3],o:idioms},
{q:'Emily stands alone because she does not know anyone.',a:idioms[7],o:idioms},
{q:'Everyone loves Jack because he is funny and enjoyable to be around.',a:idioms[2],o:idioms},
{q:'Our neighbour complains about everything and makes simple things difficult.',a:idioms[4],o:idioms},
{q:'Sarah is incredibly clever and comes up with brilliant ideas.',a:idioms[1],o:idioms},
{q:'Mike loves parties, clubs and festivals.',a:idioms[5],o:idioms}
]);

renderInputs('idiomFill',[
{q:'Do not tell Peter about the surprise. He has got ______!',a:'a big mouth'},
{q:'Invite Sophie. She is ______ and makes everyone laugh.',a:'a great laugh'},
{q:'At parties, my brother is ______. He knows absolutely everyone.',a:'a social butterfly'},
{q:'My cousin is a real ______. He cannot sit still.',a:'a live wire'},
{q:'I do not enjoy working with him. He is such ______!',a:'a pain in the neck'},
{q:'I used to be a ______ at school parties.',a:'a wallflower'},
{q:'She is a real ______. She solves complicated problems.',a:'a bright spark'},
{q:'My uncle is a ______. He goes to parties and festivals.',a:'a party animal'}
]);

renderSelect('tenseChoice',[
{q:'I ___ this book for two hours.',a:'have been reading',o:['have read','have been reading']},
{q:'She ___ three cakes today.',a:'has baked',o:['has baked','has been baking']},
{q:'How long ___ your best friend?',a:'have you known',o:['have you known','have you been knowing']},
{q:'Tom ___ basketball since 4 p.m.',a:'has been playing',o:['has played','has been playing']},
{q:'I ___ five episodes this week.',a:'have watched',o:['have watched','have been watching']},
{q:'They ___ stamps since childhood.',a:'have been collecting',o:['have collected','have been collecting']},
{q:'Why are your clothes dirty? ___ in the garden?',a:'Have you been working',o:['Have you worked','Have you been working']},
{q:'She ___ three articles this month.',a:'has written',o:['has written','has been writing']},
{q:'My brother ___ Japanese for six months.',a:'has been learning',o:['has learned','has been learning']},
{q:'We ___ four museums so far.',a:'have visited',o:['have visited','have been visiting']},
{q:'He is tired because he ___.',a:'has been running',o:['has run','has been running']},
{q:'I ___ to contact her all morning.',a:'have been trying',o:['have tried','have been trying']}
]);

renderInputs('tenseFill',[
{q:'Sarah ______ (practise) the piano for three hours, and she still has not finished.',a:'has been practising|has been practicing'},
{q:'I ______ (read) two books this month.',a:'have read'},
{q:'How long ______ you ______ (learn) photography?',a:'have you been learning'},
{q:'He ______ (not finish) his model yet.',a:"hasn't finished|has not finished"},
{q:'They ______ (play) chess since lunchtime.',a:'have been playing'},
{q:'My sister ______ (make) five dresses so far.',a:'has made'},
{q:'Your eyes are red. ______ you ______ (cry)?',a:'have you been crying'},
{q:'We ______ (know) each other since primary school.',a:'have known'},
{q:'Jack ______ (write) his blog for two years.',a:'has been writing'},
{q:'I ______ (not see) Mark recently.',a:"haven't seen|have not seen"},
{q:'How many times ______ you ______ (go) camping this year?',a:'have you gone'},
{q:'She ______ (try) to learn ballroom dancing.',a:'has been trying'}
]);

const ms=[
["I've been knowing my best friend for ten years.",false,"I've known my best friend for ten years."],
["She has been written three blog posts today.",false,"She has written three blog posts today."],
["How long have you been having this hobby?",false,"How long have you had this hobby?"],
["He's been playing basketball since five years.",false,"He's been playing basketball for five years."],
["I have been read this book all evening.",false,"I have been reading this book all evening."],
["They have visited us three times this month already.",true,"Correct."],
["She has been making clothes since she was a teenager.",true,"Correct."],
["Have you ever been trying rock climbing?",false,"Have you ever tried rock climbing?"],
["I've been collecting stamps since I was a child.",true,"Correct."],
["He has been finished his homework.",false,"He has finished his homework."]
];

$('mistakes').innerHTML=ms.map((m,i)=>`<div class="q">${i+1}. ${m[0]}<br><label><input type="radio" name="m${i}" value="yes"> Correct</label> <label><input type="radio" name="m${i}" value="no"> Incorrect</label><br><input id="fix${i}" placeholder="Write the correction if needed" style="width:min(100%,570px)"></div>`).join('');

function checkMistakes(){
let n=0;
ms.forEach((m,i)=>{
let v=document.querySelector(`input[name=m${i}]:checked`),
ok=v&&((v.value==='yes')===m[1]);
if(ok&&(m[1]||norm($('fix'+i).value)===norm(m[2])))n++;
});
$('mistakesResult').textContent=`${n} / ${ms.length} correct. For incorrect sentences, write the corrected version.`;
$('mistakesResult').className='feedback '+(n===ms.length?'good':'bad');
mark('mistakes');
}

renderInputs('dialogue',[
{q:'Anna: What ______ you ______ (do)?',a:'have you been doing'},
{q:'Ben: I ______ (prepare) for the talent show all afternoon.',a:'have been preparing'},
{q:'Ben: I ______ (learn) to play the guitar for six months.',a:'have been learning'},
{q:'Anna: How many songs ______ you ______ (learn) so far?',a:'have you learned|have you learnt'},
{q:'Ben: I ______ (learn) four.',a:'have learned|have learnt'},
{q:'Ben: I ______ (practise) the same one all week.',a:'have been practising|have been practicing'},
{q:'Anna: ______ you ever ______ (perform) in front of an audience?',a:'have you ever performed'},
{q:'Ben: No, I ______ never ______ (do) that before.',a:'have never done'}
]);

renderSelect('forSince',[
{q:'I have been interested in photography ___ I was a child.',a:'since',o:['for','since']},
{q:'She has been learning ballet ___ five years.',a:'for',o:['for','since']},
{q:'They have known each other ___ 2020.',a:'since',o:['for','since']},
{q:'I have been trying to finish this book ___ Monday.',a:'since',o:['for','since']},
{q:'He has collected coins ___ a long time.',a:'for',o:['for','since']},
{q:'We have been waiting ___ half an hour.',a:'for',o:['for','since']},
{q:'My sister has been a member of the chess club ___ September.',a:'since',o:['for','since']},
{q:'I have had this camera ___ two years.',a:'for',o:['for','since']},
{q:'They have been practising ___ lunchtime.',a:'since',o:['for','since']},
{q:'She has loved dancing ___ she was little.',a:'since',o:['for','since']}
]);

renderInputs('rewrite',[
{q:'I started learning Spanish three years ago. (FOR)',a:"I've been learning Spanish for three years|I have been learning Spanish for three years"},
{q:'She started collecting vintage postcards in 2021. (SINCE)',a:"She's been collecting vintage postcards since 2021|She has been collecting vintage postcards since 2021"},
{q:'This is my first time trying rock climbing. (NEVER)',a:"I've never tried rock climbing before|I have never tried rock climbing before"},
{q:'He started practising the piano at 5 p.m. and is still practising. (SINCE)',a:"He's been practising the piano since 5 p.m.|He has been practising the piano since 5 p.m."},
{q:'I finished four books this month. (READ)',a:"I've read four books this month|I have read four books this month"},
{q:'They started renovating their house two months ago and have not finished. (BEEN)',a:"They've been renovating their house for two months|They have been renovating their house for two months"},
{q:'She last went to a music festival in 2024. (SINCE)',a:"She hasn't been to a music festival since 2024|She has not been to a music festival since 2024"},
{q:'I started following this video blogger a year ago. (FOR)',a:"I've been following this video blogger for a year|I have been following this video blogger for a year"}
]);

$('pairs').innerHTML=[
["I've painted three pictures today.","I've been painting all afternoon."],
["She's written five blog posts this month.","She's been writing her blog all morning."],
["They've played four matches this week.","They've been playing football since lunchtime."],
["He's read the whole book.","He's been reading the book."],
["I've cleaned my room.","I've been cleaning my room."]
].map((p,i)=>`<div class="q">${i+1}a. ${p[0]}<br>${i+1}b. ${p[1]}<textarea placeholder="Explain the difference…"></textarea></div>`).join('');

$('findSomeone').innerHTML=[
['tried an unusual hobby','Have you ever tried an unusual hobby?'],
['been learning a new skill','How long have you been learning it?'],
['read more than three books this year','How many books have you read this year?'],
['been watching a series recently','What series have you been watching?'],
['visited another country this year','Which countries have you visited?'],
['been doing sport regularly','How long have you been doing it?'],
['never gone camping','Have you ever gone camping?'],
['collected something','What have you collected?'],
['recently taken up a new hobby','What hobby have you taken up?'],
['been spending more time outdoors','Why have you been doing that?']
].map((x,i)=>`<div class="q">${i+1}. Find someone who has ${x[0]}.<br><b>Ask:</b> ${x[1]}<br><input placeholder="Partner's name"> <input placeholder="Follow-up note"></div>`).join('');

renderSelect('explain',[
{q:'I have been learning guitar for six months. A: I started six months ago and I am still learning. B: I finished learning six months ago.',a:'A',o:['A','B']},
{q:'She has made four dresses this month. A: She is making the fourth right now. B: Four dresses are completed.',a:'B',o:['A','B']},
{q:'They have been arguing all morning. A: The argument has been going on for some time. B: They had exactly one argument.',a:'A',o:['A','B']},
{q:'I have visited London three times. A: I have visited on three occasions. B: I am still travelling around London.',a:'A',o:['A','B']},
{q:'He has been working on his photography project. A: The activity has been taking place recently. B: The project is definitely finished.',a:'A',o:['A','B']}
]);
</script>
</body>
</html>
