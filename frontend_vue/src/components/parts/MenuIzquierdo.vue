<template>
    <v-container>
        <v-navigation-drawer v-model="drawer" :color="isColor" permanent app expand-on-hover dark>
            <v-list>
                <v-list-item v-for="item in items" :key="item.title" :to="item.url">
                    <v-list-item-icon>
                        <v-icon>{{ item.icon }}</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <v-list-item-title>{{ item.title }}</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </v-container>
</template>

<script>
    export default {
        name: 'MenuIzquierdo',
        data: () => ({
            drawer: true,
            items: [
                { title: 'Inicio', icon: 'home', url: '/clases' },
                { title: 'Mi perfil', icon: 'perm_identity', url: '/perfil' },
                { title: 'Mis Cursos', icon: 'videocam', url: '/cursos' },
                { title: 'Monitorias', icon: 'chat', url: '/monitorias' },
                { title: 'Llamadas', icon: 'phone', url: '/phone' },
                { title: 'Calendario', icon: 'event', url: '/phone' },
                { title: 'Buscar', icon: 'search', url: '/buscar' },
            ],
        }),
        computed:{
            isColor: function(){
                if (this.$vuetify.theme.dark){
                    return 'rgba(0, 0, 0, 0.747)';
                }else{
                    return 'rgba(0, 24, 88, 0.712)';
                }
            }
        },
    }
</script>

<style scoped>
    .aaa{
        color: #071838be;
    }
</style>