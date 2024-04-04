<script setup>
import { ref } from 'vue'
const index = ref(1)
const nextSlide = () => {
  const slider = document.querySelector('.slider__footer__Wrapp')
  if (index.value === 5) {
    index.value = 1
  } else {
    index.value++
  }
  if (index.value === 1) {
    slider.style.left = 0 + '%'
  }
  if (index.value === 2) {
    slider.style.left = -400 + 'px'
  }
  if (index.value === 3) {
    slider.style.left = -800 + 'px'
  }
  if (index.value === 4) {
    slider.style.left = -1200 + 'px'
  }
  if (index.value === 5) {
    slider.style.left = -1570 + 'px'
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
      <div class="slider__footer__Wrapp">
        <div class="slider__block">
          <div class="slide">
            <div class="slide__img"><img src="/src/assets/img/footer-slide-1.png" alt="" /></div>
            <div class="slide__wrapp">
              <div class="slide__title">
                <div class="price">149.00<p class="del">155.000</p></div>
                <b>Combo Revo Đậm Đà</b>
                <p>Hàm lượng caffein trong Revo Đậm Đà đủ mạnh để làm bạn tỉnh táo làm việc...</p>
              </div>
              <div class="slide__btn">
                <button>MUA NGAY</button>
                <span>CHI TIẾT</span>
              </div>
            </div>
          </div>
          <div class="slide">
            <div class="slide__img"><img src="/src/assets/img/footer-slide-2.png" alt="" /></div>
            <div class="slide__wrapp">
              <div class="slide__title">
                <div class="price">156.00<p class="del">165.000</p></div>
                <b>Combo Revo Everyday</b>
                <p>Revo Everyday được phối trộn giữa vị đắng của hạt Robusta và hương thơm...</p>
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
            <div class="slide__img"><img src="/src/assets/img/footer-slide-3.png" alt="" /></div>
            <div class="slide__wrapp">
              <div class="slide__title">
                <div class="price">142.00<p class="del">148.000</p></div>
                <b>Combo Revo Honey</b>
                <p>Honey – trong tên gọi Revo Honey đến từ phương pháp chế biến hạt Arabica...</p>
              </div>
              <div class="slide__btn">
                <button>MUA NGAY</button>
                <span>CHI TIẾT</span>
              </div>
            </div>
          </div>
          <div class="slide">
            <div class="slide__img"><img src="/src/assets/img/footer-slide-2.png" alt="" /></div>
            <div class="slide__wrapp">
              <div class="slide__title">
                <div class="price">139.00<p class="del">145.000</p></div>
                <b>Combo Revo Honey</b>
                <p>Revo Everyday được phối vị đắng của hạt Robusta và hương thơm...</p>
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
            <div class="slide__img"><img src="/src/assets/img/footer-slide-2.png" alt="" /></div>
            <div class="slide__wrapp">
              <div class="slide__title">
                <div class="price">169.00<p class="del">175.000</p></div>
                <b>Combo Revo Honey</b>
                <p>Revo Everyday được phối trộn giữa vị đắng của hạt Robusta và hương thơm...</p>
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
.next {
  width: 45px;
  cursor: pointer;
  position: absolute;
  right: 100px;
  top: 290px;
  padding: 7px;
  box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.1);
  background: rgb(199, 161, 122);
  border-radius: 50%;
  z-index: 15;
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
  right: 0;
  bottom: 0;
  width: 25%;
  background-color: var(--Primary-Color);
}
.slider__footer__Wrapp {
  transition: 0.5s;
  display: flex;
  column-gap: 30px;
  position: relative;
  left: 0%;
  padding: 15px;
}
.slider__block {
  display: flex;
  gap: 30px;
}
.slide {
  display: flex;
  flex-direction: column;
  background-color: #fff;
  cursor: pointer;
  transition: .5s;
  justify-content: space-between;
}
.slide:hover{
    box-shadow: 0 0 15px 5px rgba(0, 0, 0, 0.075);
}
.slide__wrapp {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 25px;
}
.slide__title {
  display: flex;
  flex-direction: column;
  gap: 25px;
  padding: 25px;
  font-size: 18px;
  height: 210px;
}
.price {
  color: orange;
  display: flex;
  gap: 15px;
  align-items: flex-end;
  
}
.del {
    text-decoration: line-through;
    color: black;
    font-style: italic;
    font-size: 15px;
}
.slide__btn {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 15px;
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
@media (max-width:1322px) {
  .wrapps {
    width: 1000px;
  }
}
@media (max-width: 1020px) {
  .wrapps {
    width: 700px;
  }
}
@media (max-width: 720px) {
  .wrapps {
    width: 360px;
  }
  .next {
    right: 0;
  }
  .decoration {
    display: none;
  }
}
</style>
