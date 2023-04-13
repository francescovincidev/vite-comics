<script>
import AppHeaderMenu from "./components/AppHeaderMenu.vue"
import BodyContent from "./components/BodyContent.vue"
import BlueContent from "./components/BlueContent.vue"
import FooterMain from "./components/FooterMain.vue"
import FooterContacts from "./components/FooterContacts.vue"

export default{
  components:{
    AppHeaderMenu,
    BodyContent,
    BlueContent,
    FooterMain,
    FooterContacts

    
  }
}

</script>

<template>
  <AppHeaderMenu />
  <BodyContent />
  <BlueContent />
  <FooterMain />
  <FooterContacts />


</template>

<style lang="scss">
@use "./style/general.scss" as *;


</style>
