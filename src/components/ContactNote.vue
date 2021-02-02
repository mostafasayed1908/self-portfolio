<template>
    <div class="c-note-wrapper">
        <div class="cd-fixed-bg cd-fixed-bg--1">
            <div class="hover-bg"></div>
            <div class="note-content">
                <h1>feel free to contact us anytime, anywhere</h1>
                <ContactBtn />
            </div>
        </div>

    </div>
</template>

<script>
import ContactBtn    from   '@/components/ContactBtn.vue'

export default {
  components: {
    ContactBtn
  }
}
</script>

<style scoped>
.c-note-wrapper {
  margin-top:50px;
  
}
.cd-fixed-bg {  
  background-size: cover;
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-position: center center;
  position: relative;
}

.cd-fixed-bg.cd-fixed-bg--1 {
  background-image: url("../assets/disk.jpeg");
}
.hover-bg {
    width: 100%;
    height: 100%;
    position: absolute;
    background-color: rgba(2, 2, 2, 0.555);
    top: 0;
    left: 0;
}
.note-content {
  padding: 100px;
  width: 100%;
  text-align: center;
  color: white;
  position: relative;
  z-index: 1;
}
.note-content h1 {
  text-transform: capitalize;
  font-weight: 700;
  font-size: 50px;
  color: white;
  line-height: 1.3;
}
.btn-new {
  border-radius: 0;
  background-color: rgb(230, 230, 230);
  color: rgb(46, 46, 46)
}
</style>
