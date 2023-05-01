<template>
  <section class="section registration">
    <div class="registration__container">
      <div class="registration__content _container">
        <h2 class="registration__title title">Что нужно для регистрации?</h2>
        <div class="registration__list">
          <div class="registration__item">
            <div class="registration__item-img">
              <img src="@/assets/img/step_1.png" alt="" />
            </div>
            <div class="registration__item-text">
              <span>Номер телефона</span>
              Вам придет СМС код для подтверждения номера
            </div>
          </div>
          <div class="registration__item">
            <div class="registration__item-img">
              <img src="@/assets/img/step_2.png" alt="" />
            </div>
            <div class="registration__item-text">
              <span>Паспорт/ID-карта</span>
              Фотография паспорта (Лицевая сторона и сторона прописки)
            </div>
          </div>
          <div class="registration__item">
            <div class="registration__item-img">
              <img src="@/assets/img/step_3.png" alt="" />
            </div>
            <div class="registration__item-text">
              <span>Пластиковая карта</span>
              16ти значная цифра карты и дата срока
            </div>
          </div>
          <div class="registration__item">
            <div class="registration__item-img">
              <img src="@/assets/img/step_4.png" alt="" />
            </div>
            <div class="registration__item-text">
              <span>Камера телефона</span>
              Селфий с паспортом на фоне лица
            </div>
          </div>
        </div>
        <h2 class="registration__title title">Этап регистрации</h2>
        <p class="registration__subtitle">Посмотрите краткий видеоролик этапа регистрации и все требования для нее</p>
        <div class="registration__video">
          <iframe
            src="https://www.youtube.com/embed/nvjpYxyMC7k"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            allowfullscreen
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Registration'
}
</script>

<style scoped lang="scss">
@import "@/assets/styles/mainPage/registration";
</style>
