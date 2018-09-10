<template>
    <router-link :to=to class="no-decoration">
            <v-list-tile>
                <v-list-tile-content>
                <v-list-tile-title>{{title}}</v-list-tile-title>
                </v-list-tile-content>
            </v-list-tile>
    </router-link>
</template>

<script>
export default {
    name: 'DrawerListItem',
    props: ["to", "icon", "title"]
}
</script>
