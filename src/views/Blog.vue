<template>
<Breadcrumbs></Breadcrumbs>
<div class="col-8 col-s-12 blogs-container">
<SingleBlogCard></SingleBlogCard>
<SingleBlogCard></SingleBlogCard>
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
import BlogSubscribeCard from '../components/BlogSubscribeCard'
import BlogTagsCard from '../components/BlogTagsCard'
import BlogRecentPosts from '../components/BlogRecentPosts'
import CategoriesCard from '../components/CategoriesCard'
import BlogSearch from '../components/BlogSearch'
import SingleBlogCard from '../components/SingleBlogCard'
import Breadcrumbs from '../components/Breadcrumbs'
export default {
  components: {
    BlogSubscribeCard,
    BlogTagsCard,
    BlogRecentPosts,
    CategoriesCard,
    BlogSearch,
    SingleBlogCard, Breadcrumbs },};
</script>

<style>
* {
  box-sizing: border-box;
}
[class*="col-"] {
  float: left;
  padding: 15px;
}
.blogs-container{
  display: flex;
  justify-content: center;
}
.info-container{
   display: flex;
  justify-content:start;
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
