
<template>
    <div class="list-of-video">
        <div class="category">
            <div class="img-holder">
                <img src="../../assets/gta.webp">
            </div>
            <div class="title">
                <h1>GTA 5</h1>
            </div>
            <div class="desc">
                <h3 style="color: rgb(95,104,104)">100 Viewers</h3>
            </div>
        </div>
        <div class="category">
            <div class="img-holder">
                <img src="../../assets/sleep.webp">
            </div>
            <div class="title">
                <h1>Just Sleeping</h1>
            </div>
            <div class="desc">
                <h3 style="color: rgb(95,104,104)">99 Viewers</h3>
            </div>
        </div>
        <div class="category">
            <div class="img-holder">
                <img src="../../assets/cod.webp">
            </div>
            <div class="title">
                <h1>Call Of Duty</h1>
            </div>
            <div class="desc">
                <h3 style="color: rgb(95,104,104)">600 Viewers</h3>
            </div>
        </div>
        <div class="category">
            <div class="img-holder">
                <img src="../../assets/fornite.webp">
            </div>
            <div class="title">
                <h1>Fortnite</h1>
            </div>
            <div class="desc">
                <h3 style="color: rgb(95,104,104)">120 Viewers</h3>
            </div>
        </div>
        <div class="category">
            <div class="img-holder">
                <img src="../../assets/val.webp">
            </div>
            <div class="title">
                <h1>Valorant</h1>
            </div>
            <div class="desc">
                <h3 style="color: rgb(95,104,104)">200 Viewers</h3>
            </div>
        </div>
        <div class="category">
            <div class="img-holder">
                <img src="../../assets/apex.webp">
            </div>
            <div class="title">
                <h1>Apex Legends</h1>
            </div>
            <div class="desc">
                <h3 style="color: rgb(95,104,104)">2003 Viewers</h3>
            </div>
        </div>
        <div class="category">
            <div class="img-holder">
                <img src="../../assets/ark.webp">
            </div>
            <div class="title">
                <h1>ARK Survival</h1>
            </div>
            <div class="desc">
                <h3 style="color: rgb(95,104,104)">19 Viewers</h3>
            </div>
        </div>
        <div class="category">
            <div class="img-holder">
                <img src="../../assets/ow.webp">
            </div>
            <div class="title">
                <h1>Overwatch 2</h1>
            </div>
            <div class="desc">
                <h3 style="color: rgb(95,104,104)">60 Viewers</h3>
            </div>
        </div>
        <div class="category">
            <div class="img-holder">
                <img src="../../assets/mc.webp">
            </div>
            <div class="title">
                <h1>Minecraft</h1>
            </div>
            <div class="desc">
                <h3 style="color: rgb(95,104,104)">12 Viewers</h3>
            </div>
        </div>
        <div class="category">
            <div class="img-holder">
                <img src="../../assets/csgo.webp">
            </div>
            <div class="title">
                <h1>CS:GO</h1>
            </div>
            <div class="desc">
                <h3 style="color: rgb(95,104,104)">234 Viewers</h3>
            </div>
        </div>
        <div class="category">
            <div class="img-holder">
                <img src="../../assets/lol.webp">
            </div>
            <div class="title">
                <h1>League Game</h1>
            </div>
            <div class="desc">
                <h3 style="color: rgb(95,104,104)">203 Viewers</h3>
            </div>
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

   .list-of-video {
    margin-top: 20px;
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
   }

   .category {
    background-color: transparent;
    flex-basis: 100%; /* change size of flex item to 100% when there is only one item per row */
    display: flex;
    flex-direction: column;
    
    
   }

   .title, .desc {
    max-width: 100%;
   }

   
.img-holder {
    width: 150px;
}

 .img-holder > img {
    border-radius: 10px;
    max-width: 100%;
    object-fit: cover;
    filter: none; /* or any other filter you want to apply initially */
    transition: filter 0.5s ease-in-out; /* add a transition for a smooth effect */
 }
 .img-holder > img:hover {
    filter: hue-rotate(120deg); /* apply a green filter on hover */
    border: 3px solid  #53fc18;
    cursor: pointer;
 }



@media (min-width: 1069px) {
  .category {
    flex-basis: calc(25% - 20px);
  }

  .img-holder {
    width: 100%;
}

 

}

@media (min-width: 1078px) {
  .category {
    flex-basis: calc(20% - 20px);
  }

 

}

@media (min-width: 1252px) {
  .category {
    flex-basis: calc(16.66666666666667% - 20px);
  }

 

}

@media (min-width: 1420px) {
  .category {
    flex-basis: calc(14.28571428571429% - 20px);
  }
}
  

@media (min-width: 1563px) {
  .category {
    flex-basis: calc(12.5% - 20px);
  }
}
  
@media (min-width: 1696px) {
  .category {
    flex-basis: calc(11.11111111111111% - 20px);
  }
}


@media (min-width: 1706px) {
  .category {
    flex-basis: calc(11.11111111111111% - 20px);
  }
}


@media (min-width: 1872px) {
  .category {
    flex-basis: calc(10% - 20px);
  }
}
  
   
   </style>