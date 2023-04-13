<script>
export default {
    name: "FooterMain",
    data() {
        return {
            footerList: [
                {
                    title: "DC comics",
                    footerLinks: ["Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
                },
                {
                    title: "Shop",
                    footerLinks: ["Shop DC", "Shop DC Collectibles"]
                },
                {
                    title: "DC",
                    footerLinks: ["Terms Of Use", "Privacy policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"]
                },
                {
                    title: "Sites",
                    footerLinks: ["DC", "MAD Magazine", "DC kids", "DC Universe", "DC Power Visa"]
                },

            ]
        }
    }
}
</script>

<template>
    <div class="footer-main-content">
        <div class="content">
            <div class="lists">

                <ul v-for="list in footerList">
                    <li>
                        {{ list.title }}
                    </li>
                    <li v-for="link in list.footerLinks">
                        {{ link }}
                    </li>
                </ul>


            </div>

           
        </div>

    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;


.footer-main-content {
    background-image: url("../assets/img/footer-bg.jpg");
    height: 100%;
    color: white;
    font-size: .65rem;


    .content {
        @include container;
        @include flex(row, flex-start, flex-start);
        height: 100%;
        background-image: url("../assets/img/dc-logo-bg.png");
            background-size: 50%;
            background-repeat: no-repeat;
            background-position: right;


        .lists {
            @include flex(column, flex-start, flex-start);
            flex-wrap: wrap;
            width: 50%;
            gap: 20px;
            height: 400px;
            padding: 30px 0 50px;
            ul {
                li {
                    padding: 5px 0;
                }

                li:first-child {
                    font-size: 1rem;
                    font-weight: bolder;
                    padding: 5px 0;
                }
            }

        }
    }

}
</style>