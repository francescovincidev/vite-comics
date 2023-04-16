<script>
export default {
    name: "BlueContent",
    data() {
        return {
            blueList: [
                {
                    img: "buy-comics-digital-comics.png",
                    text: "digital comics"
                },
                {
                    img: "buy-comics-merchandise.png",
                    text: "dc merchadise"
                },
                {
                    img: "buy-comics-subscriptions.png",
                    text: "subscription"
                },
                {
                    img: "buy-comics-shop-locator.png",
                    text: "comic chop locator"
                },
                {
                    img: "buy-dc-power-visa.svg",
                    text: "dc power visa"
                },

            ]

        }

    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="blue-content">
        <div class="content">
            <div v-for="btn in blueList">
                <img :src="getImagePath(btn.img)" alt="">
                <div>{{ btn.text }}</div>

            </div>

        </div>


    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.blue-content {
    padding: 35px 0;
    background-color: $primary-blue;
    color: white;
    @include flex(row, center, center);

    .content {
        @include container;
        @include flex(row, space-around, center);
        font-size: .7rem;
        text-transform: uppercase;


        @media screen and (max-width:600px) {
            @include flex(column, stretch, stretch);
            gap: 20px;
        }


        div {
            @include flex(row, flex-start, center);
            gap: 10px;
            height: 100%;
            flex-shrink: 0;

            img {
                max-width: 50px;
                max-height: 50px;
            }
        }


    }

}
</style>