<template>
<v-app id="inspire">
    <Header @handleDrawer="drawer=!drawer"/>
    <SideBar :drawer="drawer"/>
    <v-main>
        <v-container class="py-8 px-6" fluid>
            <router-view></router-view>
        </v-container>
    </v-main>
</v-app>
</template>

<script>
import Header from './components/Header.vue';
import SideBar from './components/SideBar.vue';
export default {
    data: () => ({
        cards: ['Today', 'Yesterday'],
        drawer: true,
    }),

    components:{
        Header,
        SideBar,
    }
}
</script>
