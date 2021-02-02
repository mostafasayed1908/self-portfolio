<template>
    <div class="col-lg-3 col-md-4">
        <div @mouseenter="hovered" @mouseleave="unhovered" class="project-container">
            <img :src="imgSrc" class="img-fluid" alt="Responsive image" >
            <div class="hover-div" :class="{hovered : active, unhovered : active == false}" >
                <div class="proj-plus">
                    <ProjectOpenBtn 
                    :ptitle="ptitle"
                    />
                </div>
                <div class="proj-title">{{ptitle}}</div>
            </div>
        </div>
    </div>
</template>

<script>
import ProjectOpenBtn     from   '@/components/ProjectOpenBtn'
/*
<a href=""><i class="fas fa-plus-circle"></i></a>
*/
export default {
    components: {
        ProjectOpenBtn
    },
    data () {
        return {
            active:false,
        }
  },
  props: ['imgSrc','ptitle'],
  methods:{
      hovered: function() {
          this.active = true;
      },
      unhovered: function() {
          this.active = false;
      }
  }
}
</script>

<style scoped>
.project-container {
    position:relative;
}
.hover-div {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;
    background-color: rgb(0, 0, 0);
    opacity: 0.3;
}
a {
    color: #ededed;
}
a:hover {
    color: #a0a0a0 !important;
    text-decoration: none !important;
}
.hovered {
    animation-name: hovered;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
}
@keyframes hovered {
    0%    { opacity: 0.3;}
    100%  { opacity: 0.9;}
}
.unhovered {
    animation-name: unhovered;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
}
@keyframes unhovered {
    0%       { opacity: 0.9;color: rgba(231, 231, 231, 1);}
    100%    { opacity: 0.3;color: rgba(231, 231, 231, 0);}
}
.hovered .proj-title , .hovered .proj-plus{
    animation-name: titleHovered;
    animation-duration: 1500ms;
    animation-fill-mode: forwards;
}
@keyframes titleHovered {
    0%    {color: rgba(231, 231, 231, 0);}
    100%  {color: rgba(231, 231, 231, 1);}
}
.unhovered .proj-title , .unhovered .proj-plus{
    animation-name: titleUnHovered;
    animation-duration: 1500ms;
    animation-fill-mode: forwards;
}
@keyframes titleUnHovered {
    0%  {color: rgba(231, 231, 231, 1);}
    100%    {color: rgba(231, 231, 231, 0);}
}
.hover-div .proj-plus {
    position: absolute;
    width: 100%;
    top: 10px;
    left: 15px;
    font-size: 25px
}
.hover-div .proj-title {
    position: absolute;
    width: 80%;
    bottom: 10px;
    left: 15px;
    font-size: 18px

}

</style>
