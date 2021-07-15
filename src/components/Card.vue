<template>
    <div class="card">
        <div class="illustration">
            <div class="title">
                <a :href="link" target="_blank">
                    {{title}}
                </a>
            </div>
            <img :src="require(`@/assets/${illustrationFilename}`)">
        </div>
        <div class="badges">
            <div class="technos">
                <ul>
                    <li v-for="techno in technos" :key="techno.id">
                        <img :src="require(`@/assets/technos/${techno.logo}`)">
                    </li>
                </ul>
            </div>
        </div>
    </div>    
</template>

<script>
export default {
    name: 'Card',
    props: {
        illustrationFilename: String,
        technos: Array,
        title: String,
        link: String
    },
}
</script>

<style scoped>
    .card {
        display: flex;
        flex-flow: row;
        justify-content: flex-start;
        width: 80%;
        margin: 1rem 0;
    }
    .title {
        opacity: 0;
        position: absolute;
        display: flex;
        align-items: center;
        justify-content: space-around;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.6);
        font-weight: 700;
        transition: all .1s ease;
    }
    .title:hover {
        opacity: 1;
    }
    .title>a {
        text-decoration: none;
        color: inherit;
    }
    .illustration {
        position: relative;
        background: rgba(0, 0, 0, 0.6);
    }
    .illustration>img {
        max-width: 100%;
        height: auto;
    }
    .badges {
        background: rgba(0, 0, 0, 0.3);
    }
    .technos>ul {
        padding: 0;
        margin: .5rem;
        list-style: none;
    }
    li>img {
        width: 1rem;
    }
</style>