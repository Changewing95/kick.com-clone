
<template>
    <div class="main-content">
        <div class="content">
            <h1>Featured Streams</h1>
            <div class="content-video">
                <div class="video vid-1">
                    <img src="../../assets/chess.webp">
                    <h3>World Chess Championship Day 4</h3>
                    <h5>GMHikaru</h5>
                    <span>Chess</span>
                    <div class="livestream-block">
                        <h1>LIVE</h1>
                    </div>
                </div>
                <div class="video">
                    <img src="../../assets/thumb32___video_thumbnail_627_353.webp">
                    <h3>OIL CHANGES</h3>
                    <h5>Yupy</h5>
                    <span>Travel & Outdoors</span>
                    <div class="livestream-block">
                        <h1>LIVE</h1>
                    </div>
                </div>
                <div class="video">
                    <img src="../../assets/thumb76___video_thumbnail_550_309.webp">
                    <h3>Playing Games :D</h3>
                    <h5>Gamer1</h5>
                    <span>Call Of Duity: Warzone 2.0</span>
                    <div class="livestream-block">
                        <h1>LIVE</h1>
                    </div>
                </div>
            </div>
            <div class="border-line">
            </div>
            <AppCategory></AppCategory>
            <AppCategoryVideo></AppCategoryVideo>

        </div>
    </div>
</template>


<script setup>
import AppCategory from '../KICK/AppCategory.vue'
import AppCategoryVideo from '../KICK/AppCategoryVideo.vue'

</script>

<style scoped>

    .livestream-block {
        background-color: black;
        width: 40px;
        border-radius: 20%;
        position: absolute;
        top: 10px;
        left: 10px;
    }

    .livestream-block > h1 {
        color: rgb(81,245,24);
        text-align: center;
        font-size: 13px;
        font-weight: 700;
        padding: 3px;
    }

    .video > img {
        max-width: 100%;
        max-height: 100%;
        height: 100%;
        object-fit: cover;
    }

    .video h3 {
        color: white;
        font-weight: 700;
        font-size: 17px;
    }

    .video h5 {
        font-size: 15px;
        font-weight: 600;
        color: rgb(197,201,206);
    }

    .video span {
        color: rgb(89,95,100);
        font-size: 14px;
        font-weight: 600;
    }

    .main-content {
        max-width: 100%;
        width: 100%;
        background-color: rgb(11,14,15);
    }

    .content {
        padding: 30px 28px;
    }

    .content > h1 {
        color: white;
        font-size: 20px;
        font-weight: 700;
    }

    .content-video {
        margin-top: 10px;
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
    }
    .video {
        flex-basis: calc(33.33333333333333% - 10px);
        flex-shrink: 1;
        background-color: white;
        border-radius: 10%;
        object-fit: cover;
        margin-bottom: 25px;
        position: relative;
    }

    @media (max-width: 482px) {
        .video {
            flex-basis: 100%;
        }

    }

.border-line {
    margin-top: 50px;
  position: relative;
  height: 1px;
}

.border-line::after {
  content: "";
  position: absolute;
  top: 50%;
  left: 0;
  width: 100%;
  height: 2px;
  background-color: rgb(36,39,44);
  transform: translateY(-50%);
}


</style>