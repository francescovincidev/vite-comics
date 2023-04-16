<script>
export default {
    name: "Jumbotron"
    
}
</script>

<template>
    <div class="jumbotron">

    </div>
    
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.jumbotron{
    background-image: url("../assets/img/jumbotron.jpg");
    height: 300px;
    background-size: cover;

}



</style>