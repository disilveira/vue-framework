<template>
  <div id="app">
    <Header class="header" title="Framework Vue" />
    <NavBar :items="menus" />
  </div>
</template>

<script>
import Header from "./components/Header";
import NavBar from "./components/NavBar";

export default {
  name: "App",
  components: {
    NavBar,
    Header,
  },
  data() {
    return {
      menus: [
        { text: "Home", link: "home.html" },
        { text: "Sobre", link: "sobre.html" },
        { text: "Contato", link: "contato.html" },
      ],
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@100;500&display=swap");

* {
  margin: 0;
  padding: 0;
}

.header {
  font-family: "Roboto", sans-serif;
  padding: 20px;
  text-align: left;
  background: #1abc9c;
  color: white;
  font-size: 30px;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  border: 1px solid #e7e7e7;
  background-color: #f3f3f3;
}

li {
  float: left;
}

li a {
  display: block;
  color: #666;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover:not(.active) {
  background-color: #ddd;
}

li a.active {
  color: white;
  background-color: #4caf50;
}
</style>
