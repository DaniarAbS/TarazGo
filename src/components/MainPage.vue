<template>
  <div>
    <!-- Hamburger Icon -->

    <!-- Sidebar -->
    <div class="sidebar" v-if="showSidebar">
      <!-- Close Button -->
      <div class="close-icon" @click="showSidebar = false">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="orange" class="bi bi-x-square-fill" viewBox="0 0 16 16">
          <path d="M2 0a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2zm3.354 4.646L8 7.293l2.646-2.647a.5.5 0 0 1 .708.708L8.707 8l2.647 2.646a.5.5 0 0 1-.708.708L8 8.707l-2.646 2.647a.5.5 0 0 1-.708-.708L7.293 8 4.646 5.354a.5.5 0 1 1 .708-.708"/>
        </svg>
      </div>

      <!-- Sidebar Content -->
      <p>Sidebar Content Here</p>
    </div>
    <section class="head">
        <div class="mainBgCont">
        <img class="mainbg" src="../assets/mainbg.png" alt="">
        <div class="hamburger-icon" @click="showSidebar = true">
          <img class="hamburger-img" src="../assets/hamburger-icon.png" alt="">
        </div>
        <p class="mainTxt">TarazGo</p>
        </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showSidebar: false,
    };
  },
};
</script>

<style scoped>
.hamburger-icon {
  position: absolute;
  top: 40%;
  left: 10%;
  transform: translate(-50%, -50%);
  cursor: pointer;
  padding: 1rem;
  background-color: rgba(255, 254, 254, 0.5);
  border-radius: 1rem;
  z-index: 10;
}

.hamburger-img{
  width: 3rem;
  opacity: 1;
}

.sidebar {
  position: fixed;
  display: flex;
  flex-direction: column;
  top: 0;
  left: 0;
  width: 250px;
  height: 100%;
  background-color: #aba7a7;
  color: white;
  padding: 20px;
  z-index: 999;
}

.close-icon {
  position: absolute;
  top: 20px;
  right: 20px;
  cursor: pointer;
}

.close-img{
  width: 2rem;
}

.head {
  position: relative;
}

.mainBgCont {
  position: relative;
  display: flex;
  justify-content: center;
}

.mainbg {
  width: 100%;
  height: auto;
  display: block;
}

.mainTxt {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
  font-size: 6vw; 
  font-weight: bold;
  text-align: center;
  max-width: 90%;
}
</style>