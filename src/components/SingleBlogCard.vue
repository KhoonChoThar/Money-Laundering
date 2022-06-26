<template>
  <div class="card">
    <div class="card-header">
      <img :src="blog - image" />
    </div>
    <div class="card-body">
      <h4>{{ title }}</h4>
      <div class="user">
        <div class="user-info">
          <img
            src="https://yt3.ggpht.com/a/AGF-l7-0J1G0Ue0mcZMw-99kMeVuBmRxiPjyvIYONg=s900-c-k-c0xffffffff-no-rj-mo"
          />
          <span>July Dec</span>
        </div>
        <small>2h ago</small>
      </div>
      <p>
        {{ content }}
      </p>
      <div class="read-more">
        <span><a href="#" class="link-text">This is a link</a></span>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          aria-hidden="true"
          role="img"
          width="24px"
          height="24px"
          preserveAspectRatio="xMidYMid meet"
          viewBox="0 0 24 24"
          class="link-icon"
        >
          <path
            fill="currentColor"
            d="m23.068 11.993l-4.25-4.236l-1.412 1.417l1.835 1.83L.932 11v2l18.305.002l-1.821 1.828l1.416 1.412l4.236-4.25Z"
          />
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["title", "content"],
};
</script>

<style scoped>
.card {
  margin: 10px;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 2px 20px rgba(0, 0, 0, 0.2);
  overflow: hidden;
  width: 300px;
  font-size: 13px;
}
.card-header img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}
.card-body {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 10px;
  min-height: 250px;
  text-align: left;
}

.card-body p {
  font-size: 13px;
}
.user {
  display: flex;
  justify-content: space-between;
  width: 100%;
  align-items: center;
  margin-bottom: 10px;
}

.user img {
  border-radius: 50%;
  width: 25px;
  height: 25px;
  margin-right: 10px;
}
.user-info {
  display: flex;
  align-items: center;
}
.user-info span {
  margin: 0;
}
.user-info small {
  color: #545d7a;
}
.read-more {
  display: flex;
  align-items: center;
}
.link-text {
  text-decoration: none;
  color: #082a36;
  margin-right: 5px;
  font-weight: 700;
}
.link-text:hover {
  color: #8fa5ae;
}
.link-icon:hover {
  color: #8fa5ae;
}
</style>
