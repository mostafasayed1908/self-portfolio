<template>

  <div class="text-xs-center parent-scope">
    <v-dialog
      v-model="dialog"
    >
        <template v-slot:activator="{ on }">
          <i v-on="on" class="fas fa-plus-circle"></i>
        </template>

      <v-card>


        <v-toolbar dark color="primary">
          <v-btn icon dark @click="dialog = false">
            <v-icon>close</v-icon>
          </v-btn>
          <v-toolbar-title>{{ptitle}}</v-toolbar-title>
          <v-spacer></v-spacer>
        </v-toolbar>
        <v-content three-line subheader padding="20px">
            <div class="article-container">
                <img src="../assets/project/02.gif" alt="">
                <img src="../assets/project/03.png" alt="">
                <img src="../assets/project/05.gif" alt="">
                <img src="../assets/project/06.png" alt="">
            </div>
        </v-content>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
    data () {
      return {
        dialog: false,
        notifications: false,
        sound: true,
        widgets: false
      }
    },
    props: [
        'ptitle'
    ]
}
</script>

<style scoped>
.text-xs-center {
    text-align: left !important;
}
i:hover{
    cursor: pointer; 
}
.v-dialog:not(.v-dialog--fullscreen)[style] {
    max-height: 90%;
    width: 90%!important;
    min-width: 90% !important;
}
.v-dialog[style] {
    width: 90% !important;
    min-width: 90% !important;
    z-index: inherit;
    margin: 0!important; 
 }
.primary {
    background-color: #e7e7e7 !important;
    border-color: #1976d2 !important;
}
.theme--dark.v-toolbar {
    background-color: #212121;
    color: #414141;
}
.v-btn .v-btn__content .v-icon {
    color: #4a4a4a;
}
.v-card > :last-child:not(.v-btn):not(.v-chip) {
    border-bottom-left-radius: inherit;
    border-bottom-right-radius: inherit;
    background-color: #a1a1a1;
    padding: 20px !important;
}
.article-container {
    width: 100%

}
.article-container img {
    max-width: 100%;
}
.v-dialog__content { 
    z-index: 10000 !important;
}
</style>
