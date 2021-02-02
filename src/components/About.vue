<template>
<div id="about" class="about-wrapper">
        <div class="main-about">
            <div class="container">
                 <h3>Basic Info About Me</h3>
                 <div class="bordeer"><div class="border-itself"></div></div>
                 <div class="row">
                     <div class="col-md-4">
                         <div class="img-container">
                             <img src="../assets/mm.jpeg" alt="">
                         </div>
                     </div>
                     <div class="col-md-8">
                         <div class="info-container">
                            <h5>About Me</h5>
                            <p class="lead">
                                I'm a USA based UX/UI Designer creating awesome and effective visual identities for companies of all sizes around the globe.It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here
                            </p>
                            <h5>Personal Information</h5>
                            <ul>
                                <li><i class="fas fa-user-alt"></i> Name : Mostafa Sayed</li>
                                <li><i class="fas fa-calendar-week"></i> Age : 23 Years Old</li>
                                <li><i class="fas fa-phone-volume"></i> Phone : +20 111 232 7121</li>
                                <li><i class="fas fa-envelope"></i> E-Mail : m.sayed1908@gmail.com</li>
                                <li><i class="fas fa-map-marker-alt"></i> Address : Cairo,Egypt</li>

                            </ul>
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
.about-wrapper {
    position: relative;
    z-index: 2;
}
.main-about{
    width: 100%;
    position: relative;
    background-color: rgb(33, 33, 33);
    color: white;
    padding-top: 35px;
}
.main-about::after {
    position:absolute;
    width:100%;
    height:100%;
    content:'';
    z-index:-1;
    background-color:rgb(33, 33, 33);
    top:0;
    left:0;
    right:0;
    bottom:0;
    transform-origin: top left ;
    transform: skewY(4deg)
}
.main-about::before {
    position:absolute;
    width:100%;
    height:100%;
    content:'';
    z-index:-2;
    background-color:rgb(33, 33, 33);
    top:0;
    left:0;
    right:0;
    bottom:0;
    transform-origin: bottom right;
    transform: skewY(4deg)
}
.main-about h3 {
    width: 100%;
    text-align: center; 
    font-weight: normal
}
.main-about .bordeer {
    width: 100%;
    text-align: center;
    
}
.main-about .border-itself {
    width: 50px;
    border-top: solid rgb(255, 255, 255) 5px;
    display: inline-block;
}
.main-about .img-container {
    width: 100%;
    overflow: hidden;
    border-radius: 4px;
    border: solid 1px #747474;
}
.main-about .img-container img {
    max-width: 100%;

}
.info-container p {
    font-size: 15px;
    color: #838383;
}
.info-container ul {
    list-style-type: none;
    padding: 0;
    font-size: 15px;
    color: #838383;

}
.info-container ul li{
    display: inline-block;
    width: 50%;
    padding: 4px 0 4px 0;
}
@media (max-width: 767px) {  
.info-container {
    margin-top: 30px
}
.info-container ul li{
    display: inline-block;
    width: 100%;
    padding: 4px 0 4px 0;
}
}

</style>
