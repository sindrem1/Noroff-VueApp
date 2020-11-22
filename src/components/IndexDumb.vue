<template>
  <div class="card">
    <img :src="img">
      <h2>{{ title }}</h2>
      <br/>
      <p>{{ ingredients }}</p>
      <br/>
      <a :href="link">View full recipe</a>
    </div>
</template>

<script>
export default {
  name: "IndexDumb",
  props: ["img", "title", "ingredients", "link"],
};
</script>

<style scoped>

.row:after {
  content: "";
  display: table;
  clear: both;
}

.card {
  float: left;
  width: 20%;
  height: 400px;
  margin: auto;
  color: black;
  text-align: center;
  padding-bottom: 15px;
}

</style>
