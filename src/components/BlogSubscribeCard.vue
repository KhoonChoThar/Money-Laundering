<template>
  <div class="card">
    <div class="card-header">Subscribe to KBZ Money Alerts</div>
    <div class="card-body">
      <input type="email" class="email-subscribe" placeholder="Email Address" />
      <button class="subscribe">Subscribe Now</button>
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
  background-color: #0a59be;
}
.card-header {
  line-height: 40px;
  font-weight: 500;
  font-size: 32px;
  text-align: center;
  padding: 40px 20px 10px 20px;
  color: white;
}
.card-body {
  margin: 20px;
  padding: 10px;
  display: flex;
  flex-direction: column;
}
.email-subscribe {
  padding: 12px 35px;
  background-color: white;
  border-radius: 8px;
  color: #4f5a5e;
  border: none;
  text-align: center;
}
.email-subscribe:focus {
  outline: none;
}
.subscribe {
  font-size: 16px;
  background: #20c2ff;
  border-radius: 8px;
  text-align: center;
  margin: 20px auto;
  padding: 10px;
  border: none;
  color: white;
}
</style>
