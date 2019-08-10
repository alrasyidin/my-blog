<template>
  <Layout>
    <br />
    <g-link to="/" class="link">&larr; Go Back</g-link>
    <div class="post-title">
      <h1>{{$page.post.title}}</h1>
      <h5>{{$page.post.description}}</h5>
      <p class="post-date">{{ $page.post.date}} | {{$page.post.timeToRead}} min read</p>
    </div>
    <div class="post-content">
      <p v-html="$page.post.content" />
    </div>
  </Layout>
</template>

<page-query>
query Post ($path: String!) {
   post: post (path: $path) {
    id
    title
    description
    content
    date (format: "D MMMM YYYY")
    timeToRead
  }
}
</page-query>

<style>
.post-title {
  text-align: center;
  font-size: 20px;
  line-height: 18px;
  padding: 2em 0;
  font-family: "Stylish";
}

.post-title h5 {
  font-size: 19px;
}

.post-date {
  font-size: 16px;
  font-weight: 400;
}

.post-content {
  font-size: 20px;
}
</style>