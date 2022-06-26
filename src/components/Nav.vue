<template>
  <NavExtraInfo></NavExtraInfo>
  <div id="nav" class="grid-container">
    <div class="grid-item">
      <router-link :to="{ name: 'Home' }"
        ><img src="../assets/images/kbz.png" class="logo"
      /></router-link>
    </div>
    <div class="grid-item">
      <div class="navItems">
        <router-link :to="{ name: 'Home' }">Home</router-link>
        <router-link :to="{ name: 'Blog' }">Blog</router-link>
      </div>
    </div>
    <div class="grid-item">
      <Search></Search>
    </div>
  </div>
</template>

<script>
import NavExtraInfo from "./NavExtraInfo";
import Search from "./Search";
export default {
  components: {
    NavExtraInfo,
    Search,
  },
};
</script>

<style>
#nav {
  background-color: #ffffff;
  box-sizing: border-box;
  box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.05);
  border-radius: 2px;
}
#nav a {
  font-weight: bold;
  color: #2c3e50;
  padding: 10px;
  vertical-align: middle;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: #015EB9;
}
.navItems {
  display: inline-flex;
  vertical-align: middle;
}
.grid-container {
  display: grid;
  justify-content: space-between;
  column-gap: 10px;
  grid-template-columns: auto auto 400px;
  padding: 5px 100px;
}
.grid-item {
  text-align: center;
}
.logo {
  width: 100px;
}
</style>
