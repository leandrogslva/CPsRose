<template>
    <div>
        <img src="../imagens/header_wallpaper.jpg" id="header">
        <v-toolbar  class="pink darken-1" id="">
            <template>
                <v-tabs
                v-model="tab"
                centered
                background-color="transparent"
                >
                    <v-tabs-slider color="pink lighten-4"></v-tabs-slider>
                    <v-tab v-for="item in menu" :key="item" >
                            <a style="color: white; text-decoration: none;" :href="'#' + item">{{ item }}</a>
                    </v-tab>
                </v-tabs>
            </template>
        </v-toolbar>
    </div>
</template>
<script>
export default {
    data(){
        return{
            tab: null,
            menu: ['Boticario', 'Natura', 'Hinode', 'Eudora','Contato'],
        }
    }
}
</script>
<style >
    #header{
        height: 400px;
        width: 100%;
        padding: 0px;
        margin: 0px;
    }
    h2{
        text-align: left;
        color: purple;
        margin-top: 100px;
    }
</style>