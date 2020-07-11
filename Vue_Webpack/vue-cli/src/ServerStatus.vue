<template>
  <div>
   <p>Server Status: {{ status }} </p>
    <br>
    <button @click="changeStatus">changeStatus</button>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        statusCheck: true,
        status: 'status check is good'
      }
    },
    methods: {
       changeStatus() {
         this.statusCheck = !this.statusCheck;
         console.log(this.statusCheck);
         this.status = this.statusCheck ? "status check is good" : "status is bad"
       }
    }
  }
</script>
