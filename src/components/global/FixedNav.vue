<template>
    <div class="fixed-nav">
        <v-app-bar color="#02218f" height="4rem">
            <v-container fluid>
                <v-row class="d-flex align-center">
                    <v-col cols="2">
                        <img src="../../assets/images/logo.png" alt="logo" class="w-50">
                    </v-col>

                    <v-col cols="5">
                        <ul class="links d-flex text-white ga-8" style="list-style: none;">
                            <li>Theme Demo</li>
                            <li>Shop</li>
                            <li>Prouducts</li>
                            <li>New In</li>
                            <li>Must Have</li>
                            <li>Collections</li>
                        </ul>
                    </v-col>

                    <v-col cols="5" class="d-flex justify-end align-center ga-4">
                        <v-icon size="2rem" style="color: white;">mdi-magnify</v-icon>

                        <div class="wishlists d-flex flex-column  align-center cursor-pointer" @click="toggleCart">
                            <v-badge color="#007fff" content="2" location="right top" offset-x="-10"
                                style="z-index: 1;"></v-badge>
                            <v-icon color="orange" size="large">mdi-cart-outline</v-icon>
                            <span>Cart</span>
                        </div>
                    </v-col>
                </v-row>
            </v-container>
        </v-app-bar>
    </div>
</template>

<script>
export default {
    inject: ["Emitter"],
    methods: {
        toggleCart() {
            this.Emitter.emit("toggleCart");
        },
    },
}
</script>