<template>
  <h1>Post Detail page</h1>

  <div v-if="post" class="post">
    <!-- <img src="" alt=""> -->
    <div class="container">
      <h2>{{post.title}}</h2>
      <p>Post ID is: {{id}}</p>
      <p v-html="post.content"></p>
    </div>
  </div>

</template>

<script>
    export default {
      props: ['id'],
      data() {
        return {
          post: null
        }
      },
      mounted(){
        fetch("https://public-api.wordpress.com/rest/v1.1/sites/izamarkstrom.wordpress.com/posts/" + this.id)
        .then(res => res.json())
        .then(data => this.post = data)
        .catch(err => console.log(err.message))
      }
    }
</script>
    
    
<style>
  .post {
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.1);
    max-width: 800px;
    margin-left: 18%;
  }
  .container {
    padding: 2px 16px;
  }
</style>