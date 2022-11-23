<script setup>
import {onMounted, ref, watch } from 'vue'


const slides = [{alt:'Image no. 1', name:'CSS', id:0, src:'dist/assets/CSS.svg'},
                  {alt:'Image no. 2', name:'HTML', id:1, src:'dist/assets/HTML.svg'},
                  {alt:'Image no. 3', name:'JS', id:2, src:'dist/assets/JS.svg'},
                  {alt:'Image no. 4', name:'TW', id:3, src:'dist/assets/Tailwind.svg'},
                  {alt:'Image no. 5', name:'VUE', id:4, src:'dist/assets/logo.svg'}
                  ]
let current = ref(0)
let autoToggle = ref(true)
const auto = setInterval(()=>{
  current.value<(slides.length)-1?
  current.value++
  :current.value=0
}, 4000)

function next(){
  if(current.value<(slides.length)-1){
    current.value++
  }
  else{
    current.value = 0
  }
  console.log('Clicked Next')
  console.log(`index:${current.value}, name:${slides[current.value].name}`)
  clearInterval(auto)
}
function prev(){
  if(current.value>0){
    current.value--
  }
  else{
    current.value = slides.length -1
  }
  console.log('Clicked Previous')
  console.log(`index:${current.value}, name:${slides[current.value].name}`)
  clearInterval(auto)
}
</script>

<template>
  <div id="slider">
    <div class="slide">
      <button @click="prev()">Prev</button>
      <div  v-for="slide in slides"><img v-if="slide.id===current" :src="slide.src" :alt="slide.alt"></div>
      <button @click="next()">Next</button>
    </div>
    <div class="buttonComp">
    </div>
  </div>
</template>

<style scoped>
#slider{
  margin-top: 0rem;
  padding:1rem;
}
.slide{
  padding:1rem;
  display:flex;
  flex-direction:row;
  align-items:center;
  justify-content:center;
}
img{
  padding: 0.5rem;
  aspect-ratio:1/1;
  height:15rem;
  transform:  rotateX(-40deg)
              rotateY(20deg)
              rotateZ(20deg);
  transition: 1s ease-out;
  background: linear-gradient(0deg, #ff8fcd, #c7fcff, #94f3ff, #b8ffbc);
  box-shadow: 48px 32px 48px 10px rgba( 31, 38, 135, 0.37 );
  backdrop-filter: blur( 8px );
  -webkit-backdrop-filter: blur( 8px );
  border-radius: 10px;
  border: 0px solid rgba( 255, 255, 255, 0.18 );
}
img:hover{
  transform:  scale(1.1);
  transition: transform 1s ease-in-out;
}
button{
  width:9rem;
  padding: 0.5rem 1.5rem;
  border-radius: 1.25rem;
  font-size:1.5rem;
  border:solid 0px;
  margin:0 3rem;
  background: linear-gradient(135deg, #ff8fcd, #c7fcff, #94f3ff, #b8ffbc);
  font-family:'Poppins';
  font-weight:bold;
}
.buttonComp{
  padding:1rem;
  display:flex;
  flex-direction:row;
  align-items: center;
  justify-content:center;
}
</style>
