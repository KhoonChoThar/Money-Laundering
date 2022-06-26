<template>
  <Breadcrumbs></Breadcrumbs>
  <div class="col-8 col-s-12 blogs-container">
    <div v-for="post in posts" :key="post.id">
      <SingleBlogCard :title="post.webTitle"></SingleBlogCard>
    </div>
  </div>
  <div class="col-4 col-s-12 info-container">
    <BlogSearch></BlogSearch>
    <CategoriesCard></CategoriesCard>
    <BlogRecentPosts></BlogRecentPosts>
    <BlogTagsCard></BlogTagsCard>
    <BlogSubscribeCard></BlogSubscribeCard>
  </div>
</template>

<script>
import SingleBlog from "../components/SingleBlog";
import BlogSubscribeCard from "../components/BlogSubscribeCard";
import BlogTagsCard from "../components/BlogTagsCard";
import BlogRecentPosts from "../components/BlogRecentPosts";
import CategoriesCard from "../components/CategoriesCard";
import BlogSearch from "../components/BlogSearch";
import SingleBlogCard from "../components/SingleBlogCard";
import Breadcrumbs from "../components/Breadcrumbs";

import axios from "axios";
const api = "6a2e4bef-aae5-46bc-9d72-caaf901f08da";
export default {
  components: {
    SingleBlog,
    BlogSubscribeCard,
    BlogTagsCard,
    BlogRecentPosts,
    CategoriesCard,
    BlogSearch,
    SingleBlogCard,
    Breadcrumbs,
  },
  data() {
    return {
      posts: [],
      postContent: null,
    };
  },
  methods: {
    handleResponse(res) {
      this.posts = res.results;
      console.log(this.formatPost(this.posts[0]));
    },
    async formatPost(postData) {
      var postDataFromApi = await this.getSinglePost(postData.apiUrl);
      var post = {};
      post.id = postData.id;
      post.title = postData.webTitle;
      post.body = postDataFromApi.body;
      console.log(postDataFromApi);
      return post;
    },
    async getSinglePost(apiUrl) {
      await axios({
        method: "get",
        url: `${apiUrl}?api-key=${api}&show-fields=body`,
      }).then(
        (res) => (this.postContent = res.data.response.content.fields),
        (err) => (this.postContent = "Content Invalid")
      );
      return this.postContent;
    },
    async getPosts() {
      await axios({
        method: "get",
        url: `https://content.guardianapis.com/search?api-key=${api}&page-size=6`,
      }).then(
        (res) => this.handleResponse(res.data.response),
        (err) => console.log(err)
      );
    },
  },
  mounted() {
    this.getPosts();
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}
[class*="col-"] {
  float: left;
  padding: 15px;
}
.blogs-container {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
.info-container {
  display: flex;
  justify-content: start;
  flex-direction: column;
}
/* For mobile phones: */
[class*="col-"] {
  width: 100%;
}

@media only screen and (min-width: 600px) {
  /* For tablets: */
  .col-s-1 {
    width: 8.33%;
  }
  .col-s-2 {
    width: 16.66%;
  }
  .col-s-3 {
    width: 25%;
  }
  .col-s-4 {
    width: 33.33%;
  }
  .col-s-5 {
    width: 41.66%;
  }
  .col-s-6 {
    width: 50%;
  }
  .col-s-7 {
    width: 58.33%;
  }
  .col-s-8 {
    width: 66.66%;
  }
  .col-s-9 {
    width: 75%;
  }
  .col-s-10 {
    width: 83.33%;
  }
  .col-s-11 {
    width: 91.66%;
  }
  .col-s-12 {
    width: 100%;
  }
}
@media only screen and (min-width: 768px) {
  /* For desktop: */
  .col-1 {
    width: 8.33%;
  }
  .col-2 {
    width: 16.66%;
  }
  .col-3 {
    width: 25%;
  }
  .col-4 {
    width: 33.33%;
  }
  .col-5 {
    width: 41.66%;
  }
  .col-6 {
    width: 50%;
  }
  .col-7 {
    width: 58.33%;
  }
  .col-8 {
    width: 66.66%;
  }
  .col-9 {
    width: 75%;
  }
  .col-10 {
    width: 83.33%;
  }
  .col-11 {
    width: 91.66%;
  }
  .col-12 {
    width: 100%;
  }
}
</style>
