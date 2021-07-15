<template>
    <div :id="contentLink" class="container">
        <div class="illustration">
            <img :src="require(`@/assets/${illustrationFilename}`)"/>
        </div>
        <div class="text">

        </div>
    </div>
</template>

<script>
export default {
    name: 'Content',
    props: {
        illustrationFilename: String,
        contentLink: String
    }
}
</script>

<style>
    .container {
        margin: auto;
        width: 95%;
        height: 100vh;
        display: flex;
        flex-flow: row wrap;
    }
    .illustration {
        width: 50%;
        display: flex;
        align-items: center;
        justify-content: space-around;
    }
    .text {
        width: 50%;
    }
</style>