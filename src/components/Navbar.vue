<template>
    <ul>
        <li v-for="nav in navs" :key="nav.id">
            <Navlink :url="nav.url" :name="nav.name" :active="nav.active" @handle-nav="handleNav(nav.id)"/>
        </li>
    </ul>
</template>

<script>
import Navlink from "./Navlink.vue"
export default {
    name: 'Navbar',
    components: {
        Navlink
    },
    methods: {
        handleNav(id) {
            this.navs.map(nav => nav.active = false);
            this.navs.filter(nav => nav.id === id)[0].active = true;
        }
    },
    data() {
        return {
            navs : [
                {
                    id: 1,
                    url: "#accueil",
                    name: "accueil",
                    active: true
                },
                {
                    id: 2,
                    url: "#presentation",
                    name: "presentation",
                    active: false
                },
                {
                    id: 3,
                    url: "#projets",
                    name: "projets",
                    active: false
                },
                {
                    id: 4,
                    url: "#contacts",
                    name: "contacts",
                    active: false
                },
        ]
        }
    }
}
</script>

<style scoped>
    ul {
        display: flex;
        justify-content: flex-end;
        position: fixed;
        right: 0%;
    }
    li {
        list-style: none;
    }
</style>