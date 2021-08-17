<template>
    <div>
        <h3>{{user}}</h3>
        <p>{{tweetInfo}}</p>
        <h5>{{date}}</h5>
    </div>
</template>

<script>
    export default {
        name: 'TweetContent',
        props: {
            tweetInfo : String,
            user : String,
            date : String
        }        
    }

</script>

<style scoped>
        div {
        border: 2px double black;
        border-radius: 15%;
        background-image: linear-gradient(to bottom right, lightblue, lightgreen);
        padding: 6vw;
        margin: 2vw
    }
    h3 {
        color: rgb(28, 56, 82);
    }

</style>