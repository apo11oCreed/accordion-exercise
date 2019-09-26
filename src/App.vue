<template>
  <div id="app">
    <img src="./assets/logo.svg" class="logo" alt="Aetna logo">
    <div class="container">
      <!-- <h1>Import your component here</h1> -->
        <Accordion v-for="(accordion, i) in accordionData" 
        :key="i" 
        :index="i" 
        :title="accordion.title" 
        :content="accordion.content" 
        :link="accordion.link" 
        :open="accordion.open"
        @toggleAccordion="toggleAccordion"/>
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
  },
  methods: {
    toggleAccordion: function (index){
      this.accordionData = this.accordionData.map((accordion, i)=>{
        if(index === i){
          accordion.open = !accordion.open;
          } else {
            accordion.open = false;
          }

          return accordion;
          });
          }
  }
  }
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Open+Sans:400,700&display=swap');
body{
  background-color:#f5f5f5;
}
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
  border-top:4px solid #dddddd;
  border-bottom:1px solid #dddddd;
  border-left:1px solid #dddddd;
  border-right:1px solid #dddddd;
  padding:3rem;
  background-color:#ffffff;
  margin:2rem;
  max-height:30px;
  overflow-y:hidden;
  transition: all 0.4s ease-out;
}

.articleWrapper h2 {
  position: relative;
  clear:both;
  font-weight:700;
  margin-block-end:48px;
  margin-block-start: 0;
}

.articleWrapper h2:after{
  display: block;
  position: absolute;
  top: 13px;
  right: 0;
  width: 1em;
  height: 1.25em;
  margin-top: -0.5em;
  transform: scaleY(-1) rotate(180deg);
  background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%2024%2015%22%3E%3Ctitle%3Eicon-expand%3C%2Ftitle%3E%3Cpath%20d%3D%22M21%200l3%203.06L12%2015%200%203.06%203%200l9%209z%22%20fill%3D%22%23d31472%22%20data-name%3D%22Layer%201%22%2F%3E%3C%2Fsvg%3E");
  background-repeat: no-repeat;
  background-position: center center;
  background-size: contain;
  content: "";
  -webkit-transform: scaleY(-1) rotate(180deg);
  transition: all 0.4s ease-out;
}

.articleWrapper img {
  width:32px;
  height:32px;
  float:left;
}

.articleWrapper p {
  margin-block-start: 0;
}

.articleWrapper br {
  clear:both;
}

.articleWrapper a.link {
  color:#d91a6f;
  position: relative;
}

.articleWrapper a.link:after {
  display: block;
  position: absolute;
  top: 13px;
  right: -2rem;
  width: 1em;
  height: 1em;
  margin-top: -0.5em;
  background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%2024%2015%22%3E%3Ctitle%3Eicon-expand%3C%2Ftitle%3E%3Cpath%20d%3D%22M21%200l3%203.06L12%2015%200%203.06%203%200l9%209z%22%20fill%3D%22%23d31472%22%20data-name%3D%22Layer%201%22%2F%3E%3C%2Fsvg%3E");
  background-repeat: no-repeat;
  background-position: center center;
  background-size: contain;
  content: "";
  transform: scaleY(-1) rotate(275deg);
  -webkit-transform: scaleY(-1) rotate(275deg);
}

.articleWrapper .content {
  display:flex;
  flex-direction: row;
}

@media screen and (max-width:767px){
  .articleWrapper .content {
  display:flex;
  flex-direction: column;
  }
}

.articleWrapper .content div:nth-child(1) {
  min-width:80px;
}

@media screen and (max-width:767px){
  .articleWrapper .content div:nth-child(1) {
    min-height:80px;
    }
}

.articleWrapper.open {
  max-height:1000px;
}

.articleWrapper.open h2:after {
  transform: scaleY(-1) rotate(360deg);
  -webkit-transform: scaleY(-1) rotate(360deg);
}
</style>