<template>
  <div class="search-bar">
    <input type="text" placeholder="Найти..." />
  </div>
</template>


<style scoped>
.search-bar {
  text-align: center; /* Центрирование содержимого */
  flex: 2; /* Занимает больше пространства по сравнению с другими элементами */
}

.search-bar input {
  width: 100%;
  max-width: 400px; /* Ограничение по ширине */
  padding: 8px 15px;
  border-radius: 20px;
  border: 1px solid #ccc;
  font-size: 16px;
}
</style>