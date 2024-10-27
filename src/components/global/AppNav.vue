<template>
    <div class="nav-bar">
        <v-app-bar color="#02218f" class="py3" height="fit-content">
            <v-container fluid>
                <v-row>
                    <v-col cols="3">
                        <img src="@/assets/images/logo.png" alt="logo" />
                    </v-col>

                    <v-col cols="5">
                        <div class="search-bar position-relative">
                            <input type="search" name="navSearch" id="navSearch"
                                style="width: 90%; border-radius: 30px; outline: none;" class="py-3 px-5 bg-white"
                                placeholder="Search..." />
                            <v-icon size="large"
                                style="position: absolute; right: 12%; transform: translateY(40%); color: gray;">mdi-magnify</v-icon>
                        </div>
                    </v-col>

                    <v-col cols="4">
                        <div class="parent text-white d-flex align-center justify-end" style="gap: 30px;">
                            <div class="available me-6">
                                <span>Available 24/7</span>
                                <br>
                                <strong>(090) 234-4567</strong>
                            </div>

                            <div class="wishlists d-flex flex-column align-center">
                                <v-icon color="orange" size="large">mdi-heart-outline</v-icon>
                                <span>Wish Lists</span>
                            </div>

                            <div class="wishlists d-flex flex-column align-center">
                                <v-icon color="orange" size="large">mdi-account-outline</v-icon>
                                <span>Sign in</span>
                            </div>

                            <div class="wishlists d-flex flex-column align-center" style="cursor: pointer;"
                                @click="toggleCart">
                                <v-badge color="#007fff" content="2" location="right top" offset-x="-10"
                                    style="z-index: 1;"></v-badge>
                                <v-icon color="orange" size="large">mdi-cart-outline</v-icon>
                                <span>Cart</span>
                            </div>
                        </div>
                    </v-col>

                    <v-col cols="7">
                        <ul class="links d-flex text-white" style="list-style: none; gap: 30px;">
                            <li>Theme Demo</li>
                            <li>Shop</li>
                            <li>Prouducts</li>
                            <li>New In</li>
                            <li>Must Have</li>
                            <li>Collections</li>
                        </ul>
                    </v-col>

                    <v-col cols="5" class="d-flex justify-end" style="gap: 20px;">
                        <div class="help d-flex align-center" style="gap: 5px;">
                            <v-icon color="orange" size="large">mdi-face-agent</v-icon>
                            <span>Help</span>
                        </div>

                        <div class="lang d-flex align-center" style="gap: 5px;">
                            <v-menu>
                                <template v-slot:activator="{ props }">
                                    <div v-bind="props" class="d-flex align-center" style="gap: 5px; cursor: pointer;">
                                        <v-icon color="orange" size="large">mdi-translate</v-icon>
                                        <span>{{ selectedLang.lang }} / {{ selectedLang.currency }}</span>
                                        <v-icon color="orange" size="large">mdi-chevron-down</v-icon>
                                    </div>
                                </template>
                                <v-list>
                                    <v-list-item v-for="item in langs" :key="item.lang" :value="item"
                                        @click="selectedLang = item">
                                        <v-list-item-title>{{ item.lang }} / {{ item.currency }}</v-list-item-title>
                                    </v-list-item>
                                </v-list>
                            </v-menu>
                        </div>
                    </v-col>
                </v-row>
            </v-container>
            <!-- <v-app-bar-nav-icon @click="toggleCart"></v-app-bar-nav-icon> -->
        </v-app-bar>
    </div>
</template>

<script>
export default {
    inject: ["Emitter"],
    data() {
        return {
            selectedLang: null,
            langs: [
                { icon: 'mdi-flag-usa', lang: 'EN', currency: 'USD' },
                { icon: 'mdi-flag-germany', lang: 'DE', currency: 'EURO' },
                { icon: 'mdi-flag-france', lang: 'FR', currency: 'EURO' },
                { icon: 'mdi-flag-spain', lang: 'ES', currency: 'EURO' },
            ]
        }
    },
    created() {
        this.selectedLang = this.langs[0];
    },
    methods: {
        toggleCart() {
            this.Emitter.emit("toggleCart");
        },
    },
}
</script>