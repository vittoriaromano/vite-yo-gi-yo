<script>
import axios from 'axios';
import CharacterCard from './CharacterCard.vue';

export default{
    name: 'CardList',
    components:{
        CharacterCard
    },
    data(){
        return{
            characters:[],
        }
    },
    created(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
           .then((response) => (console.log(response)));
             this.characters = response.data.results
    }
}

</script>
<template>
    <div class="list-cont">
       <div class="col" v-for="character in characters">
        <CharacterCard></CharacterCard>
       </div>
    </div>
</template>



<style lang="scss" scoped>
.list-cont{
    max-width: 80%;
}
</style>