<template>
    <div class="degree">
        <div class="date">{{date}}</div>
        <div class="details">
            <div class="title">{{title}}</div>    
            <div class="course">{{course}}</div>
            <div class="place">{{institution}}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Degree',
    props: {
        date: String,
        title: String,
        course: String,
        institution: String
    }
}
</script>

<style scoped>
    .degree {
        margin: 1rem 0;
        display: flex;
    }
    .date {
        margin-right: .5rem;
        min-width: 20%;
    }
    .title {
        font-weight: 700;
        margin-bottom : .8rem;
    }
    .place {
        font-size: .82rem;
        font-weight: 100;
    }
</style>