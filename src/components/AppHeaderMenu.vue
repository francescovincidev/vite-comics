<script>
export default {
    name: "AppHeaderMenu",
    data() {
        return {
            menuLinks: [
                {
                    text: "Characters",
                    url: "#",
                    current: false
                },
                {
                    text: "Comics",
                    url: "#",
                    current: true
                },
                {
                    text: "Movies",
                    url: "#",
                    current: false
                },
                {
                    text: "TV",
                    url: "#",
                    current: false
                },
                {
                    text: "Games",
                    url: "#",
                    current: false
                },
                {
                    text: "Collectibles",
                    url: "#",
                    current: false
                },
                {
                    text: "Videos",
                    url: "#",
                    current: false
                },
                {
                    text: "Fans",
                    url: "#",
                    current: false
                },
                {
                    text: "News",
                    url: "#",
                    current: false
                },
                {
                    text: "Shop",
                    url: "#",
                    current: false
                },
            ]
        }
    }

}
</script>

<template>
    <div class="header-menu">
        <img src="../assets/img/dc-logo.png" alt="">
        <ul>
            <li v-for="menu in menuLinks">
                {{ menu.text }}
                <div class="blue-orizontal"></div>
            </li>
        </ul>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.header-menu {
    @include flex(row, space-between, center);
    @include container;
    text-transform: uppercase;
    height: 100px;
    font-weight: bold;
    font-size: .7rem;
    color: $primary-grey;

    img {
        max-height: 80%
    }

    ul {
        @include flex(row, space-between, center);
        gap: 30px;

        li {
            @include flex(row, space-between, center);
            position: relative;
            height: 100px;
            width: 100%;

            .blue-orizontal {
                height: 3px;
                width: 100%;
                background-color: $primary-blue;
                margin: 0 auto;
                position: absolute;
                bottom: 0;
                display: none;
            }
        }

        li:hover {
            color: $primary-blue;
            cursor: pointer;

            & .blue-orizontal {
                display: block;
            }
        }
    }
}
</style>