---
title: "Research"
layout: page
permalink: /research/
---

<p class="subtitle">My work develops likelihood-based and distribution-free methods for detecting and dating structural change, with applications to high-dimensional, sequential, and biomedical data.</p>

<style>
@import url('https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400;0,500;0,600;1,400&family=Source+Sans+3:wght@400;600&display=swap');
:root{
  --cream:#f8f5ee; --cream-2:#f2efe6; --ink:#2b2a27; --ink-soft:#57534a;
  --maroon:#7c2233; --maroon-2:#8f3247; --line:#ddd6c7; --box:#efece2;
}
.research-page{font-family:'Lora',Georgia,'Times New Roman',serif; color:var(--ink); background:var(--cream); padding:8px 4px;}
.research-page .subtitle{color:var(--ink-soft); font-size:1rem; margin:0 0 32px; max-width:62ch; line-height:1.6;}
.research-page h2{font-family:'Lora',serif; font-weight:600; font-size:1.3rem; color:var(--maroon); margin:36px 0 14px; padding-bottom:10px; border-bottom:2px solid var(--line);}
.interests{display:flex; flex-wrap:wrap; gap:10px; margin-top:4px;}
.tag-btn{font-family:'Source Sans 3',sans-serif; font-size:.92rem; font-weight:600; color:var(--maroon); background:var(--cream); border:1.5px solid var(--maroon); border-radius:999px; padding:8px 18px; cursor:pointer; transition:background .15s,color .15s; line-height:1.2;}
.tag-btn:hover{background:var(--box);}
.tag-btn.active{background:var(--maroon); color:var(--cream); border-color:var(--maroon);}
.count{color:var(--ink-soft); font-size:.9rem; margin:14px 0 0; font-family:'Source Sans 3',sans-serif;}
.legend{color:var(--ink-soft); font-size:.85rem; margin:0 0 18px; font-family:'Source Sans 3',sans-serif;}
.pub-list{list-style:none; margin:0; padding:0;}
.pub{display:flex; gap:14px; padding:22px 0; border-bottom:1px solid var(--line);}
.pub:last-child{border-bottom:none;}
.pub.hidden{display:none;}
.pub-num{color:var(--ink-soft); font-variant-numeric:tabular-nums; min-width:2.2em; font-size:.95rem; padding-top:2px;}
.pub-body{font-size:1rem; line-height:1.65;}
.pub-body b{font-weight:600;}
.venue,.pdf{display:inline-block; font-family:'Source Sans 3',sans-serif; font-size:.82rem; border:1px solid var(--line); border-radius:5px; padding:1px 8px; margin:0 3px; vertical-align:baseline;}
.venue{font-style:italic; color:var(--maroon-2); background:var(--box);}
.pdf{color:var(--maroon); text-decoration:none; font-weight:600;}
.pdf:hover{background:var(--box);}
</style>

<div class="research-page">

## Research Interests

<div class="interests" id="filters">
  <button class="tag-btn active" data-filter="all">All Publications</button>
  <button class="tag-btn" data-filter="cp">Change Point Analysis</button>
  <button class="tag-btn" data-filter="seq">Sequential Data Analysis</button>
  <button class="tag-btn" data-filter="inf">Statistical Inferences</button>
  <button class="tag-btn" data-filter="hd">High-Dimensional Data Analysis</button>
  <button class="tag-btn" data-filter="bd">Bounds and Inequalities</button>
</div>

## Publications

<p class="legend">* denotes co-first authors &nbsp;&middot;&nbsp; &dagger; denotes undergraduate/graduate student co-authors</p>
<p class="count" id="count"></p>
<ol class="pub-list" id="pubList" reversed></ol>

</div>

<script>
const PUBS = [
  {y:2026, tags:['bd'], pdf:'#', a:'From, S. G., &amp; <b>Ratnasingam, S.</b>', t:'Some New Bounds for the Dirichlet Beta Function', v:'Aust. J. Math. Anal. Appl.', i:'23(1), Art. 13, 1&ndash;22'},
  {y:2025, tags:['cp','seq','hd'], pdf:'#', a:'Gu, C.<sup>*</sup>, &amp; <b>Ratnasingam, S.</b><sup>*</sup>', t:'Change Point Detection in SCAD-Penalized Dynamic Panel Models', v:'Sequential Analysis', i:'44(4), 377&ndash;403'},
  {y:2025, tags:['bd'], pdf:'#', a:'From, S. G., &amp; <b>Ratnasingam, S.</b>', t:'New Upper and Lower Bounds for the Upper Incomplete Gamma Function', v:'Results in Applied Mathematics', i:'25, 100552'},
  {y:2025, tags:['cp','inf'], pdf:'#', a:'<b>Ratnasingam, S.</b>, &amp; Gamage, R. D. P.', t:'Empirical Likelihood Change Point Detection in Quantile Regression Models', v:'Computational Statistics', i:'40, 999&ndash;1020'},
  {y:2024, tags:['cp','inf'], pdf:'#', a:'Li, M., <b>Ratnasingam, S.</b>, Tian, Y., &amp; Ning, W.', t:'Change Point Detection in Length-biased Lognormal Distribution', v:'Communications in Statistics &ndash; Simulation and Computation', i:'54(11), 4605&ndash;4622'},
  {y:2024, tags:['inf'], pdf:'#', a:'<b>Ratnasingam, S.</b>, Wallace, S.<sup>&dagger;</sup>, Amani, I.<sup>&dagger;</sup>, &amp; Romero, J.<sup>&dagger;</sup>', t:'Nonparametric Confidence Intervals for Generalized Lorenz Curve Using Modified Empirical Likelihood', v:'Computational Statistics', i:'39, 3073&ndash;3090'},
  {y:2023, tags:['hd'], pdf:'#', a:'<b>Ratnasingam, S.</b>, &amp; Mu&ntilde;oz-Lopez, J.<sup>&dagger;</sup>', t:'Distance Correlation-Based Feature Selection in Random Forest', v:'Entropy', i:'25(9), 1250'},
  {y:2023, tags:['cp','seq'], pdf:'#', a:'Gu, C.<sup>*</sup>, &amp; <b>Ratnasingam, S.</b><sup>*</sup>', t:'Real-Time Change Point Detection in Linear Models Using the Ranking Selection Procedure', v:'Sequential Analysis', i:'42(2), 129&ndash;149'},
  {y:2023, tags:['cp'], pdf:'#', a:'<b>Ratnasingam, S.</b>, &amp; Ning, W.', t:'Change Point Detection in Linear Failure Rate Distribution Under Random Censorship', v:'Journal of Statistical Theory and Practice', i:'17(1), 1&ndash;22'},
  {y:2023, tags:['inf'], pdf:'#', a:'<b>Ratnasingam, S.</b>, &amp; Ning, W.', t:'Confidence Intervals of Mean Residual Life Function in Length-Biased Sampling Based on Modified Empirical Likelihood', v:'Journal of Biopharmaceutical Statistics', i:'33(1), 114&ndash;129'},
  {y:2022, tags:['bd','inf'], pdf:'#', a:'From, S. G., &amp; <b>Ratnasingam, S.</b>', t:'Some Efficient Closed-Form Estimators of the Parameters of the Generalized Pareto Distribution', v:'Environmental and Ecological Statistics', i:'29(4), 827&ndash;847'},
  {y:2022, tags:['cp','inf'], pdf:'#', a:'<b>Ratnasingam, S.</b>, Buzaianu, E., &amp; Ning, W.', t:'Modified Information Criterion for Testing Changes in Generalized Lambda Distribution Model Based on Confidence Distribution', v:'Communications for Statistical Applications and Methods', i:'29(3), 301&ndash;317'},
  {y:2022, tags:['bd'], pdf:'#', a:'From, S. G., &amp; <b>Ratnasingam, S.</b>', t:'Some New Inequalities for the Beta Function and Certain Ratios of Beta Functions', v:'Results in Applied Mathematics', i:'15, 100302'},
  {y:2022, tags:['inf'], pdf:'#', a:'Li, M., <b>Ratnasingam, S.</b>, &amp; Ning, W.', t:'Empirical-Likelihood-Based Confidence Intervals for Quantile Regression Models with Longitudinal Data', v:'Journal of Statistical Computation and Simulation', i:'92(12), 2536&ndash;2553'},
  {y:2021, tags:['cp','seq','hd'], pdf:'#', a:'<b>Ratnasingam, S.</b>, &amp; Ning, W.', t:'Monitoring Sequential Structural Changes in Penalized High-Dimensional Linear Models', v:'Sequential Analysis', i:'40(3), 381&ndash;404'},
  {y:2021, tags:['bd'], pdf:'#', a:'From, S. G., &amp; <b>Ratnasingam, S.</b>', t:'Some New Bounds for Moment Generating Functions of Various Life Distributions Using Mean Residual Life Functions', v:'Journal of Statistical Theory and Practice', i:'15(2), 1&ndash;14'},
  {y:2021, tags:['cp','inf'], pdf:'#', a:'<b>Ratnasingam, S.</b>, &amp; Ning, W.', t:'Modified Information Criterion for Regular Change Point Models Based on Confidence Distribution', v:'Environmental and Ecological Statistics', i:'28(2), 303&ndash;322'},
  {y:2021, tags:['cp','seq','hd'], pdf:'#', a:'<b>Ratnasingam, S.</b>, &amp; Ning, W.', t:'Sequential Change Point Detection for High-Dimensional Data Using Nonconvex Penalized Quantile Regression', v:'Biometrical Journal', i:'63(3), 575&ndash;598'},
  {y:2020, tags:['inf'], pdf:'#', a:'<b>Ratnasingam, S.</b>, &amp; Ning, W.', t:'Statistical Inference for the Lomax-Linear Failure Rate Distribution', v:'Far East Journal of Theoretical Statistics', i:'59(1), 35&ndash;58'},
  {y:2020, tags:['cp','inf'], pdf:'#', a:'<b>Ratnasingam, S.</b>, &amp; Ning, W.', t:'Confidence Distributions for Skew Normal Change Point Model Based on Modified Information Criterion', v:'Journal of Statistical Theory and Practice', i:'14(3), 1&ndash;21'},
  {y:2016, tags:['bd'], pdf:'#', a:'From, S. G., &amp; <b>Ratnasingam, S.</b>', t:'Some New Refinements of the Arithmetic, Geometric and Harmonic Mean Inequalities with Applications', v:'Applied Mathematical Sciences', i:'10(52), 2553&ndash;2569'}
];

const list = document.getElementById('pubList');
const countEl = document.getElementById('count');
const total = PUBS.length;

PUBS.forEach((p, idx) => {
  const li = document.createElement('li');
  li.className = 'pub';
  li.dataset.tags = p.tags.join(',');
  const pdfLink = p.pdf ? ` <a class="pdf" href="${p.pdf}">pdf</a>` : '';
  li.innerHTML = `<span class="pub-num">${total - idx})</span>
    <span class="pub-body">${p.a} (${p.y}), ${p.t}, <span class="venue">${p.v}</span> ${p.i}.${pdfLink}</span>`;
  list.appendChild(li);
});

function updateCount(n){
  countEl.textContent = n === total ? `Showing all ${total} publications.` : `Showing ${n} of ${total} publications.`;
}
updateCount(total);

document.getElementById('filters').addEventListener('click', (e) => {
  const btn = e.target.closest('.tag-btn');
  if(!btn) return;
  document.querySelectorAll('.tag-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  const filter = btn.dataset.filter;
  let visible = 0;
  document.querySelectorAll('.pub').forEach(li => {
    const show = filter === 'all' || li.dataset.tags.split(',').includes(filter);
    li.classList.toggle('hidden', !show);
    if(show) visible++;
  });
  updateCount(visible);
});
</script>
