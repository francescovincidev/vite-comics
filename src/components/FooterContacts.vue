<script>
export default {
    name: "FooterContacts",
    data() {
        return {
            socialList: {
                title: "Follow us",
                socials:["footer-facebook.png", "footer-twitter.png", "footer-youtube.png","footer-pinterest.png","footer-periscope.png",]
            }
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
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" integrity="sha512-iecdLmaskl7CVkqkXNQ/ZH/XLlvWZOJyj7Yy7tcenmpD1ypASozpmT/E0iPtmFIB46ZmdtAc9eNBvH0H/ZpiBw==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <div class="footer-contacts">
        <div class="content">
            <div class="singup">sing-up now!</div>
            <div class="socials">
                <ul>
                    <li>
                        {{ socialList.title }}
                    </li>
                    <li v-for="social in socialList.socials">
                        <img :src="getImagePath(social)" alt="">

                    </li>
                </ul>
            </div>
        </div>

    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.footer-contacts{
    height: 80px;
    background-color: $primary-grey;
    text-transform: uppercase;
    .content{
        height: 100%;
        @include container;
        @include flex(row, space-between, center);
        
        
        .singup{
            color: white;
            padding: 5px 10px;
            border: 1px solid $primary-blue;
            font-weight: bolder;


        }

        .socials{
            ul{
                @include flex(row, flex-start, center);
                gap: 10px;

                li:first-child {
                    font-size: 1rem;
                    font-weight: bolder;
                    color: $primary-blue;
                    padding-right: 10px;

                }

                li{
                    img{
                        width: 25px;
                    }
                }

            }
            
        }

    }
}

</style>