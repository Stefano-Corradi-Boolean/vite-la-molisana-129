<script>

import pastas from '../data/products'
import ProductCard from './partials/ProductCard.vue'

export default {
    props:{
        mainTitle: String
    },
    components:{
        ProductCard
    },
    data() {
        return {
            pastas
        }
    }
}
</script>
<template lang="">
    <main>
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <h2 class="text-center py-5">{{ mainTitle }}</h2>
                </div>

                <ProductCard
                  v-for="pasta in pastas"
                  :key="`p-${pasta.id}`"
                  :image="pasta.src"
                  :title="pasta.titolo"
                />

            </div>
        </div>
    </main>
</template>
<style lang="scss" scoped>
main {
    background-image: url('../assets/img/fondo-pag-speciali.jpg');
    background-size: cover;
}
</style>
