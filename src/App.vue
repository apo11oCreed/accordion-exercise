<template>
  <div id="app">
    <img src="./assets/logo.svg" class="logo" alt="Aetna logo">
    <div class="container">
      <!-- <h1>Import your component here</h1> -->
        <Accordion v-for="(accordion, index) in accordionData" :key="index + 0" :index="index + 1" :title="accordion.title" :content="accordion.content" :link="accordion.link" />
    </div>
  </div>
</template>

<script>
import Accordion from './components/Accordion';
export default {
  name: 'app',
  data() {
    return {
      accordionData: [
        {
          'title': 'Title 1',
          'content': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'link': 'http://www.google.com'
        },
        {
          'title': 'Title 2',
          'content': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'link': 'http://www.aetna.com'
        },
        {
          'title': 'Title 3',
          'content': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'link': 'http://www.yahoo.com'
        }
      ]
    }
  },
  components: {
    Accordion
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Open+Sans&display=swap');
#app {
  font-family: 'Open Sans', Helvetica, Arial, sans-serif;
  color: #414141;
  margin-top: 20px;
  h1 {
    color: #7D3F98;
  }
  .logo {
    width: 250px;
  }
}

.articleWrapper {
  position:relative;
}

.arrowBlueSmall{
  display: block;
  position: absolute;
  top: 13px;
  right: 0;
  width: 1em;
  height: 1em;
  margin-top: -0.5em;
  transform: scaleY(-1);
  background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%2024%2015%22%3E%3Ctitle%3Eicon-expand%3C%2Ftitle%3E%3Cpath%20d%3D%22M21%200l3%203.06L12%2015%200%203.06%203%200l9%209z%22%20fill%3D%22%238932af%22%20data-name%3D%22Layer%201%22%2F%3E%3C%2Fsvg%3E");
  background-repeat: no-repeat;
  background-position: center center;
  background-size: contain;
  content: "";
  -webkit-transform: scaleY(-1)
}

.arrowUp:after{
  display: block;
  position: absolute;
  top: 13px;
  right: 0;
  width: 1em;
  height: 1em;
  margin-top: -0.5em;
  transform: scaleY(-1);
  background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%2024%2015%22%3E%3Ctitle%3Eicon-expand%3C%2Ftitle%3E%3Cpath%20d%3D%22M21%200l3%203.06L12%2015%200%203.06%203%200l9%209z%22%20fill%3D%22%238932af%22%20data-name%3D%22Layer%201%22%2F%3E%3C%2Fsvg%3E");
  background-repeat: no-repeat;
  background-position: center center;
  background-size: contain;
  content: "";
  -webkit-transform: scaleY(-1)
}

.arrowDown:after{
  display: block;
  position: absolute;
  top: 13px;
  right: 0;
  width: 1em;
  height: 1em;
  margin-top: -0.5em;
  transform: scaleY(-1), rotate(180deg);
  background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%2024%2015%22%3E%3Ctitle%3Eicon-expand%3C%2Ftitle%3E%3Cpath%20d%3D%22M21%200l3%203.06L12%2015%200%203.06%203%200l9%209z%22%20fill%3D%22%238932af%22%20data-name%3D%22Layer%201%22%2F%3E%3C%2Fsvg%3E");
  background-repeat: no-repeat;
  background-position: center center;
  background-size: contain;
  content: "";
  -webkit-transform: scaleY(-1)
}
.collapsed {
  height:34px;
  overflow:hidden;
}
</style>
