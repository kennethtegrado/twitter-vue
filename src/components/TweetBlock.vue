<template>
    <div id="tweetBlock">
        <div class="userPhoto">
            <img :src="require('./../assets/me3.jpg')" alt="user-img" class="user-img">
        </div>

        <div id="tweet-form">
            <textarea id="tweetForm" rows="3" placeholder="What's happening?"> </textarea>
        </div>
        <div class="postActions">
            <div class="postAction">
                <img :src="require('./../assets/photo-icon.png')" class="action-icon">
            </div>
            <div class="postAction">
                <img :src="require('./../assets/gif-icon.png')" class="action-icon">
            </div>
            <div class="postAction">
                <img :src="require('./../assets/poll-icon.png')" class="action-icon">
            </div>
            <div class="postAction">
                <img :src="require('./../assets/emoji-icon.png')" class="action-icon">
            </div>
            <div class="postAction">
                <img :src="require('./../assets/sched-icon.png')" class="action-icon">
            </div>
            <button class="btn-tweet" id="tweet_button">Tweet</button>
        </div>
    </div>
</template>

<script>
export default {
    name: "TweetBlock"    
}
</script>

<style scoped>

#tweetBlock {
    border: 1px solid rgb(187, 37, 37);
    position: relative;
    display: block;
    width: 100%;
    text-align: left;
}

.userPhoto, .tweet-form, .postActions {
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


#tweet-form {
    margin-top: 10px;
    margin-left: 85px;
    border: 1px solid red;
    width: 85%;
}

#tweetForm {
    border-radius: 5px;
    width: 96%;
}



.postActions {
    margin-left: 85px;
    border: 1px solid black;
    display: inline-block;
    width: 85%;
}

.postAction {
    float: left;
    margin-right: 20px;
}

.postAction img {
    border: 1px solid black;
    width: 30px;
    height: 30px;
}

.btn-tweet {
    position: relative;
    float: right;
    margin-right: 15px;
    height: 40px;
    width: 80px;
    border-radius: 20px;
    border: none;
    background-color: #468be4 !important;
    color: white;
}
</style>