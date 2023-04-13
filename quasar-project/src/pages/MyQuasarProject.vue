<template>
    <div>
        <h1 class="titre">My Quasar Project</h1>
    </div>
    
    <q-layout>
        <q-page>
            <q-col class="left-col">
                <ListTechno />
            </q-col>
            <q-col class="right-col" >
                    <AddNewTechno />
            </q-col>
        </q-page>
    </q-layout>

</template>
  
<script>
  import { defineComponent } from 'vue';
  import ListTechno from '../components/ListTechno.vue';
  import AddNewTechno from '../components/AddNewTechno.vue';

  export default defineComponent({
    name: 'MyQuasarProject',
    components: {
        ListTechno,
        AddNewTechno
    }
  
  })
  </script>
  

<style>
.titre {
  font-size: 8rem;
  text-align: center;
}

.left-col {
  width: 50%;
  float: left;
}
.right-col {
  width: 50%;
  float: right;
}
</style>