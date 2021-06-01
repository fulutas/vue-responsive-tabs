<template>
  <div id="app">

    <TabNav :tabs="['Home', 'Settings', 'Profile']" :selected="selected" @selected="setSelected">

      <Tab  :isSelected="selected === 'Home'">
        <p>Some test text</p>
      </Tab>

      <Tab  :isSelected="selected === 'Settings'">
         <p>Some test text setting</p>
      </Tab>

      <Tab  :isSelected="selected === 'Profile'">
         <ul>
           <li>List test 1</li>
           <li>List test 2</li>
           <li>List test 3</li>
         </ul>
      </Tab>
      

    </TabNav>

  </div>
</template>

<script>

import TabNav from "./components/TabNav";
import Tab from "./components/Tab";

export default {
  name: "App",

  components: {
    TabNav,
    Tab,

  },
  data() {
    return {
      selected: "Home",
    };
  },

  methods: {
    setSelected(tab) {
      this.selected = tab;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  flex-direction: row;
  justify-content: center;
}
</style>
