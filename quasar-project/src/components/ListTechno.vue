<template>
    <div>
      <div v-for="techno in listTechno" :key="techno.id">
        <img src="../techno.png" alt="techno" />
        <h2>{{ techno.label }}</h2>
        <p class="descriptiontechno">{{ techno.text }}</p>
      </div>
    </div>
</template>
  
<script>
  import data from '../data.json';
  
  export default {
    name: 'ListTechno',
    data() {
      return {
        listTechno: data.techno
      }
    }
  }
</script>
  
<style>

.descriptiontechno {
  font-size: 1.8rem;
}

</style>