---
title: grid-template-areas
slug: Web/CSS/grid-template-areas
tags:
  - CSS
  - CSS 属性
  - CSS 布局
  - CSS 网格
translation_of: Web/CSS/grid-template-areas
---
<p><strong><code>grid-template-areas</code></strong> CSS 属性是网格区域 {{glossary("grid areas")}} 在 CSS 中的特定命名。</p>

<div>{{EmbedInteractiveExample("pages/css/grid-template-areas.html")}}</div>

<p>网格区块 (grid areas) 和网格项 (grid item) 沒有关联，但是它们可以和一些网格定位属性 (grid-placement properties) 关联起来，比如{{cssxref("grid-row-start")}}， {{cssxref("grid-row-end")}}， {{cssxref("grid-column-start")}}和{{cssxref("grid-column-end")}}；也可以和一些速记 (shorthands) 属性关联起来，比如{{cssxref("grid-row")}}，{{cssxref("grid-column")}} 和 {{cssxref("grid-area")}}。</p>

<h2 id="Syntax语法">Syntax[语法]</h2>

<pre class="brush: css no-line-numbers">/* Keyword value */
grid-template-areas: none;

/* &lt;string&gt; values */
grid-template-areas: "a b"; /* 一行 两列 */
grid-template-areas: "a b b"
                     "a c d"; /* 两行 三列 */

/* Global values */
grid-template-areas: inherit; /* 继承 */
grid-template-areas: initial; /* 默认值 */
grid-template-areas: unset; /* 未设置 */
</pre>

<h3 id="Values可选值"> Values[可选值]</h3>

<dl>
 <dt><code>none</code></dt>
 <dd>网格容器没有定义任何的网格区块 (grid areas)。</dd>
 <dt><code>{{cssxref("&lt;string&gt;")}}+</code></dt>
 <dd>每一个给定的字符串会生成一行，一个字符串中用空格分隔的每一个单元 (cell) 会生成一列。多个同名的，跨越相邻行或列的单元称为网格区块 (grid area)。非矩形的网格区块是无效的。</dd>
</dl>

<h3 id="形式化语法">形式化语法</h3>

{{csssyntax}}

<h2 id="例子">例子</h2>

<h3 id="HTML">HTML</h3>

<pre class="brush: html">&lt;section id="page"&gt;
  &lt;header&gt;Header&lt;/header&gt;
  &lt;nav&gt;Navigation&lt;/nav&gt;
  &lt;main&gt;Main area&lt;/main&gt;
  &lt;footer&gt;Footer&lt;/footer&gt;
&lt;/section&gt;</pre>

<h3 id="CSS">CSS</h3>

<pre class="brush:css; highlight[5-7]">#page {
  display: grid; /* 1.设置 display 为 grid */
  width: 100%;
  height: 250px;
  grid-template-areas: "head head"
                       "nav  main"
                       "nav  foot"; /* 2.区域划分 当前为 三行 两列 */
  grid-template-rows: 50px 1fr 30px; /* 3.各区域 宽高设置 */
  grid-template-columns: 150px 1fr;
}

#page &gt; header {
  grid-area: head; /* 4. 指定当前元素所在的区域位置，从 grid-template-areas 选取值 */
  background-color: #8ca0ff;
}

#page &gt; nav {
  grid-area: nav;
  background-color: #ffa08c;
}

#page &gt; main {
  grid-area: main;
  background-color: #ffff64;
}

#page &gt; footer {
  grid-area: foot;
  background-color: #8cffa0;
}
</pre>

<h3 id="结果">结果</h3>

<p>{{ EmbedLiveSample('例子', '100%', '250px', '', 'Web/CSS/grid-template-areas') }}</p>

<h2 id="规范">规范</h2>

{{Specifications}}

<p>{{cssinfo}}</p>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="See_also">See also</h2>

<ul>
 <li>相关 CSS 属性：{{cssxref("grid-template-rows")}}、{{cssxref("grid-template-columns")}}、{{cssxref("grid-template")}}</li>
 <li>Grid Layout 指南<em>：<a href="/en-US/docs/Web/CSS/CSS_Grid_Layout/Grid_Template_Areas">Grid template areas</a></em></li>
 <li>视频教程<em>：<a href="http://gridbyexample.com/video/grid-template-areas/">Grid Template Areas</a></em></li>
</ul>

<section id="Quick_links">
<ol>
 <li><a href="/en-US/docs/Web/CSS"><strong>CSS</strong></a></li>
 <li><a href="/en-US/docs/Web/CSS/Reference"><strong>CSS Reference</strong></a></li>
 <li><a href="/en-US/docs/Web/CSS/CSS_Grid_Layout">CSS Grid Layout</a></li>
 <li><a href="#"><strong>Guides</strong></a>
  <ol>
   <li><a href="/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout">Basics concepts of grid layout</a></li>
   <li><a href="/en-US/docs/Web/CSS/CSS_Grid_Layout/Relationship_of_Grid_Layout">Relationship to other layout methods</a></li>
   <li><a href="/en-US/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid">Line-based placement</a></li>
   <li><a href="/en-US/docs/Web/CSS/CSS_Grid_Layout/Grid_Template_Areas">Grid template areas</a></li>
   <li><a href="/en-US/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines">Layout using named grid lines</a></li>
   <li><a href="/en-US/docs/Web/CSS/CSS_Grid_Layout/Auto-placement_in_CSS_Grid_Layout">Auto-placement in grid layout</a></li>
   <li><a href="/en-US/docs/Web/CSS/CSS_Grid_Layout/Box_Alignment_in_CSS_Grid_Layout">Box alignment in grid layout</a></li>
   <li><a href="/en-US/docs/Web/CSS/CSS_Grid_Layout/CSS_Grid,_Logical_Values_and_Writing_Modes">Grids, logical values and writing modes</a></li>
   <li><a href="/en-US/docs/Web/CSS/CSS_Grid_Layout/CSS_Grid_Layout_and_Accessibility">CSS Grid Layout and Accessibility</a></li>
   <li><a href="/en-US/docs/Web/CSS/CSS_Grid_Layout/CSS_Grid_and_Progressive_Enhancement">CSS Grid Layout and Progressive Enhancement</a></li>
   <li><a href="/en-US/docs/Web/CSS/CSS_Grid_Layout/Realizing_common_layouts_using_CSS_Grid_Layout">Realizing common layouts using grids</a></li>
  </ol>
 </li>
 <li><a href="#"><strong>Properties</strong></a>
  <ol>
   <li><a href="/en-US/docs/Web/CSS/grid">grid</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-area">grid-area</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-auto-columns">grid-auto-columns</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-auto-flow">grid-auto-flow</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-auto-rows">grid-auto-rows</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-column">grid-column</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-column-end">grid-column-end</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-column-gap">grid-column-gap</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-column-start">grid-column-start</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-gap">grid-gap</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-row">grid-row</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-row-end">grid-row-end</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-row-gap">grid-row-gap</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-row-start">grid-row-start</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-template">grid-template</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-template-areas">grid-template-areas</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-template-columns">grid-template-columns</a></li>
   <li><a href="/en-US/docs/Web/CSS/grid-template-rows">grid-template-rows</a></li>
  </ol>
 </li>
 <li><a href="#"><strong>Glossary</strong></a>
  <ol>
   <li><a href="/en-US/docs/Glossary/Grid_lines">Grid lines</a></li>
   <li><a href="/en-US/docs/Glossary/Grid_tracks">Grid tracks</a></li>
   <li><a href="/en-US/docs/Glossary/Grid_cell">Grid cell</a></li>
   <li><a href="/en-US/docs/Glossary/Grid_areas">Grid areas</a></li>
   <li><a href="/en-US/docs/Glossary/Gutters">Gutters</a></li>
   <li><a href="/en-US/docs/Glossary/Grid_rows">Grid row</a></li>
   <li><a href="/en-US/docs/Glossary/Grid_column">Grid column</a></li>
  </ol>
 </li>
</ol>
</section>