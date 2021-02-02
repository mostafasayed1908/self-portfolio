<template>
    <div class="col-lg-4 col-md-6">
        <div class="single-service"
         @mouseenter="hovered" @mouseleave="unhovered"
         :class="{hovered:active,unhovered:active==false}"
         >
            <div class="row">
                <div class="col-md-3 col-sm-2 col-xs-4">
                    <i :class="icon"></i>
                </div>
                <div class="col-md-9 col-sm-10 col-xs-8">
                    <div class="sevice-info">
                        <h6>{{stitle}}</h6>
                        <p>{{scontent}}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            active : false
        }
    },
    props: [
        'icon',
        'stitle',
        'scontent'
    ],
    methods: {
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
.single-service {
    background-color: #ededed;
    box-shadow: 0 2px 8px 0 rgba(0, 0, 0, 0.1);
    margin-bottom: 37px;
    padding: 27px 24px;
    text-align: left;
}
.single-service i {
    display: inline-block;
    font-size: 50px;
}
.single-service .sevice-info h6 {
    font-size: 18px;
    font-weight: 700;
    letter-spacing: -.5px;
    margin-bottom: 8px;
}
.hovered {
    animation-name: hovered;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
}
@keyframes hovered {
    0%    { background-color: #ededed;color: #3b3b3b}
    100%  { background-color: #303030;color: #ededed}
}
.unhovered {
    animation-name: unhovered;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
}
@keyframes unhovered {
    0%  { background-color: #303030;color: #ededed}
    100%    { background-color: #ededed;color: #3b3b3b}
}
</style>
