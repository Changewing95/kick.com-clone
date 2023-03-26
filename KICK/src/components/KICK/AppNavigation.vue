<template>
    <div class="nav-container">
        <div class="navigation-bar">
        <div class="logo">
            <div class="img-holder">
                <img src="../../assets/kick.png">
            </div>
            <div class="browse" :class="{ searchMenuIsMobile: state.mobileView }">
                <h1>browse</h1>
            </div>
        </div>
        <div class="search_menu" :class="{ searchMenuIsMobile: state.mobileView }">
            <input type="text"  placeholder="search">
        </div>
        <div class="login-sign-in">
            <button  class="login">Log in</button>
            <button   class="signup">Sign up</button>
        </div>
    </div>
    </div>
</template>

<script setup>

import { reactive, onMounted } from 'vue';

const state = reactive({
  mobileView: false,
});

function handleView() {
  state.mobileView = window.innerWidth <= 748;
}

onMounted(() => {
  handleView();
  window.addEventListener('resize', handleView);
});







</script>


<style scoped>

.nav-container {
    width: 100%;
    background-color: rgb(36,39,44);
}

.navigation-bar {
    background-color: rgb(36,39,44);
    height: 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-left: 11px;
    margin-right: 32px;
}

.navigation-bar h1 {
    margin: 0;
}



.login-sign-in {
    display: flex;
    justify-content: end;
}


.login {
    background-color: transparent;
    border: none;
    color: white;
    font-size: 17px;
    font-weight: 700;
}

.signup {
    background-color: #53fc18;
    border: none;
    color: black;
    font-size: 17px;
    font-weight: 700;
    padding: 8px 10px;
    border-radius: 5px;
    text-transform: capitalize;
}

.login-sign-in > .login {
    margin-right: 32px;
}

.search-button {
    width: 100%;
}

input {
    background-color: rgb(25,27,31);
    padding: 12px 120px 8px 25px;
    border: transparent;
    border-radius: 4px;
}

.searchMenuIsMobile {
    display: none;
}



.logo {
    display: flex;
    align-items: center;
    text-align: center;
}



.browse {
    margin-left: 10px;
}

.browse h1 {
    font-size: 2rem; /* adjust to your desired font size */
    color: white;
    text-transform: capitalize;
    font-size: 17px;
    font-weight: 700;
}



.img-holder {
    width: 100px;
}
.img-holder > img {
    max-width: 100%;
}


</style>