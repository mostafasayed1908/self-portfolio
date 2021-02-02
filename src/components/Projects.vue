<template>
    <div id="projects" class="projects-wrapper">
        <h3>Projects</h3>
        <div class="borderr">
            <div class="border-itself"></div>
        </div>
        <div class="row">
            <Project 
                v-for="proj in projs"
                v-bind:key="proj.id"
                :imgSrc="proj.imgSrc"
                :ptitle="proj.ptitle"
            />

        </div>
    </div>
</template>

<script>
import Project from '@/components/Project'

export default {
    components: {
        Project
    },
    data () {
        return {
            projs: [
            { id: 1, imgSrc: require('../assets/p1.jpeg'), ptitle: 'Kolaso - Modern Multi-Purpose WordPress Theme' },
            { id: 2, imgSrc: require('../assets/p2.jpeg'), ptitle: 'CardX - Modern Personal Portfolio / CV / vCard / HTML5 Template' },
            { id: 3, imgSrc: require('../assets/p3.jpeg'), ptitle: 'EZMO - Personal Portfolio & Resume HTML5 Template' },
            { id: 4, imgSrc: require('../assets/p4.jpeg'), ptitle: 'Leila - Personal Portfolio Template' },
            { id: 5, imgSrc: require('../assets/p4.jpeg'), ptitle: 'Rivo - Personal Portfolio Template' },
            { id: 6, imgSrc: require('../assets/p3.jpeg'), ptitle: 'Medina - One Page Parallax' },
            { id: 7, imgSrc: require('../assets/p2.jpeg'), ptitle: 'Okis - Personal CV Resume HTML Template' },
            { id: 8, imgSrc: require('../assets/p1.jpeg'), ptitle: 'Miriam - Responsive Personal Template' }
            ]
        }
  },
  props: {
    
  }
}
</script>

<style scoped>
    .projects-wrapper {
        width: 100%;
        padding-top: 57px;
    }
    .projects-wrapper .row{
        margin-left: 0;
        margin-right: 0
    }
    .projects-wrapper h3{
        width: 100%;
        text-align: center;
        color: #646464;
        font-weight: normal;
    }
    .projects-wrapper .row > div{
        padding: 0
    }
    .project-container {
        overflow: hidden;
    }
    .borderr {
        width: 100%;
        text-align: center;
        margin-bottom: 20px;
    }
    .borderr .border-itself {
        width: 50px;
        border-top: solid black 5px;
        display: inline-block;
    }
</style>
