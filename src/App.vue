<template>
  <div id="app">
    <img src="./assets/logo.svg" class="logo" alt="Aetna logo">
    <div class="container">
      <h1>Import your component here</h1>
      <div v-for="(accordion, thing, index) in accordionData" :key="accordion.index">
        <h2>{{ accordion.title }} - {{ accordion.index }}</h2>
        <p>{{ accordion.content }}</p>
        <a :href="accordion.link">{{ accordion.link }}</a>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'app',
  data() {
    return {
      accordionData: [
        {
          title: 'Title 1',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          link: 'http://www.google.com'
        },
        {
          title: 'Title 2',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          link: 'http://www.aetna.com'
        },
        {
          title: 'Title 3',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          link: 'http://www.yahoo.com'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  color: #414141;
  margin-top: 20px;
  h1 {
    color: #7D3F98;
  }
  .logo {
    width: 250px;
  }
}
</style>
