<template>
    <div id="skills" class="skills-wrapper">
        <div class="container">
            <h3>Skills</h3>
            <div class="borderr">
                <div class="border-itself"></div>
            </div>
             <v-tabs
                centered
                icons-and-text>
                <v-tabs-slider color="#3f3f3f"></v-tabs-slider>

                <v-tab href="#tab-1">
                Front-End
                <i class="fas fa-paint-brush"></i>
                </v-tab>

                <v-tab href="#tab-2">
                Back-End
                <i class="fas fa-code"></i>
                </v-tab>

                <v-tab href="#tab-3">
                Graphic Design
                <i class="fab fa-adobe"></i>
                </v-tab>

                <v-tab-item
                :value="'tab-1'"
                >
                <v-card flat>
                    <v-card-text>
                    <SkillsFront />
                    </v-card-text>
                </v-card>
                </v-tab-item>
                <v-tab-item
                :value="'tab-2'"
                >
                <v-card flat>
                    <v-card-text>
                        <SkillsBack />
                    </v-card-text>
                </v-card>
                </v-tab-item>
                <v-tab-item
                :value="'tab-3'"
                >
                <v-card flat>
                    <v-card-text>
                        <SkillsGraphic />
                    </v-card-text>
                </v-card>
                </v-tab-item>
            </v-tabs>
        </div>
    </div>
</template>

<script>
import SkillsFront from '@/components/SkillsFront'
import SkillsBack from '@/components/SkillsBack'
import SkillsGraphic from '@/components/SkillsGraphic'

export default {
    data () {
      return {
      }
    },
    components: {
        SkillsFront,
        SkillsBack,
        SkillsGraphic
    }
}
</script>

<style>
.v-card__text {
    padding: 0;
    }
.theme--light.v-tabs__bar {
    background-color: transparent;
}

.theme--light.v-card {
    background-color: transparent !important;
    border-color: #fff;
    color: rgba(0,0,0,0.87);
}
.theme--light.v-sheet {
    background-color: transparent;
    border-color: #fff;
    color: rgba(0,0,0,0.87);
}
.v-tabs__item i.fab.fa-adobe {
    font-size: 22px;
    padding: 5px;
}
.v-tabs__item i.fas.fa-paint-brush {
    font-size: 22px;
    padding: 5px;
}
.v-tabs__item i.fas.fa-code {
    font-size: 22px;
    padding: 5px;
}
.skills-wrapper {
    padding-top: 35px;
}
.skills-wrapper .container {
    padding-bottom: 0;
}
.skills-wrapper h3 {
    width: 100%;
    text-align: center;
    color: #646464;
    font-weight: normal;
}
.tab-content {
    padding-top: 30px
}
.tab-content .skill-bar {
    margin-bottom: 20px
}
.tab-content .progress {
    background-color: #d7d7d7;
}
.front-end .progress-bar {
    background-color: #474646
}
.back-end .progress-bar {
    background-color: #286689
}
.graphic .progress-bar {
    background-color: #5c2b66
}

.theme--light.v-sheet {
    background-color: #fff;
    border-color: #fff;
    color: rgba(0,0,0,0.87);
}
.theme--light.v-card {
    background-color: #fff;
    border-color: #fff;
    color: rgba(0,0,0,0.87);
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
