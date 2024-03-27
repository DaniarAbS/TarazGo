<template>
  <div>
    <!-- Hamburger Icon -->

    <!-- Sidebar -->
    <div class="sidebar" v-if="showSidebar">
      <!-- Close Button -->
      <div class="close-icon" @click="showSidebar = false">
        <button type="button" class="btn-close" aria-label="Close"></button>
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
  background-color: rgba(128, 128, 128, 0.5);
  border-radius: 1rem;
  z-index: 10;
}

.hamburger-img{
  width: 3rem;
  opacity: 1;
}

.sidebar {
  position: fixed;
  top: 0;
  left: 0;
  width: 250px;
  height: 100%;
  background-color: #333;
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