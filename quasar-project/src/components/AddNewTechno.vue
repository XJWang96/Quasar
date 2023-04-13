<template>
    <div>
        <h2>Your favorite techno</h2>
    </div>
    <div>
        <input class="inputAddTechno" v-model="newTechnoFavorite" placeholder="Write your favorite techno" />
    </div>
    <div>
        <button  class="buttonAddTechno"  @click="addTechno" >Add</button>
    </div>

    <div>
        <h2>My favoitre techno are</h2>
    </div>
    <div v-for="technoFavorite in listTechnoFavorite" :key="technoFavorite.id">
        <p class="pTechnoFavorite">{{ technoFavorite.text }}</p>
    </div>


</template>
  
<script>
  export default {
    name: 'AddNewTechno',

  
  data() {
    return {
        //newTechnoFavorite: '',
        listTechnoFavorite: [
          { id: 1, text: 'JavaScript' },
          { id: 2, text: 'HTML' },
          { id: 3, text: 'CSS' },
        ]
    }
  },
  methods: {
    addTechno(){
        const newTechno = {
          id: this.listTechnoFavorite.length + 1,
          text: this.newTechnoFavorite
        };
        this.listTechnoFavorite.push(newTechno);
        this.newTechnoFavorite = '';
    }
  }
}
</script>
  
<style>
.inputAddTechno{
  font-size: 1.8rem;
}
.buttonAddTechno{
  font-size: 1.6rem;
}
.pTechnoFavorite{
    font-size: 1.6rem;
}


</style>

