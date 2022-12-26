<script setup>
import imageSlider from '../components/imageSlider.vue'
import projects from '../components/projects.vue'


</script>
<template>
  <div class="about">
    <div id="aboutHeroSec">
      <div id="aboutHeroItems1">
        <span id="heroKeyword">Founder of Aurum</span>
        <span id="heroHead"><span>Hi,<br>I'm </span><span class="Prajwol">Prajwol</span>.</span>
      </div>
      <div id="aboutHeroItems2"><img src="../assets/images/Screenshot_20221121_122752.png" alt="a picture of me"></div>
    </div>
    <div class="strike1"></div>
    <div id="content1" class="contclass">
      <div class="contentItem" id="content1Itemimg"><img src="../assets/images/Screenshot_20221121_122121.png" alt=""></div>
      <div class="contentItem" id="content1Itemdesc"><span id="content1Itemdesc1">I'm a Front-end Web Developer and UI designer. I love to build websites that are full of creativity and aesthetically pleasing.</span></div>
    </div>
    <div class="strike1"></div>
    <div class="gap"></div>
    <div class="strike2"></div>
    <div id="content2" class="contclass">
      <div class="contentItem" id="content2Itemdesc"><span id="content1Itemdesc1">I am Fluent in Front-end Technologies such as HTML, CSS, JavaScript. And I am also Good t using Frameworks such as TailwindCSS and Vue.js for CSS and JavaScript respectively.</span></div>
      <div class="contentItem" id="content2Itemimg">
        <div class="techLogos"><img src="../assets/images/HTML.svg" alt="HTML Logo"></div>
        <div class="techLogos"><img src="../assets/images/CSS.svg" alt="CSS Logo"></div>
        <div class="techLogos"><img src="../assets/images/JS.svg" alt="JS Logo"></div>
        <div class="techLogos"><img src="../assets/images/Tailwind.svg" alt="TailwindCSS Logo"></div>
        <div class="techLogos"><img src="../assets/logo.svg" alt="Vue Logo"></div>
        <div class="techLogos">Coming<br>soon</div>
      </div>
    </div>
    <imageSlider></imageSlider>
    <div class="strike2"></div>
    <div class="gap"></div>
    <div class="strike1"></div>
    <projects></projects>
    <div class="strike1"></div>
  </div>
</template>

<style>
.about{
  font-size:16px;
  margin:2em 0;
  overflow:visible;
}
#aboutHeroSec{
  display: flex;
  justify-content:space-between;
  align-items:space-between;
  flex-direction:row;
  width:100%;
  margin:5rem 0 0 0;
  padding-bottom:12em;
  overflow: visible;
}
.Prajwol{
  width:auto;
  overflow:visible;
  padding:0 0 1.5em 0 ;
}
#aboutHeroItems1{
  display:flex;
  justify-content:space-between;
  align-items:flex-start;
  flex-direction:column;
  height:20em;
 overflow: visible;
}
#aboutHeroItems2{
  margin-top:2.5em;
  display:flex;
  justify-content:flex-end;
  align-items:center;
  flex-direction:column;
  background: linear-gradient(0deg, #ff8fcd, #c7fcff, #94f3ff, #b8ffbc);
  box-shadow: 48px 32px 48px 10px rgba( 31, 38, 135, 0.37 );
  backdrop-filter: blur( 8px );
  -webkit-backdrop-filter: blur( 8px );
  border-radius: 10px;
  border: 0px solid rgba( 255, 255, 255, 0.18 );
  transform: rotateX(20deg) rotateY(30deg);
  overflow:visible;
  box-sizing: content-box;
}
#aboutHeroItems2>img{
  width:20em;
  padding:0.1em;
  border-radius: 10px;
  transform: translateX(-12.5px) translatey(7.5px);
}
#heroKeyword{
  margin:0em 0 0 0;
  font-family:'Montserrat';
  font-weight:400;
  font-size: 1.5em;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  color:rgba(240, 248, 255, 0.087);
}
#heroHead{
  height:auto;
  text-align: left;
  font-weight:700;
  font-size: 6.5em;
  padding:0rem 0 2rem 0;
  font-family:'Kaushan Script';
  background: -webkit-linear-gradient(0deg, #ccbdff, #c7f9ff, #8d85ff, #ffbdc6);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  overflow: visible;
}
#content1,#content2{
  display: flex;
  flex-direction:row;
  align-items: center;
  justify-content: space-between;
}
#content2{
  display: flex;
  flex-direction:row;
  align-items:center;
  justify-content: space-between;
}
#content1Itemimg>img{
  height:17.5em;
  aspect-ratio: auto;
  border-radius:2em;
  transform: translateY(10px) translateX(12.5px);
}
#content2Itemimg>img{
  aspect-ratio: auto;
  height:17.5em;
  width:100%;
  border-radius:2em;
  transform: translateY(10px) translateX(-12.5px);
}
#content1Itemimg{
  width:auto;
  background: linear-gradient(25deg, #ff8fcd, #c7fcff, #94f3ff, #b8ffbc);
  box-shadow: -48px 32px 48px 10px rgba( 31, 38, 135, 0.37 );
  backdrop-filter: blur( 8px );
  -webkit-backdrop-filter: blur( 8px );
  border-radius: 2em;
  border: 0px solid rgba( 255, 255, 255, 0.18 );
  transform: rotateX(25deg) rotateY(-30deg);
}
#content2Itemimg{
  display:grid;
  grid-template-columns: 5em 5em 5em;
  grid-template-rows: 5em 5em;
  grid-gap: 1em;
  width:auto;
}
.techLogos{
  padding:0.5em;
  background:linear-gradient(45deg,#2DC1E4, #E8ECC7);
  /*linear-gradient(45deg, rgb(204, 189, 255), rgb(199, 249, 255), rgb(141, 133, 255), rgb(255, 189, 198))*/
  box-shadow: 10px 10px 10px 3px rgba( 31, 38, 135, 0.37 );
  backdrop-filter: blur( 8px );
  -webkit-backdrop-filter: blur( 8px );
  border-radius: 0.5em;
  border: 0px solid rgba( 255, 255, 255, 0.18 );
  overflow:hidden;
  transition:transform 2s ease-in-out;
}
.techLogos:hover{
  transform: rotateX(25deg) rotateY(360deg) rotatez(25deg);
  transition:transform 1s ease-in-out;
}
.techLogos>img{
  aspect-ratio: 1/1;
  height:4em;
  -webkit-text-stroke: black 1px;
}
.techLogos:last-of-type{
  color:black;
  display:flex;
  flex-direction: column;
  justify-content: center;
  text-align:center;
  font-weight:bold;
}
#content1Itemdesc{
  width:40%;
  padding: 0 0 1rem 5rem;
  font-size:1.5em;
  text-align: right;
}
#content2Itemdesc{
  width:40%;
  padding: 4rem 5rem 4rem 0rem;
  font-size:1.5em;
  text-align: left;
}
#content1Itemdesc::before{
  content: 'About Me';
  padding: 1.5em 0;
  display:block;
  color: rgb(255, 255, 255, 0.2);
}
#content2Itemdesc::before{
  content: 'Skillset';
  padding: 1.5em 0;
  display:block;
  color: rgb(255, 255, 255, 0.2);
}
#content1Itemdesc>span{
  background:linear-gradient(45deg, #ff8fcd, #c7fcff, #94f3ff, #b8ffbc);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
}
#content2Itemdesc>span{
  background:linear-gradient(45deg, #ccbdff, #c7f9ff, #8d85ff, #ffbdc6);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
}
.strike1{
  width:95vw;
  background: linear-gradient(90deg, #ccbdff, #c7f9ff, #8d85ff, #ffbdc6);
  border-radius: 50em;
  height: 0.175em;
  margin:0 -8vw;
}
.strike2{
  width:95vw;
  background: linear-gradient(90deg, #9effe1, #a8c5ff, #ccedff, #cabdff );
  border-radius: 50em;
  height: 0.175em;
  margin:0 -8vw;
}
.gap{
  width:100%;
  padding: 2.5em 0;
}
@media screen and (max-width:1024px){
  .about{
    font-size:10px;
  }
  .strike1,.strike2{
    margin:-1em;
  }

  #content1,#content2,#aboutHeroSec{
    display:flex;
    flex-direction:column;
  }
  #content1Itemdesc, #content2Itemdesc{
    font-size:3em;
  }
  #content2Itemimg{
    font-size:2em;
  }
  #content1Itemdesc, #content2Itemdesc{
    width:80vw;
    padding:1em;
  }
}
</style>
