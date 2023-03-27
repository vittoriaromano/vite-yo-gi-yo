<script>
import CharacterCard from './CharacterCard.vue';
export default{
    name: 'CardList',
    components:{
        CharacterCard
    }
}

</script>
<template>
    <div class="list-cont">
       <div class="col">
        <CharacterCard></CharacterCard>
       </div>
    </div>
</template>



<style lang="scss" scoped>
.list-cont{
    max-width: 80%;
}
</style>