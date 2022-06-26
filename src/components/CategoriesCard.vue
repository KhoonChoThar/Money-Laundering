<template>
  <div class="card">
    <div class="card-header">Categories</div>
    <div class="card-body">
      <div class="card-info">
        <span>Alerts</span>
        <span>35</span>
      </div>
      <div class="card-info">
        <span>Alerts</span>
        <span>35</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.card {
  margin: 10px 0;
  width: 300px;
  border-radius: 8px;
  border: 1px solid #e6edf3;
}
.card-header {
  background: #f9fbfc;
  font-weight: 600;
  font-size: 18px;
  text-align: left;
  padding: 15px 20px;
}
.card-body {
  margin: 10px;
}
.card-info {
  padding: 10px;
  display: flex;
  justify-content: space-between;
}
</style>
