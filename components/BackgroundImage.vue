<template>
  <div class="bg-container">
    <img src="../assets/images/bg.png" alt="background" />
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      count: 0
    }
  }
}
</script>
<style>
.bg-container{
  width: 100%;
}

.bg-container img{
  width: 100%;
  max-height: 100%;
}
</style>