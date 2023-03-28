<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

import axios from 'axios';
import { store } from './store';


export default{
  name: 'App',
  components:{
    AppHeader,
    AppMain,
  },
   data(){
        return{
          //axios,
          store,

        }
    },
    methods:{
      callCard(){
          axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
           .then((response) => {
            this.store.cards = response.data.slice(0,20);
            this.store.lengthSearch = this.store.cards.length
            console.log(response)
           });
             
      }
    },
    created(){
      this.callCard()
    }
}
</script>

<template>
  <AppHeader />
  <AppMain />
</template>

<style lang="scss">

</style>
