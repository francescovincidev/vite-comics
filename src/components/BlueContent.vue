<script>
export default {
    name: "BlueContent"
}
</script>

<template>
    <div class="blue-content">

    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.blue-content{
    height: 100px;
    background-color: $primary-blue;
    color: white;
    @include flex(row, center, center);
    .content{
    @include container;

    }

}
</style>