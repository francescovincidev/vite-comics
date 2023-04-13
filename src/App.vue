<script>
import AppHeaderMenu from "./components/AppHeaderMenu.vue"
import BodyContent from "./components/BodyContent.vue"


export default{
  components:{
    AppHeaderMenu,
    BodyContent
  }
}

</script>

<template>
  <AppHeaderMenu />
  <BodyContent />

</template>

<style lang="scss">
@use "./style/general.scss" as *;


</style>
