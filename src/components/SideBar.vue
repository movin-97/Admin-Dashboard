<template>
<v-navigation-drawer v-model="drawer" app>
    <v-sheet color="grey lighten-4" class="pa-2">
        <v-img src="https://png.pngtree.com/thumb_back/fh260/background/20200714/pngtree-modern-double-color-futuristic-neon-background-image_351866.jpg" class="pa-4">
            <div class="text-center">
                <v-avatar class="mb-4" color="grey darken-1" size="64">
                    <v-img aspect-ratio="30" src="https://helostatus.com/wp-content/uploads/2021/08/profile-pictures-for-WhatsApp.jpg"></v-img>
                </v-avatar>
                <h4 class="white--text">thanamovin1997@gmail.com</h4>
            </div>
        </v-img>
    </v-sheet>

    <v-divider></v-divider>

    <v-list>
        <v-list-item v-for="[icon, text] in links" :key="icon" link>
            <v-list-item-icon>
                <v-icon>{{ icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
                <v-list-item-title>{{ text }}</v-list-item-title>
            </v-list-item-content>
        </v-list-item>
    </v-list>
</v-navigation-drawer>
</template>

<script>
export default {
    data() {
        return {
            links: [
                ['mdi-view-dashboard', 'Dashboard'],
                ['mdi-account', 'Profile'],
                ['mdi-ticket', 'Activity'],
                ['mdi-cog-box', 'Setting'],
            ],
        }
    },
    props:['drawer']
}
</script>

<style scoped>

</style>
