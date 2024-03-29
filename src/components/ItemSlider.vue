<template>
    <div class="row justify-content-between" style="margin: 2rem 0;">
        <div class="col-4" style="font-size: 1rem; font-weight: bold;">
            Общайтесь с нашим ботом
        </div>
        <div class="col-4">
            <button type="button" class="btn btn-primary" style="background-color: orange; width: 8rem;">Чат</button>
        </div>
    </div>

    <div class="container text-center">
        <div class="row">
            <div class="col-9">Категорий</div>
            <div class="slider-container">
                <div class="slide">
                    <img src="../assets/ic_nature.png" alt="Nature">
                    <p>Природа</p>
                </div>
                <div class="slide">
                    <img src="../assets/ic_shopping_cart.png" alt="Shopping">
                    <p>Шоппинг</p>
                </div>
                <div class="slide">
                    <img src="../assets/ic_restaurant.png" alt="Restaurants">
                    <p>Рестораны</p>
                </div>
                <div class="slide">
                    <img src="../assets/ic_attraction.png" alt="Attractions">
                    <p>Аттракционы</p>
                </div>
                <div class="slide">
                    <img src="../assets/ic_events.png" alt="Events">
                    <p>Мероприятие</p>
                </div>
                <div class="slide">
                    <img src="../assets/ic_history.png" alt="History">
                    <p>История</p>
                </div>
            </div>
        </div>
    </div>

    <div class="row justify-content-between" style="margin: 2rem;">
        <div class="col-4" style="font-size: 1rem; font-weight: bold;">
            Самые посящаемые
        </div>
        <div class="col-4">
            Подробнее
        </div>
    </div>

    <div class="container text-center">
        <div class="row align-items-center" style="margin: 2rem 0;">
            <router-link to="/karahan" class="col" exact href="#">
                    <img  @click="handleNav" src="../assets/karahan.png" class="rounded float-start" alt="...">
            </router-link>
            <div class="col">
                <img src="../assets/east_sauna.png" class="rounded float-start" alt="...">
            </div>
        </div>
    </div>
    
    <div class="row justify-content-between" style="margin: 2rem;">
        <div class="col-4" style="font-size: 1rem; font-weight: bold;">
            Сервисы
        </div>
        <div class="col-4">
            Подробнее
        </div>
    </div>

    <div class="btn-group slider-container" role="group" aria-label="Basic radio toggle button group" style="display: flex; gap: 1rem;">
        <input type="radio" class="btn-check" name="btnradio" id="btnradio1" autocomplete="off" checked>
        <label class="btn btn-outline-primary" for="btnradio1" id="label1"><img src="../assets/ic_hotel_white.png" alt=""> Отель</label>

        <input type="radio" class="btn-check" name="btnradio" id="btnradio2" autocomplete="off">
        <label class="btn btn-outline-primary" for="btnradio2" id="label2"><img src="../assets/ic_restaurant_white.png" alt=""> Ресторан</label>

        <input type="radio" class="btn-check" name="btnradio" id="btnradio3" autocomplete="off">
        <label class="btn btn-outline-primary" for="btnradio3" id="label3"><img src="../assets/ic_avia_white.png" alt=""> Авиасервис</label>

        <input type="radio" class="btn-check" name="btnradio" id="btnradio4" autocomplete="off">
        <label class="btn btn-outline-primary" for="btnradio4" id="label4"><img src="../assets/ic_bus_white.png" alt=""> Автобусы</label>
    </div>

    <div class="row justify-content-between" style="margin: 2rem;">
        <div class="col-4" style="font-size: 1rem; font-weight: bold;">
            Предстоящие мероприятия
        </div>
        <div class="col-4">
            Подробнее
        </div>
    </div>

    <div class="container text-center">
        <div class="align-items-center slider-container" style="margin: 2rem 0;">
            <div class="col event_img">
                <img src="../assets/img_bagjan.png" class="rounded float-start" alt="...">
            </div>
            <div class="col event_img">
                <img src="../assets/img_ulpan.png" class="rounded float-start" alt="...">
            </div>
            <div class="col event_img">
                <img src="../assets/img_muzart.png" class="rounded float-start" alt="...">
            </div>
        </div>
    </div>
</template>

<script>
    const radioButtons = document.querySelectorAll('.btn-check');
    const labels = document.querySelectorAll('.btn.btn-outline-primary');
    const images = document.querySelectorAll('.btn.btn-outline-primary img');

    radioButtons.forEach((radioButton, index) => {
        radioButton.addEventListener('change', () => {
            if (radioButton.checked) {
                labels.forEach(label => label.querySelector('img').src = label.querySelector('img').src.replace('_orange.png', '_white.png'));
                images[index].src = images[index].src.replace('_white.png', '_orange.png');
            }
        });
    });

    // const handleNav = {
    //     //window.location.replace("Karahan.vue")
    // }

</script>

<style>
    .btn-outline-primary.active {
        background-color: orange;
    }

    .btn-outline-primary img.active {
        filter: grayscale(100%);
    }
    .col-9{
        text-align: start;
        font-size: 1.5rem;
        font-weight: 600;
    }
    .slider-container {
        margin-top: 2rem;
        background-color: white;
        display: flex;
        width: 100%;
        gap: 1rem;
        margin: 0 1rem;
        overflow-x: auto; /* Enable horizontal scrolling */
        white-space: nowrap; /* Prevent line breaks */
    }

    .slide {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      width: 50%; /* Adjust as needed */
      vertical-align: top;
    }

    .slide img {
      width: 30%;
      height: auto;
    }
    
    .event_img img{
        width: 10rem;
    }
</style>