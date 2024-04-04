<script setup>
import { ref } from 'vue'

let showNum = ref(1)

const checkActive = (e) => {
  const buttons = document.querySelectorAll('.btn-1, .btn-2, .btn-3')
  for (let button of buttons) {
    if (button.classList.contains(e.target.classList[0])) {
      button.classList.add('active')
      showNum.value = Number(button.textContent)
    } else {
      button.classList.remove('active')
    }
  }
}
</script>

<template>
  <div class="best__block">
    <div class="decoration"></div>
    <div class="best__body">
      <div class="best__title">
        <p>Best Gift For Best Friend</p>
        <h1>GIFTSET</h1>
      </div>
      <!-- таб -->
      <div class="best__tabs">
        <!-- картинка таба -->
        <div class="wrapp">
          <div v-show="showNum === 1" class="best__img"><img src="/src/assets/img/slide-1.png" alt="" /></div>
          <div v-show="showNum === 2" class="best__img"><img src="/src/assets/img/slide-2.png" alt="" /></div>
          <div v-show="showNum === 3" class="best__img"><img src="/src/assets/img/slide-3.png" alt="" /></div>
          <!-- текст таба -->
          <div class="best__tabs__body">
            <div class="best__tabs__price"><p>285.000</p></div>
            <div class="best__tabs__title"><b>Giftset "Cà phê phin Việt Nam"</b></div>
            <div class="best__tabs__text">
              <p>
                Món quà tuyệt vời dành cho người sành cà phê. Hạt cà phê được Revo cẩn trọng chọn
                lựa, rang xay theo công nghệ và bí quyết học hỏi từ những nghệ nhân nổi tiếng, cùng
                với tình yêu, sự đam mê của người làm cà phê… tạo ra những tách cà phê tinh khiết
                chỉ dành riêng cho bạn.
              </p>
            </div>
            <div class="best__tabs__info">
              <div class="best__tabs__info__left tabs-i">
                <img src="/src/assets/img/coffee-beans.png" alt="coffee-beans" />
                <div class="text">
                  <p>Loại hạt</p>
                  <b>Fine Robusta Blend</b>
                </div>
              </div>
              <div class="best__tabs__info__right tabs-i">
                <img src="/src/assets/img/mountain.png" alt="mountain" />
                <div class="text">
                  <p>Độ cao</p>
                  <b>700 - 800m</b>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- текст таба -->

        <!-- кнопки таба -->
        <div class="best__tabs__btn">
          <button @click="checkActive" class="active btn-1">1</button>
          <button @click="checkActive" class="btn-2">2</button>
          <button @click="checkActive" class="btn-3">3</button>
        </div>
        <!-- кнопки таба -->
      </div>
      <!-- таб -->
    </div>
  </div>
</template>

<style scoped>
.best__block {
  background-color: var(--bold-gray);
  position: relative;
  z-index: 1;
}
.decoration {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  width: 650px;
  background-color: var(--Light-gray);
  z-index: -1;
}
.best__body {
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 68px;
  text-align: center;
  padding: 86px 25px;
  z-index: 10;
}
.best__title {
  color: var(--Primary-Color);
  font-weight: 500;
}
.wrapp {
  display: flex;
  padding: 65px 50px;
}

.best__tabs {
  z-index: 10;
  background: #fff;
  width: 850px;
  text-align: left;
  display: flex;
  justify-content: space-between;
  position: relative;
  left: 130px;
  font-family: 'Nunito', sans-serif;
}
.best__img img {
  position: relative;
  left: -150px;
  width: 250px;
}

.best__tabs__price {
  color: rgb(199, 161, 122);
  font-size: 20px;
  margin-bottom: 12px;
}
.best__tabs__title {
  color: var(--Primary-Color);
  font-size: 24px;
  margin-bottom: 12px;
}
.best__tabs__text {
  color: var(--Primary-Color);
  font-size: 16px;
  margin-bottom: 24px;
}
.best__tabs__info {
  display: flex;
  justify-content: space-between;
}
.tabs-i {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 15px;
}
.best__tabs__btn {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background: rgb(237, 240, 245);
  width: 88px;
  box-shadow: 8px -2px 11px -9px rgba(34, 60, 80, 0.459) inset;
}
.best__tabs__btn button {
  color: rgb(65, 81, 103);
  font-weight: 900;
  background: rgb(237, 240, 245);
  font-family: Montserrat;
  font-size: 30px;
  width: 100px;
  height: 100%;
  border: none;
  cursor: pointer;
  opacity: 0.3;
}
.best__tabs__btn button.active {
  transition: 0.4s;
  box-shadow: 8px -2px 11px -9px rgba(34, 60, 80, 0.329) inset;
  background-color: #fff;
  opacity: 1;
}

@media (max-width: 1308px) {
  .wrapps {
    width: 950px;
  }
  .decoration {
    width: 25%;
  }
  .best__tabs {
    position: relative;
  }
  .best__tabs__btn {
    flex-direction: row;
    width: 230px;
    height: 80px;
    position: absolute;
    left: 0;
    top: -80px;
  }
  .best__img img {
    position: relative;
    left: 0;
    right: 0;
  }
  .best__tabs {
    width: 620px;
    left: 0;
  }
  .best__body {
    align-items: normal;
  }
  .wrapp {
    display: flex;
    flex-direction: column;
    padding: 30px 25px;
  }
}
@media (max-width: 662px) {
  .best__tabs {
    width: 350px;
    left: 0;
  }
  .best__title{
    margin-bottom: 50px;
  }
}
@media (max-width: 380px) {
  .best__tabs {
    width: 300px;
    left: 0;
  }
  .best__title{
    margin-bottom: 50px;
  }
}
</style>
