<template>
  <div class="card">
    <div class="card-header">Categories</div>
    <div class="card-body">
      <span class="tag">Technology</span>
      <span class="tag">Information</span>
      <span class="tag">Uno</span>
      <span class="tag">Information</span>
      <span class="tag">Technology</span>
      <span class="tag">Information</span>
      <span class="tag">Uno</span>
      <span class="tag">Technology</span>
      <span class="tag">Information</span>
    </div>
  </div>
</template>

<script>
import axios from "axios";
const api = "6a2e4bef-aae5-46bc-9d72-caaf901f08da";
// const url = `http://content.guardianapis.com/tags?api-key=${api}`;
export default {
  data() {
    return {
      tags: [],
    };
  },
  // methods: {
  //   handleResponse(res) {
  //     this.tags = res;
  //     console.log(this.tags);
  //   },
  //   async getTags() {
  //     // await axios({
  //     //   method: "get",
  //     //   url: `http://content.guardianapis.com/tags?api-key=${api}`,
  //     // })

  //       // .then((res) => this.handleResponse(res))
  //       // .catch((error) => {
  //       //   console.log("Error:", error);
  //       // });
  //   },
  //},
  mounted() {
    const res =axios.get(`http://content.guardianapis.com/tags?api-key=${api}`)
    console.log(res.data);
  },
};
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
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  padding: 10px;
}
.tag {
  align-self: flex-start;
  background: #f1f6f8;
  border: 1px solid #e6edf3;
  border-radius: 5px;
  padding: 8px;
  margin: 5px 0 5px 5px;
  font-size: 14px;
  display: inline-block;
}

/* .tag + .tag {
  margin-left: 0.5em;
} */
</style>
