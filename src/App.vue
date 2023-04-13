<script>
import AppHeaderMenu from "./components/AppHeaderMenu.vue"
import BodyContent from "./components/BodyContent.vue"
import BlueContent from "./components/BlueContent.vue"
import FooterMain from "./components/FooterMain.vue"




export default{
  components:{
    AppHeaderMenu,
    BodyContent,
    BlueContent,
    FooterMain
  }
}

</script>

<template>
  <AppHeaderMenu />
  <BodyContent />
  <BlueContent />
  <FooterMain />

</template>

<style lang="scss">
@use "./style/general.scss" as *;


</style>
