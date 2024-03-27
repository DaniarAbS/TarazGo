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
            <div class="col">
                <img src="../assets/karahan.png" class="rounded float-start" alt="...">
            </div>
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

    <div class="btn-group" role="group" aria-label="Basic radio toggle button group" style="display: flex; gap: 10rem;">
        <input type="radio" class="btn-check" name="btnradio" id="btnradio1" autocomplete="off" checked>
        <label class="btn btn-outline-primary" for="btnradio1"><img src="" alt=""> Отель</label>

        <input type="radio" class="btn-check" name="btnradio" id="btnradio2" autocomplete="off">
        <label class="btn btn-outline-primary" for="btnradio2">Ресторан</label>

        <input type="radio" class="btn-check" name="btnradio" id="btnradio3" autocomplete="off">
        <label class="btn btn-outline-primary" for="btnradio3">Авиасервис</label>

        <input type="radio" class="btn-check" name="btnradio" id="btnradio4" autocomplete="off">
        <label class="btn btn-outline-primary" for="btnradio4">Автобусы</label>
    </div>
    
</template>

<style>
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
</style>