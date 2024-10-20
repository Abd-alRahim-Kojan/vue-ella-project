<!-- Side NavBar === drawer -->
<template>
    <div class="app-drawer">
        <v-navigation-drawer v-model="drawer" location="right" temporary>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quod vero sapiente ullam nam delectus,
                velit odit qui quibusdam distinctio, ipsa vitae illo aliquid. Praesentium, laboriosam dolorem modi
                tenetur libero blanditiis.</p>
        </v-navigation-drawer>
    </div>
</template>

<script>
export default {
    inject: ["Emitter"],
    data() {
        return {
            drawer: false
        }
    },
    mounted() {
        this.Emitter.on("toggleCart", () => {
            this.drawer = true;
        });
    }
}
</script>