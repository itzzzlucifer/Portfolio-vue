<script setup>
import { ref } from 'vue'
const projects = ref([{ date: '2022/11/20', name: 'Project 1', src: 'src/assets/images/CSS.svg' },
{ date: '2022/11/20', name: 'Project 2', src: 'src/assets/images/HTMl.svg' },
{ date: '2022/11/21', name: 'Project 3', src: 'src/assets/images/JS.svg' },
{ date: '2022/11/22', name: 'Project 4', src: 'src/assets/images/Tailwind.svg' },
{ date: '2022/11/22', name: 'Project 5', src: 'src/assets/images/CSS.svg' },
{ date: '2022/11/23', name: 'Project 6', src: 'src/assets/images/HTML.svg' }
])
</script>

<template>
    <div class="projects">
        <h1>Projects Completed</h1>
        <ul id="projectsList">
            <li v-for="project in projects" class="project">
                <div class="projectHead">
                    <span class="date">{{ project.date }}</span>
                    <button class="projectOptions"><img src="../assets/images/3d.png" alt="options icon"></button>
                </div>
                <div class="projectImg"><img :src="project.src" :alt="project.name"></div>
                <div class="projectContent">
                    <div class="projectTitle">{{ project.name }}</div>
                    <div class="projectDesc">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt velit
                        corrupti nemo facere nostrum voluptatem? Voluptatibus sed ipsa ex nihil doloribus iste vitae
                        iure perspiciatis! </div>
                </div>
                <div class="projectInteractions">
                    <button id="likeBtn">👌</button>
                    <input type="text" placeholder="Type a comment">
                    <button type="submit" id="submitBtn">✅</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<style scoped>
#projectsList {
    display: grid;
    grid-template-columns: repeat(3, 20rem);
    grid-template-rows: repeat(3, auto);
    grid-gap: auto;
}

.projects {
    margin: 5rem 0;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
}

.project {
    width: 16.5rem;
    background-color: azure;
    color: black;
    padding: 1em;
    border-radius: 0.5rem;
    margin: 2em 1em;
    background: -webkit-linear-gradient(135deg, #ff8fcd, #c7fcff, #94f3ff, #b8ffbc);
    box-shadow: 24px 24px 20px 16px rgba(31, 38, 135, 0.322);
    overflow: hidden;
}

.projects>h1:first-of-type {
    font-size: 3rem;
    text-align: center;
    margin: 0 0 2rem 0;
    background: -webkit-linear-gradient(0deg, #ccbdff, #c7f9ff, #8d85ff, #ffbdc6);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    padding: 1em;
}

.projectHead>button>img {
    width: 2rem;
}

.projectOptions {
    border-radius: 0.25rem;
    background-color: honeydew;
    border: solid rgba(0, 0, 0, 0.763) 2px;
    box-shadow: 3.5px 5px 0px 0px rgba(0, 0, 0, 0.571);
}

.projectOptions:active {
    border-radius: 0.25rem;
    border: solid rgba(0, 0, 0, 0.763) 2px;
    background-color: rgb(160, 168, 160);
    box-shadow: 0px 0px 0px 0px rgba(0, 0, 0, 0);
}


.projectHead {
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: rgba(0, 0, 0, 0.55);
}

.projectImg {
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgb(48, 11, 79);
    margin: 1rem 0;
}

.projectImg>img {
    height: 10rem;
}

.projectContent {
    font-family: 'montserrat';
}

.projectTitle {
    font-size: 1.5em;
    font-weight: bold;
    padding: 0.5rem 0;
    font-family: inherit;
}
.projectDesc{
    font-size: 0.9em;
    padding: 0.5rem 0;
    font-family: inherit;
    font-weight: 400;
}
#likeBtn {
    height:2.25em;
    margin-right: 0.5rem;
    background-color: cornflowerblue;
    border: solid rgba(0, 0, 0, 0.763) 2px;
    box-shadow: 3.5px 5px 0px 0px rgba(0, 0, 0, 0.571);
    border-radius: 0.25rem;
    transform: translateY(1px);
}

#likeBtn:active {
    border-radius: 0.25rem;
    border: solid rgba(0, 0, 0, 0.763) 2px;
    background-color: rgb(54, 79, 125);
    box-shadow: 0px 0px 0px 0px rgba(0, 0, 0, 0);
}
.projectInteractions>input{
    height:1.8em;
    margin-right: 0.5rem;
    border: solid rgba(0, 0, 0, 0.763) 2px;
    box-shadow: 3.5px 5px 0px 0px rgba(0, 0, 0, 0.571);
    border-radius: 0.25rem;
    font-family:'Montserrat';
}
#submitBtn{
    margin-right: 0.5rem;
    border: solid rgba(0, 0, 0, 0.763) 2px;
    padding: 0;
    font-size: 1.2rem;
    box-shadow: 3.5px 5px 0px 0px rgba(0, 0, 0, 0.571);
    border-radius: 0.25rem;
    transform:translateY(3.5px);
}
#submitBtn:active{
    border: solid rgba(0, 0, 0, 0.763) 2px;
    box-shadow: 0px 0px 0px 0px rgba(0, 0, 0, 0);
}
/*
@media screen and (orientation:portrait){
    #projectsList{
        display:grid;
        grid-template-columns: repeat(1, auto);
        grid-template-rows: repeat(9, auto);
    }
    .project{
        width:30rem;
        padding: 2rem;
    }
    .projectImg>img{
        height:20rem;
    }
    .projectHead{
        font-size:2rem;
    }
    .projectHead>button>img{
        width:4rem;
        aspect-ratio: 1/1;
    }
    .projectTitle{
        font-size:3rem;
    }
    .projectDesc{
        font-size:1.75rem;
        line-height: 1.35;
    }
    #submitBtn{
        font-size:2em;
    }
}*/
</style>
