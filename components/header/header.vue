<template>
  <header ref="header" class="header">
    <Logo />
    <nav class="header-center">
      <ul>
        <li><a href="/catalog">Каталог</a></li>
        <li><a href="/about">О нас</a></li>
        <li><a href="/contacts">Контакты</a></li>
      </ul>
      <SearchBar />
    </nav>
    <div class="auth-container">
      <AuthIcons />
      <button class="auth-button">Войти</button>
    </div>
    <Tools v-if="fetchedUser" :isDesktop="isDesktop" />
  </header>
</template>

<script>
import Logo from "@/components/header/logo";
import SearchBar from "@/components/header/search-bar";

export default {
  components: {
    Logo,
    SearchBar,
    Catalog: () => import("@/components/header/catalog"),
    Tools: () => import("@/components/header/tools"),
  },
  data() {
    return {
      isDesktop: true,
      fetchedUser: true,
      menuCatalog: [
        { name: "пункт1", semanticId: "1" },
        { name: "пункт2", semanticId: "2" },
        { name: "пункт3", semanticId: "3" },
        { name: "пункт4", semanticId: "4" },
      ],
    };
  },
};
</script>

<style scoped>
/* Основной стиль хедера */
.header {
  display: flex;
  justify-content: space-between; /* Разделить элементы по ширине */
  align-items: center; /* Выравнивание элементов по вертикали */
  padding: 10px 20px;
  background-color: #1c87e4;
  border-bottom: 1px solid #0ae2f6;
}

/* Центральный блок (поиск) */
.header-center {
  flex: 2; /* Больше пространства для поиска */
  display: flex;
  justify-content: center; /* Центрирование поиска */
  align-items: center;
}

.search-bar input {
  width: 100%;
  max-width: 400px; /* Ограничиваем максимальную ширину поля поиска */
  padding: 8px 15px;
  border-radius: 20px;
  border: 1px solid #09b5f4;
  background-color: #0ae2f6;
  font-size: 16px;
}

.auth-button {
  color: white;
  flex-direction: column;
  background-color: #0ae2f6;
  display: flex;
  transition: color 0.3s ease;
  border: none;
  cursor: pointer;
  padding: 10px;
  border-radius: 5px;
}

.auth-button:hover {
  color: rgb(0, 204, 255);
}
.auth-login {
  background-color: transparent;
  border: 1px solid #007bff;
  color: #007bff;
  padding: 8px 16px;
  border-radius: 4px;
  cursor: pointer;
  font-size: 16px;
}
</style>
