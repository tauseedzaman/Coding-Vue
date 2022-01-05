<template>
  <h1>Testing Child Components</h1>
  <!-- <Heading text="This is the props for this Component" /> -->
  <div class="p-5 bg-success shadow" :style="{ fontSize: postFontSize + 'em' }">
    <BlogPost
      v-for="post in posts"
      :key="post.id"
      :title="post.title"
      :text="post.text"
      @enlarge-text="postFontSize += 0.1"
      @ensmall-text="postFontSize -= 0.1"
    />
  </div>
</template>

<script>
// import Heading from './Child/Heading.vue';
import BlogPost from "./Child/BlogPost.vue";
export default {
  components: {
    // Heading
    BlogPost,
  },
  data() {
    return {
      postFontSize: 2,
      posts: [
        {
          id: 1,
          title: "My journey with Vue",
          text: "This is the content of post hahahah. yeah you got at",
        },
        {
          id: 2,
          title: "Blogging with Vue",
          text: "This is the content of post hahahah. yeah you got at",
        },
        {
          id: 3,
          title: "Why Vue is so fun",
          text: "This is the content of post hahahah. yeah you got at",
        },
      ],
    };
  },
};
</script>

<style>
</style>