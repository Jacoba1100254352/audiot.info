<template>
  <div id="app">
    <!------------
		-   Header   -
		------------->

    <header class="section_1" id="header">
      <img
        src="../public/Images/audiot logo 1.png"
        alt="AudioT Logo"
        id="Logo"
      />

      <h1 id="AudioT_name_plate">AudioT</h1>

      <nav class="all_caps" id="main_nav">
        <ul class="semantic_list">
          <!-- <li><a href="index.html">Home</a></li> -->
          <li><a href="#welcome">Welcome</a></li>
          <li><a href="#news">News</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>

    <!-----------------
    -   Router View   -
    ------------------>

    <router-view />

    <!------------
    -   Footer   -
    ------------->

    <footer class="section_3">
      <div class="footer_content_nav">
        <h2><!-- Contents --></h2>
        <nav class="footer_nav">
          <ul class="semantic_list">
            <!-- 						<li><a href="#welcome">Welcome</a></li></li>
						<li><a href="#news">News</a></li>
						<li><a href="#projects">Projects</a></li>
						<li><a href="#contact">Contact</a></li> -->
          </ul>
        </nav>
      </div>

      <div class="footer_courses_sub_nav">
        <br />
        <h2>AudioT.ai</h2>
        <br />
        <nav class="footer_nav">
          <ul class="semantic_list">
            <li>Atlanta, GA, USA</li>
            <li>©2020 AudioT. All rights reserved.</li>
          </ul>
        </nav>
      </div>

      <div class="footer_resources_nav">
        <h2><!-- Header 3 --></h2>
        <nav class="footer_nav">
          <ul class="semantic_list">
            <li><a href="#"></a></li>
          </ul>
        </nav>
      </div>
    </footer>
  </div>
</template>

<style>
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed,
figure, figcaption, footer, header, hgroup,
menu, nav, output, ruby, section, summary,
time, mark, audio, video /* eslint-disable-line */ {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure,
footer, header, hgroup, menu, nav, section /* eslint-disable-line */ {
  display: block;
}
body {
  line-height: 1;
}
ol,
ul {
  list-style: none;
}
blockquote,
q {
  quotes: none;
}
blockquote:before,
blockquote:after,
q:before,
q:after {
  content: "";
  content: none;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}

/**************
*   General   *
**************/

/* Responsive layout - when the screen is less than 700px wide, make the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 700px) {
  body {
    background-size: 600px;
    background-position: top left;
  }
  :root {
    --size_adjustment: 1;
  }
}

* {
  box-sizing: border-box;
}

html {
  min-height: 100%;
  /* min-width: 100%; */
  width: 90em;
}

body {
  /* background-image: linear-gradient( rgb( 165, 165, 165), rgb( 160, 160, 160)); */
  /* background-color: white; */
  position: relative;
  min-width: 960px;

  background-color: rgb(227, 226, 224);
  font-family: sans-serif;
  --size_adjustment: 1;
  --header_height: calc(200px * var(--size_adjustment));
  --name_plate_height: calc(2.5 * var(--size_adjustment));
  --nav_height: calc((50 / 12) * var(--size_adjustment));

  min-width: 700px;
  max-width: 1800px;
  max-height: 720px;
}

.flexbox_container {
  display: flex;
  justify-content: space-between;
  flex-flow: row wrap;
}

.all_caps {
  text-transform: uppercase;
}

/**************
*   Heading   *
**************/

/* alt text and link styler */
header img,
a,
#AudioT_name_plate {
  color: black;
  text-decoration: none;
}

header {
  background-color: rgb(204, 188, 157);
  background-position: left;
  font-family: Tahoma, Arial, sans-serif;
}

header,
header img {
  height: var(--header_height);
}

/*  */
header img {
  /*background-image: url("../../Images/Chicken-farm-3.jpg");*/
  background-repeat: no-repeat;
  background-size: 100% 100%;
  width: 30%;
  float: left;
}

#AudioT_name_plate,
#main_nav {
  display: inline-block;
  width: 70%;
  height: 50%;
  text-align: center;
  float: right;
}

#AudioT_name_plate {
  line-height: var(--name_plate_height);
  font-size: 50px;
}

#main_nav {
  font-size: 23px;
}

#main_nav > ul > li {
  width: 25%;
  line-height: var(--nav_height); /* Changes the box height!!! */
  white-space: nowrap;
  float: left;
}

#main_nav a {
  display: block;
  transition-duration: 0.5s;
  transition-delay: 0s;
  transition-timing-function: ease;
}
#main_nav a:link,
#main_nav a:visited,
#main_nav a:focus {
  /* background: rgb( 80, 81, 79 ); */
}
#main_nav a:hover {
  transform: scale(1.1, 1.1); /* background: rgb( 39, 45, 45 ); */
}
/* #main_nav a:active{ background: rgb( 39, 45, 45 ); } */

/*** Sub Menu ***/

nav li ul {
  position: absolute;
  display: none;
  padding-top: 1px;
  width: 14%; /*As a default*/
  width: calc(14% + 1px);
  transform: translateX(-1px);
}

nav li:hover ul {
  display: block;
  z-index: 1;
}

nav li ul li {
  border: 1px solid black;
  border-top: none;
  clear: both;
}

/**************
*   Section   *
**************/

section {
  margin: 1rem;
  margin-bottom: 2%;
  height: 30.5rem;
  /*min-height: 30.5rem;*/
  min-width: 640px;
  height: auto;
}
section > div.flexbox_container li {
  padding: 2.5px;
  padding-left: 40px;
}

h2 {
  font-size: 20px;
  text-align: center;
}
h3 {
  font-size: 19px;
  text-align: center;
}
h4 {
  text-align: left;
  font-weight: bold;
}
p {
  text-align: justify;
}

/*****************
*   Navigation   *
*****************/

nav.local {
  position: relative;
  margin-top: 2%;
}
nav.local li {
  width: calc(100% / 8);
}
nav.local a {
  color: black;
  display: block;
  padding: 3%;
}

ul.flexbox_container {
  flex-wrap: nowrap;
}
li.pseudo_element {
  outline: 1px solid;
} /* had a background color, why? */
#pseudo_list li {
  min-width: 80px;
}
#pseudo_list {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
}
#real_list,
#real_list li {
  text-align: center;
  align-items: center;
  z-index: 1;
}

/************
*   Aside   *
************/

aside,
article {
  margin-top: 2%;
  padding: 15px;
  /* background-color: rgb( 227, 226, 224); */
  background-color: white;
}

/* aside h2{ font-weight: bold; } */

/**************
*   Article   *
**************/

article {
  width: 100%;
} /* 49% to be on top of eachother */
article li {
  list-style-position: inside;
}
article > ul {
  list-style-type: disc;
}
section.index_section article a {
  color: black;
  text-decoration: none;
}

/*   ECE 6254 Specifications   */

section > div > div {
  order: 8;
  margin-top: 1.1%;
  width: 49%;
}
section > div > div > article {
  width: 100%;
}
article.article_exam {
  margin-top: 4.2%; /*align-self: flex-end;*/
}
article.article_homework ul ul li {
  padding-left: 100px;
}
article.article_homework > ul > li {
  list-style-type: none;
}
/*article.article_schedule>ul{ font-weight: bold; }*/

span.red {
  color: rgb(220, 25, 0);
}

/*************
*   Footer   *
*************/

footer {
  display: flex;
  position: fixed;
  bottom: 0;
  color: white;
  flex-flow: row nowrap;
  padding-top: 10px;
  text-align: center;
  height: 6rem;
  width: 100%;
  min-width: 43.75rem;
  background-color: rgb(160, 160, 160);
}

footer div {
  width: calc(100% / 3);
}

footer h2 {
  text-transform: uppercase;
  font-size: 19px;
  letter-spacing: 2px;
  font-family: Trebuchet, Trebuchet MS, Tahoma, Arial, sans-serif;
}

footer li {
  font-size: 12px;
}
</style>
