# Basic-Calculator-with-React
Basic Calculator with React

<body id="the-body" style="border: 1px solid #555555; --borderWidth: 1px;" class="codepen-embed-body static results-active" data-new-gr-c-s-check-loaded="14.1119.0" data-gr-ext-installed="" data-new-gr-c-s-loaded="14.1119.0">
<nav class="embed-nav group" id="embed-nav">
<ul class="code-types">
<li class="code-type">
<a id="html-link" href="#html-box" role="button" aria-pressed="false">
HTML
</a>
</li>
<li class="code-type">
<a id="css-link" href="#css-box" role="button" aria-pressed="false">
CSS
</a>
</li>
<li class="code-type">
<a id="js-link" href="#js-box" role="button" aria-pressed="false">
Babel
</a>
</li>
</ul>
<ul class="result-button-list">
<li class="results results-type">
<a id="result-link" href="#result-box" class="active" aria-pressed="true" role="button">
Result
</a>
</li>
<li>
<a href="#resources-link" id="skip-results-iframe-link">Skip Results Iframe</a>
</li>
</ul>
<div class="logo-wrap" id="edit-area">
<a class="edit-on-codepen" target="_blank" rel="noopener" href="https://codepen.io/asmnajmussakibkhan/pen/KKrjLWO" title="Edit on CodePen">
<div class="large-logo">
<span id="edit-on-text" class="open-on">EDIT ON</span>
<svg id="embed-codepen-logo" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 138 26" fill="none" stroke="#000" stroke-width="2.3" stroke-linecap="round" stroke-linejoin="round" role="img" aria-label="CodePen">
<path d="M80 6h-9v14h9m34-14h-9v14h9m-3-7h-6m-28 0h-6m51 7V6l11 14V6M22 16.7L33 24l11-7.3V9.3L33 2 22 9.3v7.4zm22 0L33 9.3l-11 7.4m0-7.4l11 7.3 11-7.3M33 2v7.3m0 7.4V24m55-10h6c2.2 0 4-1.8 4-4s-1.8-4-4-4h-6v14M15 8c-1.3-1.3-3-2-5-2-4 0-7 3-7 7s3 7 7 7c2 0 3.7-.8 5-2m49-5c0 4-3 7-7 7h-5V6h5c4 0 7 3 7 7z"></path>
</svg>
</div>
<div class="box-logo">
<svg xmlns="http://www.w3.org/2000/svg" viewBox="20 0 26 26" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2.3" role="img" aria-label="Edit on CodePen">
<path id="icon-codepen-box" d="M22 16.7L33 24l11-7.3V9.3L33 2 22 9.3v7.4zm22 0L33 9.3l-11 7.4m0-7.4l11 7.3 11-7.3M33 2v7.3m0 7.4V24"></path>
</svg>
</div>
</a>
</div>
</nav>
<div id="output" data-border-style="thin" data-header="true">
<div id="html-box" class="code-wrap code-box box " role="region" aria-label="HTML">
<pre tabindex="0"><code data-lang="htmlmixed" id="actual-html-code" class=" cm-s-default"><span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">div</span> <span class="cm-attribute">id</span>=<span class="cm-string">"root"</span><span class="cm-tag cm-bracket">&gt;</span><span class="cm-tag cm-bracket">&lt;/</span><span class="cm-tag">div</span><span class="cm-tag cm-bracket">&gt;</span></code></pre>
</div>
<div id="css-box" class="code-wrap code-box box " role="region" aria-label="CSS">
<pre tabindex="0"><code data-lang="css" id="actual-css-code" class=" cm-s-default"><span class="cm-qualifier">.app-container</span> {
   <span class="cm-property">width</span>: <span class="cm-number">400px</span>;
   <span class="cm-property">height</span>: <span class="cm-number">400px</span>;
}
<span class="cm-qualifier">.calculator</span> {
   <span class="cm-property">display</span>: <span class="cm-atom">grid</span>;
   <span class="cm-property">grid-template-columns</span>: <span class="cm-variable cm-callee">repeat</span>(<span class="cm-number">4</span>, <span class="cm-number">100px</span>);
}
<span class="cm-qualifier">.display</span> {
   <span class="cm-property">grid-column-start</span>: <span class="cm-number">1</span>;
   <span class="cm-property">grid-column-end</span>: <span class="cm-number">5</span>;
   <span class="cm-property">height</span>: <span class="cm-number">60px</span>;
   <span class="cm-property">font-size</span>: <span class="cm-number">30px</span>;
   <span class="cm-property">text-align</span>: <span class="cm-atom">right</span>;
   <span class="cm-property">border</span>: <span class="cm-number">1px</span> <span class="cm-atom">solid</span> <span class="cm-keyword">black</span>;
   <span class="cm-property">padding-right</span>: <span class="cm-number">10px</span>;
   <span class="cm-property">padding-top</span>: <span class="cm-number">10px</span>;
}
<span class="cm-tag">button</span> {
   <span class="cm-property">height</span>: <span class="cm-number">60px</span>;
   <span class="cm-property">background-color</span>: <span class="cm-keyword">white</span>;
   <span class="cm-property">border</span>: <span class="cm-number">1px</span> <span class="cm-atom">solid</span> <span class="cm-keyword">lightgray</span>;
   <span class="cm-property">font-size</span>: <span class="cm-number">25px</span>;
}
<span class="cm-tag">button</span><span class="cm-qualifier">.operator</span> {
   <span class="cm-property">background-color</span>: <span class="cm-keyword">lightgray</span>;
}</code></pre>
</div>
<div id="js-box" class="code-wrap code-box box " role="region" aria-label="JS">
<pre tabindex="0"><code data-lang="jsx" id="actual-js-code" class=" cm-s-default"><span class="cm-keyword">function</span> <span class="cm-def">Calculator</span>() {
    <span class="cm-keyword">const</span> [<span class="cm-def">calc</span>, <span class="cm-def">setCalc</span>] <span class="cm-operator">=</span> <span class="cm-variable">React</span>.<span class="cm-property">useState</span>({
        <span class="cm-property">current</span>: <span class="cm-string">"0"</span>,
        <span class="cm-property">total</span>: <span class="cm-string">"0"</span>,
        <span class="cm-property">isInitial</span>: <span class="cm-atom">true</span>,
        <span class="cm-property">preOp</span>: <span class="cm-string">""</span>
    });
    <span class="cm-keyword">function</span> <span class="cm-def">handleNumber</span>(<span class="cm-def">value</span>) {
    <span class="cm-keyword">let</span> <span class="cm-def">newValue</span> <span class="cm-operator">=</span> <span class="cm-variable-2">value</span>;
    <span class="cm-keyword">if</span> (<span class="cm-operator">!</span><span class="cm-variable-2">calc</span>.<span class="cm-property">isInitial</span>) {
       <span class="cm-variable-2">newValue</span> <span class="cm-operator">=</span> <span class="cm-variable-2">calc</span>.<span class="cm-property">current</span> <span class="cm-operator">+</span> <span class="cm-variable-2">value</span>;
    }
        <span class="cm-variable-2">setCalc</span>({<span class="cm-property">current</span>: <span class="cm-variable-2">newValue</span>, <span class="cm-property">total</span>: <span class="cm-variable-2">calc</span>.<span class="cm-property">total</span>, <span class="cm-property">isInitial</span>: <span class="cm-atom">false</span>, <span class="cm-property">preOp</span>: <span class="cm-variable-2">calc</span>.<span class="cm-property">preOp</span>});
    }
    <span class="cm-keyword">function</span> <span class="cm-def">handleOperator</span>(<span class="cm-def">value</span>) {
        <span class="cm-keyword">const</span> <span class="cm-def">total</span> <span class="cm-operator">=</span> <span class="cm-variable">doCalculation</span>();
        <span class="cm-variable-2">setCalc</span>({<span class="cm-property">current</span>: <span class="cm-variable-2">total</span>.<span class="cm-property">toString</span>(), <span class="cm-property">total</span>: <span class="cm-variable-2">total</span>.<span class="cm-property">toString</span>(), <span class="cm-property">isInitial</span>: <span class="cm-atom">true</span>, <span class="cm-property">preOp</span>: <span class="cm-variable-2">value</span>});
   }
    <span class="cm-keyword">function</span> <span class="cm-def">doCalculation</span>() {
        <span class="cm-keyword">let</span> <span class="cm-def">total</span> <span class="cm-operator">=</span> <span class="cm-variable">parseInt</span>(<span class="cm-variable-2">calc</span>.<span class="cm-property">total</span>);
 
    <span class="cm-keyword">switch</span>(<span class="cm-variable-2">calc</span>.<span class="cm-property">preOp</span>) {
        <span class="cm-keyword">case</span> <span class="cm-string">"+"</span>:
            <span class="cm-variable-2">total</span> <span class="cm-operator">+=</span> <span class="cm-variable">parseInt</span>(<span class="cm-variable-2">calc</span>.<span class="cm-property">current</span>);        
            <span class="cm-keyword">break</span>;
        <span class="cm-keyword">case</span> <span class="cm-string">"-"</span>:
            <span class="cm-variable-2">total</span> <span class="cm-operator">-=</span> <span class="cm-variable">parseInt</span>(<span class="cm-variable-2">calc</span>.<span class="cm-property">current</span>); 
            <span class="cm-keyword">break</span>;
        <span class="cm-keyword">case</span> <span class="cm-string">"*"</span>:
            <span class="cm-variable-2">total</span> <span class="cm-operator">*=</span> <span class="cm-variable">parseInt</span>(<span class="cm-variable-2">calc</span>.<span class="cm-property">current</span>); 
            <span class="cm-keyword">break</span>;
        <span class="cm-keyword">case</span> <span class="cm-string">"/"</span>:
            <span class="cm-variable-2">total</span> <span class="cm-operator">/=</span> <span class="cm-variable">parseInt</span>(<span class="cm-variable-2">calc</span>.<span class="cm-property">current</span>); 
            <span class="cm-keyword">break</span>;
        <span class="cm-keyword">default</span>:
            <span class="cm-variable-2">total</span> <span class="cm-operator">=</span> <span class="cm-variable">parseInt</span>(<span class="cm-variable-2">calc</span>.<span class="cm-property">current</span>);
    }
    <span class="cm-keyword">return</span> <span class="cm-variable-2">total</span>;
    }
    <span class="cm-keyword">function</span> <span class="cm-def">renderDisplay</span> () {
        <span class="cm-keyword">return</span> <span class="cm-variable-2">calc</span>.<span class="cm-property">current</span>;
    }
    <span class="cm-keyword">function</span> <span class="cm-def">handleClear</span>() {
        <span class="cm-variable-2">setCalc</span>({
            <span class="cm-property">current</span>: <span class="cm-string">"0"</span>,
            <span class="cm-property">total</span>: <span class="cm-string">"0"</span>,
            <span class="cm-property">isInitial</span>: <span class="cm-atom">true</span>,
            <span class="cm-property">preOp</span>: <span class="cm-string">""</span>
        });
    }
    <span class="cm-keyword">return</span> (
        <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">div</span> <span class="cm-attribute">className</span>=<span class="cm-string">"calculator"</span><span class="cm-tag cm-bracket">&gt;</span>
        <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">div</span> <span class="cm-attribute">className</span>=<span class="cm-string">"display"</span><span class="cm-tag cm-bracket">&gt;</span>{<span class="cm-variable">renderDisplay</span>()}<span class="cm-tag cm-bracket">&lt;/</span><span class="cm-tag">div</span><span class="cm-tag cm-bracket">&gt;</span>
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">value</span>=<span class="cm-string">"7"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleNumber</span>}<span class="cm-tag cm-bracket">/&gt;</span>
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">value</span>=<span class="cm-string">"8"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleNumber</span>}<span class="cm-tag cm-bracket">/&gt;</span>
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">value</span>=<span class="cm-string">"9"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleNumber</span>}<span class="cm-tag cm-bracket">/&gt;</span>
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">className</span>=<span class="cm-string">"operator"</span> <span class="cm-attribute">value</span>=<span class="cm-string">"/"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleOperator</span>}<span class="cm-tag cm-bracket">/&gt;</span>
       
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">value</span>=<span class="cm-string">"4"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleNumber</span>}<span class="cm-tag cm-bracket">/&gt;</span>
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">value</span>=<span class="cm-string">"5"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleNumber</span>}<span class="cm-tag cm-bracket">/&gt;</span>
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">value</span>=<span class="cm-string">"6"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleNumber</span>}<span class="cm-tag cm-bracket">/&gt;</span>
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">className</span>=<span class="cm-string">"operator"</span> <span class="cm-attribute">value</span>=<span class="cm-string">"*"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleOperator</span>}<span class="cm-tag cm-bracket">/&gt;</span>
       
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">value</span>=<span class="cm-string">"1"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleNumber</span>}<span class="cm-tag cm-bracket">/&gt;</span>
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">value</span>=<span class="cm-string">"2"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleNumber</span>}<span class="cm-tag cm-bracket">/&gt;</span>
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">value</span>=<span class="cm-string">"3"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleNumber</span>}<span class="cm-tag cm-bracket">/&gt;</span>
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">className</span>=<span class="cm-string">"operator"</span> <span class="cm-attribute">value</span>=<span class="cm-string">"-"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleOperator</span>}<span class="cm-tag cm-bracket">/&gt;</span>
            
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">value</span>=<span class="cm-string">"C"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleClear</span>}<span class="cm-tag cm-bracket">/&gt;</span>
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">value</span>=<span class="cm-string">"0"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleNumber</span>}<span class="cm-tag cm-bracket">/&gt;</span>
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">value</span>=<span class="cm-string">"="</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleOperator</span>}<span class="cm-tag cm-bracket">/&gt;</span>
            <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">CalcButton</span> <span class="cm-attribute">className</span>=<span class="cm-string">"operator"</span> <span class="cm-attribute">value</span>=<span class="cm-string">"+"</span> <span class="cm-attribute">onClick</span>={<span class="cm-variable">handleOperator</span>}<span class="cm-tag cm-bracket">/&gt;</span>
     <span class="cm-tag cm-bracket">&lt;/</span><span class="cm-tag">div</span><span class="cm-tag cm-bracket">&gt;</span>
    )
}
<span class="cm-keyword">function</span> <span class="cm-def">CalcButton</span>(<span class="cm-def">props</span>) {
    <span class="cm-keyword">return</span> <span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">button</span> <span class="cm-attribute">className</span>={<span class="cm-variable">props</span>.<span class="cm-property">className</span>} <span class="cm-attribute">onClick</span>={() <span class="cm-operator">=&gt;</span> <span class="cm-variable">props</span>.<span class="cm-property">onClick</span>(<span class="cm-variable">props</span>.<span class="cm-property">value</span>)}<span class="cm-tag cm-bracket">&gt;</span>{<span class="cm-variable">props</span>.<span class="cm-property">value</span>}<span class="cm-tag cm-bracket">&lt;/</span><span class="cm-tag">button</span><span class="cm-tag cm-bracket">&gt;</span>
}

<span class="cm-variable">ReactDOM</span>.<span class="cm-property">render</span>(<span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">div</span> <span class="cm-attribute">className</span>=<span class="cm-string">"app-container"</span><span class="cm-tag cm-bracket">&gt;</span><span class="cm-tag cm-bracket">&lt;</span><span class="cm-tag">Calculator</span><span class="cm-tag cm-bracket">/&gt;</span><span class="cm-tag cm-bracket">&lt;/</span><span class="cm-tag">div</span><span class="cm-tag cm-bracket">&gt;</span>, <span class="cm-variable">document</span>.<span class="cm-property">getElementById</span>(<span class="cm-string">"root"</span>));</code></pre>
<a href="#0" id="view-js-compiled-button" class="action-button bottom right view-compiled-button" data-type="js">
View Compiled
</a>
</div>
<div id="result-box" class="code-box active zoom-1" role="region" aria-label="Result">
<iframe allow="accelerometer; camera; encrypted-media; display-capture; geolocation; gyroscope; microphone; midi; clipboard-read; clipboard-write; web-share" allowfullscreen="true" allowpaymentrequest="true" allowtransparency="true" class="result-iframe  " frameborder="0" id="result-iframe" loading="lazy" name="CodePen Preview for Basic Calculator with React" sandbox="allow-forms allow-modals allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-top-navigation-by-user-activation allow-downloads allow-presentation" scrolling="yes" title="CodePen Preview for Basic Calculator with React" data-src="https://cdpn.io/asmnajmussakibkhan/fullembedgrid/KKrjLWO?animations=run&amp;type=embed" src="https://cdpn.io/asmnajmussakibkhan/fullembedgrid/KKrjLWO?animations=run&amp;type=embed">
  </iframe>
</div>
<div id="about-box">
<div class="about-container">
<div class="about-user">
<a href="https://codepen.io/asmnajmussakibkhan" target="_blank" rel="noopener"><img src="https://assets.codepen.io/10444411/internal/avatars/users/default.png?fit=crop&amp;format=auto&amp;height=256&amp;version=1686860341&amp;width=256" loading="lazy" alt="" class="about-image"></a>
<div class="about-user-info">
<p>
This Pen is owned by <a href="https://codepen.io/asmnajmussakibkhan" target="_blank" rel="noopener">ASM Najmus Sakib Khan</a> on <a href="https://codepen.io" target="_blank" rel="noopener">CodePen</a>.
</p>
<p>
<a href="/asmnajmussakibkhan" target="_blank" rel="noopener" class="about-user-more">
See more by @asmnajmussakibkhan on CodePen
</a>
</p>
</div>
</div>
</div>
</div>
<div id="resources-box" class="resources-box">
<h3>External CSS</h3>
<p>
This Pen doesn't use any external CSS resources.
</p>
<h3>External JavaScript</h3>
<ol class="list-of-resources">
<li>
<a href="https://unpkg.com/react@17/umd/react.development.js" target="_blank">https://unpkg.com/react@17/umd/react.development.js</a>
</li>
<li>
<a href="https://unpkg.com/react-dom@17/umd/react-dom.development.js" target="_blank">https://unpkg.com/react-dom@17/umd/react-dom.development.js</a>
</li>
</ol>
</div>
</div>
<footer class="embed-footer" id="embed-footer">
<button id="resources-link" class="resources-link action-button bottom left" href="#resources-box" aria-pressed="false" role="button">
Resources
</button>
<ul class="scaling-choices bottom right">
<li><button class="action-button" id="zoom-button-1">1×</button></li>
<li><button class="action-button" id="zoom-button-05">0.5×</button></li>
<li><button class="action-button" id="zoom-button-025">0.25×</button></li>
</ul>
<button id="rerun-button" class="action-button rerun-button bottom right">
Rerun
</button>
 </footer>
<script nonce="">
    __processedPen = {"html":"&lt;div id=&quot;root&quot;&gt;&lt;/div&gt;","css":".app-container {\n   width: 400px;\n   height: 400px;\n}\n.calculator {\n   display: grid;\n   grid-template-columns: repeat(4, 100px);\n}\n.display {\n   grid-column-start: 1;\n   grid-column-end: 5;\n   height: 60px;\n   font-size: 30px;\n   text-align: right;\n   border: 1px solid black;\n   padding-right: 10px;\n   padding-top: 10px;\n}\nbutton {\n   height: 60px;\n   background-color: white;\n   border: 1px solid lightgray;\n   font-size: 25px;\n}\nbutton.operator {\n   background-color: lightgray;\n}","js":"function Calculator() {\n  const [calc, setCalc] = React.useState({\n    current: &quot;0&quot;,\n    total: &quot;0&quot;,\n    isInitial: true,\n    preOp: &quot;&quot; });\n\n  function handleNumber(value) {\n    let newValue = value;\n    if (!calc.isInitial) {\n      newValue = calc.current + value;\n    }\n    setCalc({ current: newValue, total: calc.total, isInitial: false, preOp: calc.preOp });\n  }\n  function handleOperator(value) {\n    const total = doCalculation();\n    setCalc({ current: total.toString(), total: total.toString(), isInitial: true, preOp: value });\n  }\n  function doCalculation() {\n    let total = parseInt(calc.total);\n\n    switch (calc.preOp) {\n      case &quot;+&quot;:\n        total += parseInt(calc.current);\n        break;\n      case &quot;-&quot;:\n        total -= parseInt(calc.current);\n        break;\n      case &quot;*&quot;:\n        total *= parseInt(calc.current);\n        break;\n      case &quot;/&quot;:\n        total /= parseInt(calc.current);\n        break;\n      default:\n        total = parseInt(calc.current);}\n\n    return total;\n  }\n  function renderDisplay() {\n    return calc.current;\n  }\n  function handleClear() {\n    setCalc({\n      current: &quot;0&quot;,\n      total: &quot;0&quot;,\n      isInitial: true,\n      preOp: &quot;&quot; });\n\n  }\n  return /*#__PURE__*/(\n    React.createElement(&quot;div&quot;, { className: &quot;calculator&quot; }, /*#__PURE__*/\n    React.createElement(&quot;div&quot;, { className: &quot;display&quot; }, renderDisplay()), /*#__PURE__*/\n    React.createElement(CalcButton, { value: &quot;7&quot;, onClick: handleNumber }), /*#__PURE__*/\n    React.createElement(CalcButton, { value: &quot;8&quot;, onClick: handleNumber }), /*#__PURE__*/\n    React.createElement(CalcButton, { value: &quot;9&quot;, onClick: handleNumber }), /*#__PURE__*/\n    React.createElement(CalcButton, { className: &quot;operator&quot;, value: &quot;/&quot;, onClick: handleOperator }), /*#__PURE__*/\n\n    React.createElement(CalcButton, { value: &quot;4&quot;, onClick: handleNumber }), /*#__PURE__*/\n    React.createElement(CalcButton, { value: &quot;5&quot;, onClick: handleNumber }), /*#__PURE__*/\n    React.createElement(CalcButton, { value: &quot;6&quot;, onClick: handleNumber }), /*#__PURE__*/\n    React.createElement(CalcButton, { className: &quot;operator&quot;, value: &quot;*&quot;, onClick: handleOperator }), /*#__PURE__*/\n\n    React.createElement(CalcButton, { value: &quot;1&quot;, onClick: handleNumber }), /*#__PURE__*/\n    React.createElement(CalcButton, { value: &quot;2&quot;, onClick: handleNumber }), /*#__PURE__*/\n    React.createElement(CalcButton, { value: &quot;3&quot;, onClick: handleNumber }), /*#__PURE__*/\n    React.createElement(CalcButton, { className: &quot;operator&quot;, value: &quot;-&quot;, onClick: handleOperator }), /*#__PURE__*/\n\n    React.createElement(CalcButton, { value: &quot;C&quot;, onClick: handleClear }), /*#__PURE__*/\n    React.createElement(CalcButton, { value: &quot;0&quot;, onClick: handleNumber }), /*#__PURE__*/\n    React.createElement(CalcButton, { value: &quot;=&quot;, onClick: handleOperator }), /*#__PURE__*/\n    React.createElement(CalcButton, { className: &quot;operator&quot;, value: &quot;+&quot;, onClick: handleOperator })));\n\n\n}\nfunction CalcButton(props) {\n  return /*#__PURE__*/React.createElement(&quot;button&quot;, { className: props.className, onClick: () =&gt; props.onClick(props.value) }, props.value);\n}\n\nReactDOM.render( /*#__PURE__*/React.createElement(&quot;div&quot;, { className: &quot;app-container&quot; }, /*#__PURE__*/React.createElement(Calculator, null)), document.getElementById(&quot;root&quot;));"};
    __preprocessors = {
      "html": "none",
      "css": "none",
      "js": "babel"
    };
    __preprocessorNames = {
      "html": "HTML",
      "css": "CSS",
      "js": "Babel"
    };
    __editable = false;
    __embed_prefill = false;
  </script>
<script src="https://cpwebassets.codepen.io/assets/embed/embed-008e8e63bc8f4f7a03df3f5da5b5c4d5e25fe5a438f147d0a2325f15fcd47555.js"></script>


</body>
