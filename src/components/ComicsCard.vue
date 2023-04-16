<script>
export default {
    name: "ComicsCard",
    props: {
        img: String,
        name: String
    }
}
</script>

<template>
    <div class="card">
        <div class="img">
            <img :src="img" alt="">
        </div>
        <div>{{ name }}</div>
    </div>
</template>


<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;


.card {
    width: calc(100% / 6 - 20px);
    color: white;
    font-size: .7rem;

    @media screen and (max-width:850px) {
        width: calc(100% / 4 - 20px);

    }

    @media screen and (max-width:600px) {
        width: 100%;
        text-align: center;
        @include flex(column, center, center);

    }

    .img {
        width: 100px;
        height: 120px;
        margin-bottom: 10px;
        cursor: pointer;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }

}
</style>