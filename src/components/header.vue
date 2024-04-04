<script setup>
import { ref } from 'vue'
let isActive = ref(false)

function HeaderMenu() {
  isActive.value ? (isActive.value = false) : (isActive.value = true)
}
</script>

<template>
  <header class="header">
    <div @click="HeaderMenu" 
    :class="{ open: isActive }"
     class="close__header__btn">
      <button :class="{ open: isActive }"></button>
    </div>
    <div class="left__col">
      <div class="left__col__logo"><img src="/src/assets/img/revologo.png" alt="revologo" /></div>
      <div class="left__col__title">  
        <p class="your">YOUR</p>
        <p class="h1-bg">PERSONALIZED</p>
        <p class="coffe">COFFEE</p>
      </div>
    </div>
    <div class="middle__col">
    </div>
    <div :class="{ active: isActive }" class="right__col">
      <div class="right__col__nav">
        <div class="cart">
          <img src="/src/assets/img/cart.png" alt="" />
          <p class="count__cart">2</p>
        </div>
        <div class="nav">
          <h3>TRANG CHỦ</h3>
          <ul>
            <li><a href="#">COFFEE</a></li>
            <li><a href="#">PHIN MẠ MÀU</a></li>
            <li><a href="#">COMBO PHIN PHÊ</a></li>
            <li><a href="#">GIFTSET</a></li>
            <li><a href="#">LIÊN HỆ</a></li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped>
.close__header__btn button {
  z-index: 15;
  width: 70px;
  height: 4px;
  background: var(--Accent-Color);
  border: none;
  position: absolute;
  right: 30px;
  top: 40px;
  cursor: pointer;
}
.close__header__btn {
  display: none;
}
.close__header__btn button::before {
  display: block;
  content: '';
  width: 70px;
  height: 4px;
  background: var(--Accent-Color);
  border: none;
  position: relative;
  top: 8px;
  transition: 0.3s ease-in-out;
}
.close__header__btn button::after {
  display: block;
  content: '';
  width: 70px;
  height: 4px;
  background: var(--Accent-Color);
  border: none;
  position: relative;
  top: 12px;
  transition: 0.3s ease-in-out;
}

.header {
  display: flex;
  height: 768px;
  overflow: hidden;
}
.left__col {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  background-color: var(--Light-gray);
  padding: 75px 0;
  flex: 1;
}
.left__col__logo {
  cursor: pointer;
}
.left__col__title {
  font-size: 54px;
  font-weight: bold;
  color: var(--Primary-Color);
  position: relative;
  left: 25%;
}
.your {
  animation: run-y 3s 1s ease forwards;
  position: relative;
  left: -150%;
}
@keyframes run-y {
  0% {
    left: -100%;
    opacity: 0.3;
  }
  25% {
    left: 50%;
    opacity: 0.8;
  }
  100% {
    left: 0%;
    opacity: 1;
  }
}
@keyframes run-bg {
  0% {
    left: -100%;
    opacity: 0.3;
  }
  25% {
    left: 50%;
    opacity: 0.8;
  }
  100% {
    left: 0%;
    opacity: 1;
    color: #fff;
    background-color: var(--Accent-Color);
  }
}
.h1-bg {
  position: relative;
  left: -150%;
  animation: run-bg 2s 2.5s forwards;
  padding: 0 15px;
}
.coffe {
  position: relative;
  left: -150%;
  animation: run-y 2s 2s ease forwards;
}
.middle__col {
    background: url('/src/assets/img/video.png')50% / cover no-repeat;
    width: 50%;
    height: 100%;
}
.right__col {
    flex: 1;
  font-family: 'Nunito', sans-serif;
  background-color: var(--Primary-Color);
  display: flex;
  flex-direction: column;
}
.right__col__nav {
  display: flex;
  flex-direction: column;
  gap: 95px;
  padding: 75px 60px;
}
.cart {
  display: flex;
  position: relative;
  width: 35px;
}
.count__cart {
  position: absolute;
  right: -5px;
  top: -10px;
  background-color: var(--Accent-Color);
  border-radius: 50%;
  padding: 1px 6px;
  color: #fff;
  font-size: 14px;
}
.nav {
  display: flex;
  flex-direction: column;
  gap: 25px;
  color: #fff;
}
ul li {
  margin-bottom: 35px;
}
.nav a {
  color: #fff;
  font-weight: 100;
  position: relative;
  width: 100%;
}
.nav a::before {
  transition: 0.4s;
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 0%;
  height: 2px;
  background-color: var(--Accent-Color);
}
.nav a:hover:before {
  width: 100%;
}

@media (max-width: 1280px) {
  .right__col {
    transition: .5s;
    position: fixed;
    left: -500px;
    top: 0;
    bottom: 0;
    z-index: 15;
  }
  header{
    flex-direction: column;

  }
  .left__col{
    padding: 25px 15px 75px 15px;
    align-items: start;
  }
  .middle__col {
    width: 100%;
  }
  .left__col__title {
    left: 0;
  }
  .active {
    left: 0;
  }
  .close__header__btn {
    display: block;
  }
  .close__header__btn .open{
    background: 0 0;
    position: absolute;
  }
  .close__header__btn .open::before {
    width: 30px;
    transform: rotate(40deg);
    right: -17px;
    top: 19px;
}
.close__header__btn .open::after {
    width: 30px;
    transform: rotate(-40deg);
    right: -16px;
    top: 15px;
}
}

@media (max-width: 511px) {
  .left__col__title{
    font-size: 36px;
  }
}
</style>
