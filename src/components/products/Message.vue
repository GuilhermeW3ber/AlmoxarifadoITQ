<template>
  <div class="message-container">
    <p>{{ msg }}</p>
  </div>
</template>

<script>
/* eslint-disable */
  export default {
    name: "Message",
    props:{
        msg:String,
    }
  };
</script>
  
<style scoped>
    @import '../../css/Styles.scss';
</style>
  