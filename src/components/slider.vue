<script setup>
import { ref } from 'vue'
const index = ref(1)
const nextSlide = () => {
  const slider = document.querySelector('.slider__Wrapp')
  if (index.value === 4) {
    index.value = 1
  } else {
    index.value++
  }
  if (index.value === 1) {
    slider.style.left = 0 + '%'
  }
  if (index.value === 2) {
    slider.style.left = -350 + 'px'
  }
  if (index.value === 3) {
    slider.style.left = -700 + 'px'
  }
  if (index.value === 4) {
    slider.style.left = -1050 + 'px'
  }
}

</script>

<template>
  <div class="slider">
    <div class="decoration"></div>
    <div class="slider__title">
      <p>Choose Your Favorite</p>
      <b>CHUẨN GU ĐÚNG VỊ</b>
    </div>
    <div class="wrapps">
      <img @click="nextSlide" src="/src/assets/img/arrow-right.png" alt="next" class="next" />
      <div class="slider__Wrapp">
        <div class="slider__block">
          <div class="slide">
            <div class="slide__img"><img src="/src/assets/img/slide-1.png" alt="" /></div>
            <div class="slide__wrapp">
              <div class="slide__title">
                <p class="price">99.00</p>
                <b>REVO Morning</b>
                <p>đắng, hậu ngọt, hương hoa</p>
              </div>
              <div class="slide__btn">
                <button>MUA NGAY</button>
                <span>CHI TIẾT</span>
              </div>
            </div>
          </div>
          <div class="slide">
            <div class="slide__img"><img src="/src/assets/img/slide-2.png" alt="" /></div>
            <div class="slide__wrapp">
              <div class="slide__title">
                <p class="price">99.00</p>
                <b>REVO Morning</b>
                <p>đắng, hậu ngọt, hương hoa</p>
              </div>
              <div class="slide__btn">
                <button>MUA NGAY</button>
                <span>CHI TIẾT</span>
              </div>
            </div>
          </div>
        </div>
        <div class="slider__block">
          <div class="slide">
            <div class="slide__img"><img src="/src/assets/img/slide-3.png" alt="" /></div>
            <div class="slide__wrapp">
              <div class="slide__title">
                <p class="price">99.00</p>
                <b>REVO Morning</b>
                <p>đắng, hậu ngọt, hương hoa</p>
              </div>
              <div class="slide__btn">
                <button>MUA NGAY</button>
                <span>CHI TIẾT</span>
              </div>
            </div>
          </div>
          <div class="slide">
            <div class="slide__img"><img src="/src/assets/img/slide-4.png" alt="" /></div>
            <div class="slide__wrapp">
              <div class="slide__title">
                <p class="price">99.00</p>
                <b>REVO Morning</b>
                <p>đắng, hậu ngọt, hương hoa</p>
              </div>
              <div class="slide__btn">
                <button>MUA NGAY</button>
                <span>CHI TIẾT</span>
              </div>
            </div>
          </div>
        </div>
        <div class="slider__block">
          <div class="slide">
            <div class="slide__img"><img src="/src/assets/img/slide-1.png" alt="" /></div>
            <div class="slide__wrapp">
              <div class="slide__title">
                <p class="price">99.00</p>
                <b>REVO Morning</b>
                <p>đắng, hậu ngọt, hương hoa</p>
              </div>
              <div class="slide__btn">
                <button>MUA NGAY</button>
                <span>CHI TIẾT</span>
              </div>
            </div>
          </div>
          <div class="slide">
            <div class="slide__img"><img src="/src/assets/img/slide-1.png" alt="" /></div>
            <div class="slide__wrapp">
              <div class="slide__title">
                <p class="price">99.00</p>
                <b>REVO Morning</b>
                <p>đắng, hậu ngọt, hương hoa</p>
              </div>
              <div class="slide__btn">
                <button>MUA NGAY</button>
                <span>CHI TIẾT</span>
              </div>
            </div>
          </div>
        </div>
        <div class="slider__block">
          <div class="slide">
            <div class="slide__img"><img src="/src/assets/img/slide-1.png" alt="" /></div>
            <div class="slide__wrapp">
              <div class="slide__title">
                <p class="price">99.00</p>
                <b>REVO Morning</b>
                <p>đắng, hậu ngọt, hương hoa</p>
              </div>
              <div class="slide__btn">
                <button>MUA NGAY</button>
                <span>CHI TIẾT</span>
              </div>
            </div>
          </div>
          <div class="slide">
            <div class="slide__img"><img src="/src/assets/img/slide-3.png" alt="" /></div>
            <div class="slide__wrapp">
              <div class="slide__title">
                <p class="price">99.00</p>
                <b>REVO Morning</b>
                <p>đắng, hậu ngọt, hương hoa</p>
              </div>
              <div class="slide__btn">
                <button>MUA NGAY</button>
                <span>CHI TIẾT</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.wrapps {
  overflow: hidden;
  width: 1300px;
  position: relative;
}
.slider {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 125px 0;
  overflow: hidden;
  position: relative;
  background-color: #edf0f54f;
}
.slider__title {
  display: flex;
  flex-direction: column;
  text-align: center;
  align-items: center;
  justify-content: center;
  margin-bottom: 75px;
}
.slider__title p {
  color: rgb(65, 81, 103);
  font-size: 20px;
}
.slider__title b {
  color: rgb(65, 81, 103);
  font-size: 30px;
  font-weight: 900;
}
.decoration {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 35%;
  background-color: var(--Primary-Color);
}
.slider__Wrapp {
  transition: 0.5s;
  display: flex;
  column-gap: 45px;
  position: relative;
  left: 0%;
}
.slider__block {
  display: flex;
  flex-direction: column;
  gap: 35px;
}
.slide {
  display: flex;
  background-color: #fff;
  width: 550px;
  height: 256px;
}
.slide__img {
  height: 255px;
}
.slide__wrapp {
  display: flex;
  flex-direction: column;
  gap: 25px;
}
.slide__title {
  display: flex;
  flex-direction: column;
  gap: 25px;
  padding: 25px;
  font-size: 18px;
}
.price {
  color: orange;
}
.slide__btn {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 15px;
}
.slide__btn button {
  border-radius: 19px;
  background: rgb(199, 161, 122);
  border: none;
  padding: 5px 15px;
  color: #fff;
  font-weight: 400;
}
.slide__btn span {
  color: var(--Primary-Color);
  font-weight: bold;
}
.next {
  width: 45px;
  cursor: pointer;
  position: absolute;
  right: 60px;
  top: 250px;
  padding: 7px;
  box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.1);
  background: rgb(199, 161, 122);
  border-radius: 50%;
  z-index: 15;
}

@media (max-width: 1308px) {
  .wrapps {
    width: 950px;
  }
  .decoration {
    width: 25%;
  }
}
@media (max-width: 1020px) {
  .wrapps {
    width: 700px;
  }
}
@media (max-width: 720px) {
  .slide {
    display: block;
    width: 100%;
    height: 100%;
    padding: 15px 35px;
  }
  .wrapps {
    width: 300px;
  }
  .next {
    right: 0px;
    top: 350px;
  }
  .decoration {
    display: none;
  }
}
</style>
