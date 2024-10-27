<template>
    <div class="banner">
        <div class="parent">
            <div class="banner-content">
                <v-container>
                    <v-row>
                        <v-col cols="6" class="d-flex align-center justify-center">
                            <div class="content">
                                <h3><span>Huge Saving</span> on UHD Televisions</h3>
                                <p>Sale up to 70% off on selected items*</p>
                                <v-btn variant="outlined" class="btn-shop">Shop Now!</v-btn>
                            </div>
                        </v-col>
                    </v-row>
                </v-container>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.parent {
    background-image: url('../../assets/images/banner-bg.jpg');
    height: 50vh;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    .content {
        color: #fff;
        padding: 40px 0 0 100px;
        h3 {
            font-size: 45px;
            font-weight: 900;
            span {
                color: #00fff7
            }
        }
        p {
            font-size: 20px;
            margin-top: 10px;
        }
        .btn-shop {
            margin-top: 60px;
            padding: 20px 40px;
            display: flex;
            border-radius: 30px;
            text-transform:none
        }
    }
}
</style>