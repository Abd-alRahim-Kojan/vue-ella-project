<template>
    <div class="layout">
        <v-layout class="position-relative">

            <CartDrawer />

            <AppNav />
            <FixedNav />

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
import FixedNav from './FixedNav.vue';

export default {
    components: {
        AppNav, CartDrawer, AppFooter, FixedNav
    },
    data() {
        return {
            drawer: false
        }
    }
}
</script>