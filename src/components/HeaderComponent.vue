<script>
    export default {
        name: "HeaderComponent",
  data() {
    return {
        menuItems: [
                {
                    label: "Characters",
                    url: "#",
                    active: false
                },
                {
                    label: "Comics",
                    url: "#",
                    active: true
                },
                {
                    label: "Movies",
                    url: "#",
                    active: false
                },
                {
                    label: "Tv",
                    url: "#",
                    active: false
                },
                {
                    label: "Games",
                    url: "#",
                    active: false
                },
                {
                    label: "Collectibles",
                    url: "#",
                    active: false
                },
                {
                    label: "Videos",
                    url: "#",
                    active: false
                },
                {
                    label: "Fans",
                    url: "#",
                    active: false
                },
                {
                    label: "News",
                    url: "#",
                    active: false
                },
                {
                    label: "Shop",
                    url: "#",
                    active: false
                },
            ]
    }
  }
}
</script>


<template>
    <header>
        <div>
            <img src="../assets/img/dc-logo.png" alt="">
        </div>

        <div>
            <ul>
                <li  v-for="(item, index) in menuItems" ::key="index" :class="item.active ? 'active' : ''">

                    <a :href="item.url" :class="item.active ? 'active' : ''">

                        {{ item.label }}
                        
                    </a>
                </li>
            </ul>
        </div>
    </header>
</template>


<style lang="scss" scoped>

$blue-color: #0282f9;

$border-btn-blue: 3px solid $blue-color;

    header{
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 40px 0;
        background-color: white;

        img{
            max-width: 100%;
        }

            ul{
                list-style: none;
                display: flex;

            }

                li{

                    &:hover{
                        border-bottom: $border-btn-blue
                    }

                    &.active{
                        border-bottom: $border-btn-blue;
                }


                    a{
                        text-decoration: none;
                        color: black;
                        padding: 30px 15px;

                        &:hover{
                            color: $blue-color;
                        }

                        
                        &.active{
                            color: $blue-color;
                        }
                    }
                }
    }
</style>