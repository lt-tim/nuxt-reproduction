<template>
  <div class="link">
<!--    Please note, This link will most likely work since Nuxt does generate a seperate index.html file specifically for this 12 page.
    Using the custom ID function will result in the same behavior as the 12 page.-->
    <a href="/link/12">Dynamic Link #1 - /link/12</a>
    <a href="/link/listall">Static link - /link/listall</a>
    <a href="/link">Index - /link/</a>
  </div>
  <div class="customID">
    <label class="label" for="customID">Put in your custom ID to go to that dynamic link.</label>
    <input id="customID" type="text" v-model="id">
    <a :href="'/link/' + id">Dynamic link #2 - /link/{{id}}</a>
  </div>
</template>

<script>

export default {
  data() {
    return {
      id: ''
    }
  }
}

</script>

<style scoped>

.link {
  display: flex;
  flex-direction: column-reverse;
  gap: 5px;
  font-weight: bold;
}

.customID {
  display: flex;
  flex-direction: column;
  width: 10rem;
  margin-top: 50px;
}

.label {
  margin-bottom: 5px;
  font-size: 15px;
  white-space: nowrap;
}

</style>