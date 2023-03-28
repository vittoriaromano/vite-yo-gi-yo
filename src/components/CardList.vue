<script >
//import axios from 'axios';
import CharacterCard from './CharacterCard.vue';
import { store } from '../store';
export default{
    name: 'CardList',
    components:{
        CharacterCard
    },
    data(){
        return{
            //axios,
            store,
        }
    },
    
}

</script>
<template>
    <div class="list-cont">
       <div class="col" v-for="character in store.cards">
        <CharacterCard :img="character.character_images[0].image_url" :name="character.name"></CharacterCard>
       </div>
    </div>
</template>



<style lang="scss" scoped>
.list-cont{
    max-width: 80%;
    .col{
        width: calc(100% / 4);
    }
}

</style>