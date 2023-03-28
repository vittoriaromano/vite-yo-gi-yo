<script>
export default{
    name: 'CharacterCard',
    props:{
      img: String,
      name: String,
      type: {
        default: 'Generic',
        type: String
      }
    }
}
</script>

<template>
    <div>
      <!-- <img :src="img" :alt="name"> -->
    </div>
    <div>{{ name }}</div>
    <div>{{ type }}</div>
</template>



<style lang="scss" scoped>

</style>