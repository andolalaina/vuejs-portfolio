<template>
    <ul>
        <li>
            <Navlink url="#accueil" name="accueil" active/>
        </li>
        <li>
            <Navlink url="#presentation" name="présentation"/>
        </li>
        <li>
            <Navlink url="#projets" name="projets"/>
        </li>
        <li>
            <Navlink url="#contacts" name="contacts"/>
        </li>
    </ul>
</template>

<script>
import Navlink from "./Navlink.vue"
export default {
    name: 'Navbar',
    components: {
        Navlink
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