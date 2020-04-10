<template>
  <div id="app">
    <nav id="nav">
      <ul class="navbar">
        <li>
          <router-link to="/">Home</router-link>
        </li>
        <li>
          <router-link to="/about">About</router-link>
        </li>
      </ul>
    </nav>
    <router-view />
  </div>
</template>

<style lang="scss">
@import url("./grid.css");
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@400;700&display=swap");

body {
  font-family: Raleway, Helvetica, Arial, sans-serif;
  background-color: whitesmoke;
  color: #241c15;
}

address {
  font-style: normal;
}

a {
  color: dodgerblue;
  text-decoration: none;
}

a:hover,
a:active {
  text-decoration: underline;
  color: lighten($color: dodgerblue, $amount: 12);
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // color: #2c3e50;
}

#nav {
  // padding: 30px;
  background-color: dodgerblue;

  a {
    font-weight: bold;
    // color: #2c3e50;
    color: white;

    &.router-link-exact-active {
      background-color: lighten($color: dodgerblue, $amount: 12);
      // color: #42b983;
    }
  }
}

.navbar {
  list-style: none;
  margin: 0;
  padding: 0;

  li {
    display: inline;

    a {
      display: inline-block;
      padding: 15px;

      &:hover {
        text-decoration: none;
        background-color: lighten($color: dodgerblue, $amount: 12);
      }
    }
  }
}
</style>
