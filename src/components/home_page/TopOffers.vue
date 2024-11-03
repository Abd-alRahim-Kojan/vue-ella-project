<template>
    <div class="top-offers bg-grey-lighten-4 py-5">
        <v-container fluid>
            <v-row>
                <v-col cols="4">
                    <v-hover v-slot="{ isHovering, props }">
                        <img src="../../assets/images/playstations.webp" alt="product" width="100%" v-bind="props"
                            :style="`${isHovering ? 'transform: scale(1.05)' : ''}`" class="hover-img" />
                    </v-hover>
                </v-col>

                <v-col cols="4">
                    <v-hover v-slot="{ isHovering, props }">
                        <img src="../../assets/images/headset.webp" alt="product" width="100%" v-bind="props"
                            :style="`${isHovering ? 'transform: scale(1.05)' : ''}`" class="hover-img" />
                    </v-hover>
                </v-col>

                <v-col cols="4">
                    <v-hover v-slot="{ isHovering, props }">
                        <img src="../../assets/images/chairs.webp" alt="product" width="100%" v-bind="props"
                            :style="`${isHovering ? 'transform: scale(1.05)' : ''}`" class="hover-img" />
                    </v-hover>
                </v-col>
            </v-row>

            <v-row>
                <v-col cols="6">
                    <v-hover v-slot="{ isHovering, props }">
                        <img src="../../assets/images/iphones.webp" alt="product" width="100%" v-bind="props"
                            :style="`${isHovering ? 'transform: scale(1.05)' : ''}`" class="hover-img" />
                    </v-hover>
                </v-col>

                <v-col cols="6">
                    <v-hover v-slot="{ isHovering, props }">
                        <img src="../../assets/images/laptops.webp" alt="product" width="100%" v-bind="props"
                            :style="`${isHovering ? 'transform: scale(1.05)' : ''}`" class="hover-img" />
                    </v-hover>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<style lang="scss" scoped>
.hover-img {
    transition: all 0.3s ease;
    padding: 0.5rem 1rem;
    cursor: pointer;
}
</style>