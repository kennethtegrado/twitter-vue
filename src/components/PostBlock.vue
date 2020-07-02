<template>
    <div class="post-block">
        <div class="userPhoto">
            <img :src="require('./../assets/' + tweet.user_img + '')" alt="user-img" class="user-img">
        </div>
        <div class="tweetContent">
            <h5>
                <b> {{ tweet.username }} </b>
                <small class="text-muted"> {{ tweet.usertag }} - {{ tweet.time_elapsed}} </small>
            </h5>
            <p class="tweet-text"> 
                {{ tweet.content}}
            </p>
            <img :src="require('./../assets/' + tweet.content_img + '')" alt="tweet-img" class="tweet-img">
        </div>
        <div class="tweetActions">
            <div class="tweetAction">
                <img :src="require('./../assets/comment-icon.png')" class="action-icon"> <span class="actionCountLabel"> 9,696 </span>
            </div>
            <div class="tweetAction">
                <img :src="require('./../assets/rt-icon.png')" class="action-icon"> <span class="actionCountLabel"> 9,696 </span>
            </div>
            <div class="tweetAction">
                <img :src="require('./../assets/like-icon.png')" class="action-icon"> <span class="actionCountLabel"> 9,696 </span>
            </div>
            <div class="tweetAction">
                <img :src="require('./../assets/message-icon.png')" class="action-icon"> <span class="actionCountLabel"> 9,696 </span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "PostBlock",
    props: ["tweet"]
}
</script>

<style scoped>


.post-block {
    border: 1px solid black;
    width: 100%;
    position: relative;
    display: block;
}

.userPhoto, .tweetContent, .tweetActions {
    border: 1px solid black;
    position: relative;
}

.userPhoto {
    border-radius: 50%;
    float: left;
    margin-top: 15px;
    margin-left: 15px;
    background-color: grey;
    overflow: hidden;
}
.userPhoto img {
    width: 60px;
    height: 60px;
    object-fit:contain;
    transform: translate(0, 3%);
}

.tweetContent, .tweetActions {
    margin-left: 85px;
}

.tweetContent {
    text-align: left;
}

small {
    color: grey;
}


h5 {
    margin-bottom: 10px;
}
p {
    padding-top: 0px;
    margin-top: 0px;
    margin-bottom: 5px;
}

.tweet-img {
    max-width: 100%;
}

.tweetActions {
    justify-content: space-between;
    display: flex;
    width: 79%;
}

.tweetAction {
    display: flex;
    justify-content: center;
}
.action-icon {
    width: 30px;
    height: 30px;
}

.actionCountLabel {
    border: 1px solid black;
    padding-top: 5px;
    margin-left: 5px;
}

</style>