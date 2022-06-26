<template>
  <div class="container">
    <div class="searchInputContainer" v-if="toggleInput">
      <input type="search" class="searchInput" />
    </div>
    <div class="searchIcon" @click="Toggle">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
        stroke="#000000"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      >
        <circle cx="11" cy="11" r="8"></circle>
        <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
      </svg>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      toggleInput: false,
    };
  },
  methods: {
    Toggle() {
      this.toggleInput = !this.toggleInput;
    },
  },
};
</script>

<style>
.searchInputContainer {
  display: inline-block;
}
.searchInput {
  border: 1px solid grey;
  border-radius: 5px;
  width: 200px;
  box-sizing: border-box;
  outline: none;
  padding: 5px 10px;
  color: #fff;
}
.searchIcon {
  display: inline-block;
  cursor: pointer;
  padding: 5px;
  vertical-align: middle;
}
</style>
