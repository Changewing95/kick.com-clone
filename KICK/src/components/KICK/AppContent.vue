
<template>
    <div class="main-content">
        <div class="content">
            <h1>Featured Streams</h1>
            <div class="content-video">
                <div class="video">xqc</div>
                <div class="video">xqc</div>
                <div class="video">xqc</div>
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
        height: 200px;
        flex-shrink: 1;
        background-color: white;
        border-radius: 5px;
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