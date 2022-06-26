<template>
  <div>
    <div class="heading">
      <h2>TITLE HEADING</h2>
    </div>
    <div class="info">
      <div class="user-info">
      <img
        src="https://yt3.ggpht.com/a/AGF-l7-0J1G0Ue0mcZMw-99kMeVuBmRxiPjyvIYONg=s900-c-k-c0xffffffff-no-rj-mo"
      />
      <span>July Dec</span>
    </div>
    <div class="detail-info">
      <span>8/27/22</span>
      <span>25k views</span>
      <span>4 mins read</span>
    </div>
    </div>
    <div class="blog-image">
<img
      src="https://c0.wallpaperflare.com/preview/483/210/436/car-green-4x4-jeep.jpg"
    />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.info{
  display: flex;
  align-items: center;
  justify-content: space-between;
  color: #4F5A5E;
  font-size: 14px;
  margin-bottom: 10px;
}
.user-info {
  display: flex;
  align-items: center;
  font-weight: 600;
}
.user-info img {
  border-radius: 50%;
  width: 25px;
  height: 25px;
  margin-right: 5px;
}
.detail-info{
  display: flex;
  justify-content: space-evenly;
  
}
.detail-info span{
  display: inline-block;
  margin-right: 10px;
}
.blog-image img{
  max-width: 700px;
  height: auto;
  border-radius: 8px;
}
</style>
