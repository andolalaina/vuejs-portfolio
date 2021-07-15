<template>
    <div :id="contentLink" :class="reversed ? 'container reversed':'container'">
        <div class="illustration">
            <img :src="require(`@/assets/${illustrationFilename}`)"/>
        </div>
        <div class="text">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Content',
    props: {
        illustrationFilename: String,
        contentLink: String,
        reversed: Boolean
    }
}
</script>

<style scoped>
    .container {
        margin: auto;
        width: 95%;
        height: 100vh;
        display: flex;
        flex-flow: row wrap;
    }
    .container.reversed {
        flex-flow: row-reverse wrap;
    }
    .illustration {
        width: 50%;
        display: flex;
        align-items: center;
        justify-content: space-around;
    }
    .text {
        width: 50%;
        color: var(--white);
        display: flex;
        flex-flow: column;
        justify-content: center;
    }
</style>