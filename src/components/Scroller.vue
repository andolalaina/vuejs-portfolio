<template>
    <div class="scroller" :style="style">
        <slot></slot>
    </div>    
</template>

<script>
export default {
    name: 'Scroller',
    props: {
        width: String,
        height: String
    },
    computed: {
        style() {
            return {
                'max-width': this.width,
                'max-height': this.height
            }
        }
    }
}
</script>

<style scoped>
    .scroller {
        overflow: scroll;
    }

    ::-webkit-scrollbar {
        width: 3px;
        height: 0;
        border-radius: 5px;
    }

    ::-webkit-scrollbar-thumb {
        background: var(--primary);
    }

</style>