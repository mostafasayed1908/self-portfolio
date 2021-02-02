<template>
  <div class="text-xs-center">
    <v-dialog
      v-model="dialog"
      width="500"
    >
      <template v-slot:activator="{ on }">
        <v-btn
          color="red lighten-2"
          dark
          v-on="on"
        >
          Get In Touch
        </v-btn>
      </template>

      <v-card>
        <v-card-title
          class="headline grey lighten-2"
          primary-title
        >
        <div class="socials  text-center">
            <ul>
                <li><i class="fab fa-facebook-f"></i></li>
                <li><i class="fab fa-twitter"></i></li>
                <li><i class="fab fa-behance"></i></li>
                <li><i class="fab fa-youtube"></i></li>
                <li><i class="fab fa-instagram"></i></li>
            </ul>
        </div>

        </v-card-title>

        <v-card-text>
            <div class="row">
                <div class="col-md-12">
                    <ContactBtnDetails 
                    v-for="detail in details"
                    :key="detail.id"
                    :dIcon="detail.dIcon"
                    :dTitle="detail.dTitle"
                    :dContent="detail.dContent"
                    />
                </div>
            </div>

        </v-card-text>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
import ContactBtnDetails    from   '@/components/ContactBtnDetails.vue'

export default {
    components: {
        ContactBtnDetails,
    },
    data () {
      return {
        dialog: false,
        details: [
            {id:1,dIcon:'fas fa-file-signature',dTitle:'Name',dContent:'Mostafa Sayed'},
            {id:2,dIcon:'fab fa-leanpub',dTitle:'Location',dContent:'4155 Mann Island, Liverpool, United Kingdom.'},
            {id:3,dIcon:'fas fa-headset',dTitle:'Call Me',dContent:'+44 1632 967704'},
            {id:4,dIcon:'fas fa-paper-plane',dTitle:'Email',dContent:'daniel@example.com'}
        ]
      }
    }
}
</script>

<style scoped>
.red.lighten-2 {
    background-color: #383838 !important;
    border-color: #fbfbfb !important;
}
.theme--light.v-card {
    overflow: hidden
}
.v-card > :last-child:not(.v-btn):not(.v-chip) {
    border-bottom-left-radius: inherit;
    border-bottom-right-radius: inherit;
    background-color: #ececec;
    padding: 20px;
}
.grey.lighten-2 {

    background-color: #3c3c3c !important;
    border-color: #e0e0e0 !important;
    color: white;
    text-align: center;
}
.socials {
    width: 100%;
}
.socials ul {
    list-style-type: none;
    display: inline-block;
    padding-left: 0;
    margin-bottom: 0
}
.socials ul li {
    float: left;
    width: 25px;
    height: 25px;
    background-color: #ececec;
    border-radius: 50%;
    margin-left: 10px;
    margin-right: 10px;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    color: #3c3c3c;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center;
    font-size: 12px;
}
</style>
