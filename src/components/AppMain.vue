<script>
import CardSearch from './CardSearch.vue';
import CardList from './CardList.vue';
export default{
    name:'Main',
    components: {
        CardSearch,
        CardList
    }
}
</script>
<template>
    <main>
        <CardSearch></CardSearch>
        <CardList></CardList>
    </main>
</template>



<style lang="scss" scoped>
//@use './assets/scss/main.scss/variables.scss';
main{
    background-color: orange;
    display: flex;
    flex-direction: column;
    height: 100vh;
    align-items: center;
}
</style>