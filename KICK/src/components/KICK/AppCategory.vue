
<template>
 <div class="first-row">
    <div class="category">
        <h1>Category</h1>
    </div>
    <div class="live-channels">
        <h1>Live Channels</h1>
    </div>
    <div class="clips">
        <h1>Clips</h1>
    </div>
 </div>
</template>


<script setup>
</script>

<style scoped>

h1  {
    font-weight: 700;
    font-size: 18px;
    color: white;
}

.first-row {
    margin-top: 30px;
    display: flex;
}
.first-row > div {
    margin-right: 10px;
    cursor: pointer;
}

.category-title > h1 {
    color: white;
        font-size: 20px;
        font-weight: 700;
}

</style>