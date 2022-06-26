<template>
  <div class="breadcrumb-container">
    <h2>Blog</h2>
    <ul class="breadcrumb">
      <li class="breadcrumb-item">
        <router-link :to="{ name: 'Home' }">Home</router-link>
      </li>
      <li class="breadcrumb-item">
        <router-link :to="{ name: 'Blog' }">Blog</router-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style>
.breadcrumb-container {
  padding: 30px 0px;
  background-image: url("../assets/images/Breadcrumb_bg.png");
  color: white;
  text-align: center;
}
.breadcrumb {
  list-style: none;
  padding: 0;
}
.breadcrumb-item {
  display: inline;
  font-size: 18px;
}
.breadcrumb-item a {
  font-weight: bold;
  color: #8fa5ae;
  padding: 10px;
  vertical-align: middle;
  text-decoration: none;
}

.breadcrumb-item a.router-link-exact-active {
  color: white;
}
.breadcrumb li + li:before {
  padding: 8px;
  color: #8fa5ae;
  content: ">";
}
</style>
