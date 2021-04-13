<template>
  <div id="app">
    <div class="main">
      <Header class="header" title="Framework Vue" />
      <NavBar :items="menus" />
      <Article :articles="articles" />
    </div>
    <div class="sidenav">
      <Aside :asideMenus="menusAside" />
    </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import NavBar from "./components/NavBar";
import Article from "./components/Article";
import Aside from "./components/Aside";

export default {
  name: "App",
  components: {
    Header,
    NavBar,
    Article,
    Aside,
  },
  data() {
    return {
      menus: [
        { text: "Home", link: "home.html" },
        { text: "Sobre", link: "sobre.html" },
        { text: "Contato", link: "contato.html" },
      ],
      articles: [
        {
          title: "Title 1",
          text:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tristique nisl vitae mi interdum, vel vehicula nisl rutrum. Etiam at nunc justo. Donec vel lectus suscipit urna pretium aliquet. Praesent in mattis nunc. Nunc blandit accumsan sapien, pellentesque euismod libero sollicitudin nec. Morbi bibendum eget enim id luctus",
        },
        {
          title: "Title 2",
          text:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tristique nisl vitae mi interdum, vel vehicula nisl rutrum. Etiam at nunc justo. Donec vel lectus suscipit urna pretium aliquet. Praesent in mattis nunc. Nunc blandit accumsan sapien, pellentesque euismod libero sollicitudin nec. Morbi bibendum eget enim id luctus",
        },
        {
          title: "Title 3",
          text:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tristique nisl vitae mi interdum, vel vehicula nisl rutrum. Etiam at nunc justo. Donec vel lectus suscipit urna pretium aliquet. Praesent in mattis nunc. Nunc blandit accumsan sapien, pellentesque euismod libero sollicitudin nec. Morbi bibendum eget enim id luctus",
        },
      ],
      menusAside: [
        { text: "Futebol", link: "futebol.html" },
        { text: "Novelas", link: "novelas.html" },
        { text: "Músicas", link: "musicas.html" },
        { text: "Tecnologia", link: "tecnologia.html" },
      ],
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@100;500&display=swap");

* {
  font-family: "Roboto", sans-serif;
  margin: 0;
  padding: 0;
}

.header {
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

article {
  padding: 15px;
  margin: 15px;
  border: 1px solid;
  -webkit-box-shadow: 1px 4px 3px 1px rgba(0, 0, 0, 0.59);
  box-shadow: 1px 4px 3px 1px rgba(0, 0, 0, 0.59);
}

/* The sidebar menu */
.sidenav {
  height: 100%; /* Full-height: remove this if you want "auto" height */
  width: 160px; /* Set the width of the sidebar */
  position: fixed; /* Fixed Sidebar (stay in place on scroll) */
  z-index: 1; /* Stay on top */
  top: 0; /* Stay at the top */
  left: 0;
  background-color: #111; /* Black */
  overflow-x: hidden; /* Disable horizontal scroll */
  padding-top: 20px;
}

/* The navigation menu links */
.sidenav a {
  text-align: center;
  padding: 5px;
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  display: block;
}

/* When you mouse over the navigation links, change their color */
.sidenav a:hover {
  color: #f1f1f1;
}

/* Style page content */
.main {
  margin-left: 160px; /* Same as the width of the sidebar */
}

/* On smaller screens, where height is less than 450px, change the style of the sidebar (less padding and a smaller font size) */
@media screen and (max-height: 450px) {
  .sidenav {
    padding-top: 15px;
  }
  .sidenav a {
    font-size: 18px;
  }
}
</style>
