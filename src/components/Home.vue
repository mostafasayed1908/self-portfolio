<template>
    <div id="home" class="home">
        <div class="container">
            <div class="socials  text-center">
                <ul>
                    <li><i class="fab fa-facebook-f"></i></li>
                    <li><i class="fab fa-twitter"></i></li>
                    <li><i class="fab fa-behance"></i></li>
                    <li><i class="fab fa-youtube"></i></li>
                    <li><i class="fab fa-instagram"></i></li>
                </ul>
            </div>
            <div class="home-main">
                <div class="name">
                    <div class="parag">
                        <h4>UI UX DEVELOPER</h4>
                        <p class="lead">
                            It is a long established fact that<br/>
                            a reader will be distracted by the readable<br/>
                            content of a page
                        </p>
                    </div>
                    <span class="m-letter">M</span>
                    <span class="name-letters">OSTAFA SAYED</span>
                </div>

                <!--
                <div class="row">
                    <div class="col-md-6">
                        <div class="m-letter">
                            M
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="">
                            OSTAFA SAYED
                        </div>
                    </div>
                </div>
                -->
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.home {
    width: 100%;
    margin-top: 110px;
}

.socials ul {
    list-style-type: none;
    display: inline-block;
    padding-left: 0
}
.socials ul li {
    float: left;
    width: 25px;
    height: 25px;
    background-color: black;
    border-radius: 50%;
    margin-left: 10px;
    margin-right: 10px;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    color: white;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center;
    font-size: 12px;
}
.home-main {
    width: 100%
}
.name {
    text-align: center;
        position: relative;

}
.m-letter {
    font-weight: bold;
    font-size: 278px;
}
.name-letters {
    font-weight: bold;
    font-size: 50px;

}
.parag {
    position: absolute;
    top: 104px;
    left: 527px;
}

@media (max-width: 576px) {
    .home {
        margin-bottom: 142px;
    } 
    .m-letter {
        font-weight: bold;
        font-size: 70px;
    }
    .name-letters {
        font-weight: bold;
        font-size: 20px;

    }
    .parag {
        position: absolute;
        top: 104px;
        left: 10px;
        width: 100%;
    }
    .home-main[data-v-8dc7cce2] {
    width: 100%;
    margin-top: -30px;
    }
 }

@media (min-width: 577px) { 
    .parag {
        position: absolute;
        top: 74px;
        left: 221px;
    }
    .parag h4  {
        font-size: 22px
    }
    .parag p  {
        font-size: 14px
    }
    .m-letter {
        font-weight: bold;
        font-size: 203px;
        -webkit-text-fill-color: transparent;
        background: url(../assets/ss.jpg) -100px -40px no-repeat;
        -webkit-background-clip: text;
        background-clip: text;
        background-position: center;
        background-size: cover;
    }
    .name-letters {
    font-weight: bold;
    font-size: 36px;

    }
    .home-main[data-v-8dc7cce2] {
    width: 100%;
    margin-top: -65px;
    }
 }
@media (min-width: 767px) { 
    .parag {
    position: absolute;
    top: 103px;
    left: 337px;
    }
    .parag h4  {
        font-size: 27px
    }
    .parag p  {
        font-size: 14px
    }
    .m-letter {
        font-weight: bold;
        font-size: 279px;
    }
    .name-letters {
        font-weight: bold;
        font-size: 35px;

    }
    .home-main[data-v-8dc7cce2] {
    width: 100%;
    margin-top: -100px;
    }
 }
@media (min-width: 992px) {  
    .parag {
    position: absolute;
    top: 114px;
    left: 406px;
    }
    .parag h4  {
        font-size: 34px
    }
    .parag p  {
        font-size: 15px
    }
    .m-letter {
        font-weight: bold;
        font-size: 313px;
    }
    .name-letters {
        font-weight: bold;
        font-size: 59px;

    }
    .home-main[data-v-8dc7cce2] {
    width: 100%;
    margin-top: -100px;
}
}

@media (min-width: 1260px) { 
    .parag {
    position: absolute;
    top: 114px;
    left: 550px;
    }
    .parag h4  {
        font-size: 38px
    }
    .parag p  {
        font-size: 17px
    }
    .m-letter {
        font-weight: bold;
        font-size: 313px;
    }
    .name-letters {
        font-weight: bold;
        font-size: 59px;

    }
    .home-main[data-v-8dc7cce2] {
    width: 100%;
    margin-top: -90px;
}
}
</style>
