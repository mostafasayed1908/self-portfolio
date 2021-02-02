<template>
<div id="testimonials" class="testi">

    <div class="testo-wrapper">
        <div class="container">
            <h3>Testimonials</h3>
            <div class="bd-example">
            <div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
                <ol class="carousel-indicators">
                <li data-target="#carouselExampleCaptions" data-slide-to="0" class="active"></li>
                <li data-target="#carouselExampleCaptions" data-slide-to="1"></li>
                <li data-target="#carouselExampleCaptions" data-slide-to="2"></li>
                </ol>
                <div class="carousel-inner">
                <div class="carousel-item active">
                    <div class="carousel-caption d-md-block">
                    <p class="lead"><i class="fas fa-quote-left"></i> Nulla vitae elit libero, a pharetra augue mollis interdum. <br > Nulla vitae elit libero, a pharetra augue mollis interdum. <i class="fas fa-quote-right"></i></p>
                    <span>First slide label</span>
                    </div>
                </div>
                <div class="carousel-item">
                    <div class="carousel-caption d-md-block">
                    <p class="lead"><i class="fas fa-quote-left"></i> Nulla vitae elit libero, a pharetra augue mollis interdum. <br > Nulla vitae elit libero, a pharetra augue mollis interdum. <i class="fas fa-quote-right"></i></p>
                        <span>Jack Doe CEO at Company</span>
                    </div>
                </div>
                <div class="carousel-item">
                    <div class="carousel-caption d-md-block">
                    <p class="lead"><i class="fas fa-quote-left"></i> Nulla vitae elit libero, a pharetra augue mollis interdum. <br > Nulla vitae elit libero, a pharetra augue mollis interdum. <i class="fas fa-quote-right"></i></p>
                    <span>Third slide label</span>
                    </div>
                </div>
                
                </div>
            </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {

}
</script>

<style scoped>
.testi {
    position: relative;
    z-index: 1;
}
.testo-wrapper {
    width: 100%;
    padding-top: 70px;
    margin-bottom: 70px;
    background-color: #292929;
    position: relative;
}
.testo-wrapper:after {
    position:absolute;
    width:100%;
    height:100%;
    content:'';
    z-index:-1;
    background-color:#292929;
    top:0;
    left:0;
    right:0;
    bottom:0;
    transform-origin: top left ;
    transform: skewY(4deg)
}
.testo-wrapper h3 {
    width: 100%;
    text-align: center;
    color: white;
    font-weight: normal;
}
.carousel-caption {
    color:#838383;
    position: relative;
    right: 0;
    bottom: 0;
    left: 0;
    padding-bottom: 35px;
}
.carousel-caption p {
    font-size: 17px;
    margin-bottom: 6px;
    color: #bcbcbc;
}
.carousel-caption p i{
    font-size: 22px;
}
.carousel-caption span {
    font-size: 13px;
    margin-bottom: 10px
}
.carousel-indicators li {
    background-color: white;
}

</style>
