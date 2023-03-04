<script>
   export default {
      data() {
         return {
            content: "Hello, see you again!!!",
            isDisable: true,
            number: 1,
            users: [
               {id:1,name: 'khanh'},
               {id:2,name: 'Nam'},
               {id:3,name: 'Trung'},
               {id:4,name: 'Thanh'}
            ]
         }
      },
      methods: {
         changeText() {
            this.number++
         }
      }
   }
</script>

<template>
   <div>
      <h2>{{ isDisable ? content : 'Content is false' }}</h2>
      <h1 class="title__learn" :class="{content : isDisable, header__title : isDisable}">Learn more about</h1>
      <h1>{{ number }}</h1>
      <button @click="changeText">Click me!!!</button>
   </div>
</template>

<style scoped>

</style>
