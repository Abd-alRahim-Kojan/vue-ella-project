<template>
    <div class="nav-bar">
        <v-app-bar>
            <v-app-bar-nav-icon @click="toggleCart"></v-app-bar-nav-icon>
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