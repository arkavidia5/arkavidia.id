<template >
    <v-container>
        <router-link to="/" class="no-decoration">
        <v-layout flex flex-column align-center style="margin-top: 10%;" not-found>
            <img src="https://static.arkavidia.id/5/images/logo.svg" alt="" height="150">
            <h1>Page Not Found :(</h1>
        </v-layout>
        </router-link>
    </v-container>
</template>
<script>
export default {
    name: 'NotFound'
}
</script>
<style scoped>
    .not-found {
        filter: grayscale(0.9);
        transition: 0.5s ease-in-out;
    }
    .not-found:hover {
        filter: none;
        transition: 0.5s ease-in-out;
    }
</style>

