<template>
  <div>
    <h1>You are now on the dynamic page of /link/[id] with the dynamic id of {{id}}</h1>
    <a href="/">Go back to index - /</a>
  </div>
</template>
<script setup lang="ts">

let router = useRoute()
let id = router.params.id

</script>