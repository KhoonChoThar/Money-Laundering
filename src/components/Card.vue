<template>
  <div class="card">
    <img src="{{filename}}" />
    <div class="content">
      <header>{{ header }}</header>
      <p>
        {{ content }}
      </p>
      <div class="buttons">
        <span>Get Started</span>
        <svg
          width="24"
          height="24"
          xmlns="http://www.w3.org/2000/svg"
          fill-rule="evenodd"
          clip-rule="evenodd"
        >
          <path
            d="M21.883 12l-7.527 6.235.644.765 9-7.521-9-7.479-.645.764 7.529 6.236h-21.884v1h21.883z"
          />
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["filename", "header", "content"],
  data() {
    return {};
  },
};
</script>

<style scoped>
.card {
  position: absolute;
  max-width: 365px;
  background: #fff;
  padding: 25px 25px 30px 25px;
  border-radius: 15px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.3s;
}
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}
.buttons {
  display: inline-flex;
  margin-bottom: 0;
}
</style>
