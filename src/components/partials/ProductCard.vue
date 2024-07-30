<script>
  export default {
    props:{
      image: String,
      title: String
    }
  }
</script>



<template>
  <div class="col-12 col-md-3 p-0" >
        <div class="p-0 m-0 product-card">
            <img :src="image" :alt="title">
            <h6 class="text-center text-bold">{{ title }}</h6>
        </div>
  </div>
</template>


<style lang="scss" scoped>
@use '../../styles/partials/variables' as *;
.product-card{
    border:1px solid lighten($brand_color, 65%);
}
</style>  