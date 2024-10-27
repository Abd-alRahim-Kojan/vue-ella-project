<template>
    <div class="layout">
        <v-layout>

            <CartDrawer />

            <AppNav />

            <v-main style="padding-top: 130px;">
                <slot></slot>
            </v-main>

            <AppFooter />

        </v-layout>
    </div>
</template>

<script>
import AppNav from './AppNav.vue';
import CartDrawer from './CartDrawer.vue';
import AppFooter from './AppFooter.vue';

export default {
    components: {
        AppNav, CartDrawer, AppFooter
    },
    data() {
        return {
            drawer: false
        }
    }
}
</script>