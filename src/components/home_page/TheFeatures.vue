<template>
    <div class="features py-5">
        <v-contaier>
            <v-row>
                <v-col>
                    <div class="parent d-flex align-center justify-center" style="gap: 1rem;">
                        <v-icon color="#02218f" size="2.5rem">mdi-truck-fast</v-icon>
                        <span>Free Shipping & Returens</span>
                    </div>
                </v-col>

                <v-col>
                    <div class="parent d-flex align-center justify-center saprator" style="gap: 1rem;">
                        <v-icon color="#02218f" size="2.5rem">mdi-seal-variant</v-icon>
                        <span>Lowest Price Guarantee</span>
                    </div>
                </v-col>

                <v-col>
                    <div class="parent d-flex align-center justify-center saprator" style="gap: 1rem;">
                        <v-icon color="#02218f" size="2.5rem">mdi mdi-trophy-award</v-icon>
                        <span>Longest Warranties Offer</span>
                    </div>
                </v-col>
            </v-row>
        </v-contaier>
    </div>
</template>

<style lang="scss" scoped>
.saprator {
    position: relative;
    &::before {
        content: '';
        position: absolute;
        background-color: #a1a1a1;
        left: 0;
        top: 50%;
        transform: translateY(-50%);
        width: 1px;
        height: 70%;
        bottom: -10px;
    }
}
</style>