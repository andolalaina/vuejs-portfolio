<template>
    <a :href="url" :class="active?'active':''" @click="e">{{name}}</a>
</template>

<script>
export default {
    name:'Navlink',
    props: {
        url: String,
        name: String,
        active: Boolean
    }
}
</script>

<style scoped>
    a {
        text-transform: capitalize;
        text-decoration: none;
        color: var(--white);
        margin: 0 1rem;
    }
    a:hover:not(.active) {
        text-decoration: underline;
    }
    a.active {
        font-weight: 700;
    }
</style>