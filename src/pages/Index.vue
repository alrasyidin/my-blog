<template>
  <Layout>
    <header class="header">
      <g-image src="~/assets/img/photo.jpg" alt="My Photo" width="100" class="photo" blur="50"></g-image>
      <ul class="navi">
        <li class="navi__li">
          <g-link to="/" class="navi__link link">Home</g-link>
        </li>
        <li class="navi__li">
          <g-link to="/about/" class="navi__link link">About</g-link>
        </li>
      </ul>
      <h1 v-html="$page.metaData.siteName" />
      <p v-html="$page.metaData.siteDescription" />
    </header>
    <section class="posts">
      <PostList v-for="edge in $page.allPost.edges" :key="edge.node.id" :post="edge.node" />
    </section>
  </Layout>
</template>

<script>
import PostList from "@/components/PostList";
export default {
  components: {
    PostList
  },
  metaInfo: {
    title: "A simple blog"
  }
};
</script>

<page-query>
query {
  metaData {
    siteName
    siteDescription
  }
  allPost {
    totalCount
    edges {
      node {
        id
        title
        timeToRead
        description
        date (format: "D MMMM YYYY")
        path
      }
    }

  }
}
</page-query>

<style>
.header {
  font-family: "Stylish";
  font-size: 20px !important;
  text-align: center;
  line-height: 20px;
  padding: 0.7em;
}

.header p {
  font-weight: 200;
}
.photo {
  border-radius: 50%;
  filter: blur(5px);
}
</style>