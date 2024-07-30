<script>
  export default {
    props:{
      linkData: Object
    }
  }
</script>


<template>
  <li :class="{'active' : linkData.current}"  >
      <a :href="linkData.url">{{ linkData.label }}</a>
  </li>
</template>



<style lang="scss" scoped>
@use '../../styles/partials/variables' as *;
li {
        padding: 20px 30px;

        a {
            text-decoration: none;
            color: #000;
            transition: font-weight 0.3s;

            &:hover {
                font-weight: 800;
            }
        }
      &.active {
          // background-color: $primary_color;
          background-color: lighten($brand_color, 65%);
      }
    }

</style>