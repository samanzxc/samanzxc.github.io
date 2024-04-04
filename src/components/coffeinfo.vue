<script setup>

</script>

<template>
    <div class="coffe__info__wrapp">
        <div class="coffe__info__block">
            <div class="coffe__info__title">
                <p>Your Personalized Coffee</p>
                <h1>COFFEE BUILD YOUR BASE</h1>
            </div>
            <div class="coffe__info__card">
                <div class="card">
                    <div class="card__img"><img src="/src/assets/img/coffe-1.png" alt="coffe"></div>
                    <div class="txt">
                    <div class="card__title"><b>Nguồn gốc</b></div>
                    <div class="card__text"><p>Những hạt cà phê Arabica, Robusta đạt chất lượng theo tiêu chuẩn quốc tế.</p></div>
                    </div>
                </div>

                <div class="card">
                    <div class="card__img"><img src="/src/assets/img/coffe-2.png" alt="coffe"></div>
                    <div class="txt">
                    <div class="card__title"><b>Chất lượng</b></div>
                    <div class="card__text"><p>Từng một hạt cà phê là cả một quá trình tập trung cao độ của nghệ nhân cà phê.</p></div>
                    </div>
                </div>

                <div class="card">
                    <div class="card__img"><img src="/src/assets/img/coffe-3.png" alt="coffe"></div>
                    <div class="txt">
                    <div class="card__title"><b>Các loại hạt</b></div>
                    <div class="card__text"><p>70% chất lượng tách cà phê đến từ nguồn gốc và chất lượng green bean.</p></div>
                    </div>
                </div>

                <div class="card">
                    <div class="card__img"><img src="/src/assets/img/coffe-4.png" alt="coffe"></div>
                    <div class="txt">
                    <div class="card__title"><b>Pha chế</b></div>
                    <div class="card__text"><p>Những hạt cà phê được lột xác qua quá trình rang xay kỹ lưỡng và nghiêm ngặt.</p></div>
                </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.coffe__info__wrapp {
    padding: 130px 150px;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: var(--Light-gray);
}
.coffe__info__block {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}
.coffe__info__title {
    color: var(--Primary-Color);
    margin-bottom: 75px;
}
.coffe__info__card {
    display: flex;
}
.card {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.txt {
display: flex;
flex-direction: column;
align-items: center;
row-gap: 10px;
margin-top: 40px;
}

.card__text {
    width: 60%;
}


@media (max-width: 1280px){
    .card {
        max-width: 200px;
        max-height: 230px;
    }
    .coffe__info__wrapp{
        padding: 50px 5%;
    }
    .txt {
        margin-top: 5px;
    }
}
@media (max-width:  735px){
    .coffe__info__card{
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
        row-gap: 25px;
    }
    .coffe__info__wrapp{
        padding: 50px 2%;
    }
}
</style>