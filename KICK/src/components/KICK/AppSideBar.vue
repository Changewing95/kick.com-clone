
<template>
    <div class="side-bar" :class="{ mobileSideBarWidth : state.mobileView  }">
        <div class="recommended-div" :class="{ mobileViewCSS : state.mobileView  }">
            <h1>Recommended</h1>
            <div class="object">
                <h1>Click</h1>
            </div>
        </div>
        <div class="user-row" v-for="(object, index) in listOfStreamer" :key="index">
            <div class="user-profile">
                <img :src="object.img" />

            </div>
            <div class="user-name" :class="{ mobileViewCSS : state.mobileView  }">
                <div class="username">
                    <h1>{{object.username}}</h1>
                </div>
                <div class="game">
                    <h3>{{object.game}}</h3>
                </div>
            </div>
            <div class="user-view" :class="{ mobileViewCSS : state.mobileView  }">
                <h3>{{object.viewers}}</h3>
            </div>
        </div>
    </div>
</template>


<script setup>
import { reactive, onMounted } from 'vue';
import gm from '../../assets/GM.webp'
import gm2 from '../../assets/2.webp'
import gm3 from '../../assets/3.webp'
import xqc from '../../assets/xqc.jpg'


var listOfStreamer = [
    {
        username: "GMHikaru",
        game: "Chess",
        viewers: 232,
        img: gm
    },
    {
        username: "Stephen",
        game: "Fortnite",
        viewers: 1500,
        img: gm2
    },
    {
        username: "Gamer1",
        game: "Call Of Duty",
        viewers: 1000,
        img: gm3
    },
    {
        username: "xqc",
        game: "Just Chatting",
        viewers: 10,
        img: xqc

    },
]

var state = reactive({
    mobileView : false
})

function handleView() {
    state.mobileView = window.innerWidth <= 597
}

onMounted(() => {
    handleView()
    window.addEventListener('resize', handleView);
})

</script>

<style scoped>
    h1 {
        color: white;
    }
    .side-bar {
        background-color: rgb(25,27,31);
        height: auto;
        width: 298px;
        display: flex;
        flex-direction: column;
        padding: 16px;
    }

    .recommended-div h1 {
        font-weight: 800;
        font-size: 13px;
    }

    .recommended-div {
        display: flex;
        justify-content: space-between;
    }

    .user-profile {
        width: 40px;
        height: 40px;
        overflow: hidden;
        max-width: 100%;
    }

    .user-row {
        display: flex;
        margin-top: 10px;
        padding: 6px;
    }

    .user-row:hover {
        background-color: rgb(36,39,44);
        border-radius: 5px;
        cursor: pointer;
    }

    .user-profile > img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 50%;
    filter: none; /* or any other filter you want to apply initially */
    transition: filter 0.5s ease-in-out; /* add a transition for a smooth effect */
}


 
.user-name {
    display: flex;
    flex-direction: column;
    margin-left: 10px;
}

.user-name h1 {
    font-size: 15px;
    font-weight: 800;
}

.game > h3 {
    font-size: 14px;
    color: #bcbcc3;
    font-weight: 500;
}

.user-view {
    margin-left: auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    
}

.user-view > h3 {
    font-size: 14px;
    color: white;
    font-weight: 500;


}

.mobileViewCSS {
    display: none;
}

.mobileSideBarWidth {
    width: 90px;
}



</style>