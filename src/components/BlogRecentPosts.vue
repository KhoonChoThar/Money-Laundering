<template>
  <div class="card">
    <div class="card-header">Recent Posts</div>
    <div class="card-body">
      <div class="card-info">
        <img
          src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
        />

        <div class="card-info-text">
          <h4>White Mountains</h4>
          <small>8 hours ago</small>
        </div>
      </div>
      <div class="card-info">
        <img
          src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
        />

        <div class="card-info-text">
          <h4>White Mountains</h4>
          <small>8 hours ago</small>
        </div>
      </div>
      <div class="card-info">
        <img
          src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
        />

        <div class="card-info-text">
          <h4>White Mountains</h4>
          <small>8 hours ago</small>
        </div>
      </div>
      <div class="card-info">
        <img
          src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
        />

        <div class="card-info-text">
          <h4>White Mountains</h4>
          <small>8 hours ago</small>
        </div>
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
  padding: 15px 20px;
  font-weight: 600;
  font-size: 18px;
  text-align: left;
}

.card-body {
  margin: 10px;
}
.card-info {
  padding: 10px;
  display: flex;
}
.card-info img {
  width: 60px;
  height: 60px;
  border-radius: 5px;
  object-position: center;
  object-fit: cover;
  margin-right: 10px;
}
.card-info-text {
  text-align: left;
}
.card-info-text h4 {
  margin: 0;
  padding: 5px 0;
}
</style>
