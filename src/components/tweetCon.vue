<template>
    <div :class="{active:isActive}">
            <TweetContent v-for="tweet in tweets" 
            :key="tweet.id" 
            v-bind="tweet" />
            
    </div>
</template>

<script>
    import TweetContent from './TweetContent.vue'
    export default {
        name : 'TweetCon',
        components:{
            TweetContent
        },
        data : () =>{
            return {
                isActive : true,
                tweets : [
                    {
                        id : 1,
                        tweetInfo : "Today is not Ted Dansons birthday.",
                        user : "@TedDansonBDay",
                        date : "August 13, 2021",
                    },
                    {
                        id : 2,
                        tweetInfo : "Movies with Ashton Kutcher don't make top 5/10 lists.",
                        user : "@RearAdBsBlog",
                        date : "August 12, 2021",
                    },
                    {
                        id : 3,
                        tweetInfo : "Khloe Kardashian Flaunts Her Natural Curls in Gym Selfie: 'Felt Kinda Cute'",
                        user : "@people",
                        date : "August 13, 2021",
                    },
                    {
                        id : 4,
                        tweetInfo : "After you die, the last part of your body to stop working are your pupils because... They dilate!",
                        user : "@jokesUK",
                        date : "August 14, 2021",
                    },
                    {
                        id : 5,
                        tweetInfo : "Love it when a cat smells like laundry",
                        user : "@BaruchelNDG",
                        date : "August 15, 2021",
                    },
                    {
                        id : 6,
                        tweetInfo : "tweet tweet",
                        user : "@tweetguy",
                        date : "August 13, 2021",
                    },
                ]
        }},
        mounted(){
                this.$root.$on('isActive', this.toggleStyle)
        },
        methods : {
            toggleStyle() {
                console.log("print");
                if (this.isActive==true){
                    this.isActive = false;
                    console.log('true');
                }else{
                    this.isActive = true;
                    console.log('false');
                    
                }
            }
        }
    }

</script>

<style scoped>
    .active{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        height: 100vh;
        border: 1px solid black;
    }


</style>