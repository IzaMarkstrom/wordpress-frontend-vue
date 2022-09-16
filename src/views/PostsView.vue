<template>
    <div>
      <h1>Blog posts</h1>
      <h2>Different blog posts</h2>
      <div v-if="posts">
        <div v-for="post in posts" :key="post.ID" class="detailsLink">
          <router-link :to="{name: 'postDetails', params: {id: post.ID}}">
            <h2>{{post.title}}</h2>
          </router-link>
          <p>{{post.date.split("T")[0]}}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'posts',
    data() {
      return {
        posts: null
      }
    },
    mounted(){
      fetch(`${process.env.VUE_APP_BACKEND_URL}`)
      .then(res => res.json())
      .then(data => this.posts = data.posts)
      .catch(err => console.log(err.message))
    }
  }
  </script>

  <style>
    .detailsLink h2 {
        background: #f4f4f4;
        padding: 10px;
        border-radius: 10px;
        margin: 10px auto;
        max-width: 400px;
        cursor: pointer;
        color: #444;
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
        transition: 0.3s;
    }
    .detailsLink h2:hover {
        background: #ddd;
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
    }
    .detailsLink a {
        text-decoration: none;
        max-width: 400px;
    }
  </style>