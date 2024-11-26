<template>
  <div class="main-menu">
    <div id="button-container">
      <div id="upper-container">
        <button class = "menu-button">Вход</button>
      </div>
      <div id="middle-container">
        <button class = "menu-button">Таблица лидеров</button>
      </div>
      <div id="bottom-container">
        <div id="bottom-left">
          <button class = "menu-button" @click="openSettings">Настройки</button>
        </div>
        <div id="bottom-middle">
          <button class = "menu-button" @click="startGame">Начать игру</button>
        </div>
        <div id="bottom-right">
          <button class = "menu-button" @click="exitGame">Выход</button>
        </div>
      </div>
    </div>
  </div>
</template>
<button>Вход</button>
<script>
export default {
  name: 'MainMenu',
  methods: {
    startGame() {
      // Логика для начала игры
      this.$emit('start-game');
    },
    openSettings() {
      // Логика для открытия настроек
      this.$emit('open-settings');
    },
    exitGame() {
      // Логика для выхода из игры
      this.$emit('exit-game');
    }
  }
}
</script>

<style scoped>
.main-menu {
  background-image: url("@/assets/background.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
.main-menu {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
}
button {
  margin: 10px;
  padding: 10px 20px;
  font-size: 16px;
}
#button-container {
  display: flex;
  flex-direction: column;
  bottom: 10px;
}
#bottom-container {
  display: flex;
  flex-direction: row;
}
#middle-container {
  display: flex;
  justify-content: start;
}
#upper-container {
  display: flex;
  justify-content: start;
}
.menu-button {
  background-color: #7B6E62;
  font-size: 32;
  border: #000000;
  border-radius: 15px;
  border-width: 100px;
  width: 150px;
  height: 50;
  stroke-width: 5px;
  border-color: #000000;
  box-shadow: 3px 3px 2px 1px #000000;
}

</style>