<template>
  <div class="video_container">
    <iframe
      width="640"
      height="360"
      :src="propsdata.youtubeURL"
      frameborder="0"
      allow="autoplay; encrypted-media"
      allowfullscreen
    ></iframe>
    <h3>{{propsdata.title}}</h3>
    <div class="row">
      <p>{{propsdata.views}} views</p>
      <p>
        {{propsdata.likes}}
        <button>Like</button>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["propsdata"]
};
</script>

<style>
.video_container {
  margin-right: 40px;
}

.row {
  display: flex;
  justify-content: space-between;
}
button {
  padding: 10px 20px;
  background: #d0021b;
  color: white;
  border: none;
  cursor: pointer;
}
</style>