<template>
  <div>
    <picture>
      <source srcset="/images/logo-main.svg"media="(min-width: 1024px)"/>
      <source srcset="/images/logo-pad.svg" media="(min-width: 768px)" />
      <img src="/images/logo-mobile.svg" />
    </picture>
  </div>
</template>




<style scoped>
.logo img {
  max-width: 100%; /* Логотип будет растягиваться на доступную ширину */
  height: auto; /* Соотношение сторон сохранено */
  width: 150px; /* Размер логотипа, можно корректировать */
}
</style>