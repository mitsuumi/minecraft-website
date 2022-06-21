<template>
    <div class="container-fluid indexbg">
    <div class="row d-flex flex-column text-center">
      <div class="col webtitle">
        <h1 class="display-1 fw-bold">2022麥塊建築大賽</h1>
      </div>
      <div class="col navposition" id="navbar">
        <div class="burgar p-3">
          <i class="bi bi-list"></i>
        </div>
        <nav>
          <ul class="col menu overflow-hidden fs-3 fw-bold">
            <li><router-link to="/">首頁</router-link></li>
            <li><router-link to="/about">關於</router-link></li>
            <li><router-link to="/products">比賽周邊</router-link></li>
            <li><router-link to="/mineVerse">元宇宙商圈</router-link></li>
          </ul>
          <router-view/>
        </nav>
      </div>
      <div class="col position-absolute bottom-0 start-0">
        <img :src="image" class="img-fluid" alt="minecraft">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainNavbar',
  data() {
    return {
      image: require('@/assets/minecraftserver.png'),
    };
  },
};
</script>

<style scoped>
/* title */

.indexbg {
background: url('@/assets/bg/2022-04-22_02.44.16.png') no-repeat center / cover;
height: 100vh;

}

h1{
  margin-top: 180px;
}

nav ul {
display: flex;
justify-content: center;
overflow: hidden;
}

nav a{
display: inline-block;
width: 200px;
height: 70px;
padding: 15px 0 15px 0;
color: rgb(255, 255, 255);
}

nav a:hover{
color: rgb(255, 255, 255);
border-bottom: 3px solid yellow;
}

.burgar{
color: var(--white);
font-size: 1.5rem;
display:none;
}

.sticky{
position: fixed;
top:0;
background:rgba(0, 0, 0,0.7);
transition:0.5s;
z-index: 1;
}

.sticky a{
color:white;
}

.sticky a:hover{
  color:white;
}

.navposition {
  position: relative;
  top: 370px;
}

</style>
