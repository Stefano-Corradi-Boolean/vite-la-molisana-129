<script>
import { pastificioMenu, prodottiMenu } from '../data/menues';
export default {
    data(){
        return{
            pastificioMenu,
            prodottiMenu
        }
    },
    methods: {
        getImageUrl(path) {
            return new URL(path, import.meta.url).href;
        }
    }
}
</script>
<template lang="">
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-12 col-md-4">
                    <a href="/">
                        <img src="/la-molisana-logo.png" class="logo-footer" alt="La molisana">
                    </a>
                </div>
                <div class="col-12 col-md-4">
                    <h4>Pastificio</h4>
                    <ul class="list-unstyled">
                        <li
                          v-for="item, index in pastificioMenu"
                          :key="`ip-${index}`"
                        >
                            <a :href="item.href">{{item.text}}</a>
                        </li>
                    </ul>
                </div>
                <div class="col-12 col-md-4">
                    <h4>Prodotti</h4>
                    <ul class="list-unstyled">
                        <li
                          v-for="item, index in prodottiMenu"
                          :key="`ip-${index}`"
                        >
                            <a :href="item.href">{{item.text}}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
        <img :src="getImageUrl('../assets/img/footer-montagne-bottom.jpg')">
    </footer>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

footer {
    padding: 50px 0px;

    h4 {
        text-transform: uppercase;
    }

    a {
        text-decoration: none;
        color: #000;
        transition: color 0.3s;

        &:hover {
            color: $primary_color;
        }
    }

    img {
        max-width: 100%;
    }

}
</style>