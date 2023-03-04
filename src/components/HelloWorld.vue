<script>
export default {
   data() {
      return {
         subjects: [
            {id:1, subject: 'Javascript'},
            {id:2, subject: 'VueJS'},
            {id:3, subject: 'ReactJs'},
            {id:4, subject: 'HTML'}
         ],
      }
   }
}
</script>

<template>
   <ul>
      <li 
         v-for="subject in subjects" 
         :key="subject.id"
      >
         {{ subject.subject }}
      </li>
   </ul>
</template>

<style scoped>
.text-danger {
   color: green;
}
</style>
