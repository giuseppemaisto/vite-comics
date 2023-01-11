     <script>
        export default {
            data(){
                return{
                    menu: [
                        {
                            label: 'CHARACTERS',
                            url: '#',
                            active: false,
                        },
                        {
                            label: 'COMICS',
                            url: '#',
                            active: true,
                        },
                        {
                            label: 'MOVIES',
                            url: '#',
                            active: false,
                        },
                        {
                            label: 'TV',
                            url: '#',
                            active: false,
                        },
                        {
                            label: 'GAMES',
                            url: '#',
                            active: false,
                        },
                        {
                            label: 'COLLECTIBLES',
                            url: '#',
                            active: false,
                        },
                        {
                            label: 'VIDEOS',
                            url: '#',
                            active: false,
                        },
                        {
                            label: 'FANS',
                            url: '#',
                            active: false,
                        },
                        {
                            label: 'NEWS',
                            url: '#',
                            active: false,
                        },
                        {
                            label: 'SHOP',
                            url: '#',
                            active: false,
                        },


                    ]
                }
            }
            
        }
    </script>
<template lang="">
    <header>
        <a href="/" class="brand">
            <img src="../assets/img/dc-logo.png" alt="logo">
        </a>
        <nav>
            <ul>
                <li v-for="(item, index) in menu" ::key="index">
                <a :href="item.url" :class="item.active ? 'active': ''">
                {{item.label}}
                </a>
                </li>
            </ul>
        </nav>
    </header>
</template>
<style lang="scss">
    @use '../styles/partials/variable' as *;
    @use '../styles/partials/mixins' as *;
    header{
        width: 95%;
        display: flex;
       padding: 40px;
       justify-content: space-between;

       ul{
        list-style: none;
        margin: 2rem 2rem;
        @include flex;

        li a{
            display: inline-block;
            padding: 1rem;
            text-decoration: none;
            color: black;
            

            &.active,
            &:hover{
                color: $primary;
            }
        }
       }
    }
</style>