<script>
import { mainMenu } from '../data/menues';
import ItemMenu from './partials/ItemMenu.vue';

export default {
    components:{
        ItemMenu
    },
    data() {
        return {
            mainMenu
        }
    }
}
</script>
<template lang="">
    <header>
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="text-center">
                        <img src="/la-molisana-logo.png" alt="La molisana" >
                    </div>
                </div>
                <div class="col-12">
                    <ul class="list-unstyled mt-5 d-flex justify-content-center">
                        <ItemMenu
                          v-for="link, index in mainMenu"
                          :key="`mm-${index}`"
                          :linkData="link"
                        />
                        <!-- <li
                          v-for="link, index in mainMenu"
                          :key="`mm-${index}`"
                          :class="{'active': link.current}"
                        >
                            <a :href="link.url">{{ link.label }}</a>
                        </li> -->
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

ul {
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
    }

    .active {
        // background-color: $primary_color;
        background-color: lighten($brand_color, 65%);
    }
}
</style>