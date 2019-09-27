<template>
    <div>
        <v-card height="50px" class="text-center pink darken-1">
            <v-card-text style="color: white">
                <v-icon color="white">mdi-phone</v-icon>
                Telefone: (11)5852-9044 /
                <v-icon color="white">mdi-whatsapp</v-icon>
                WhatsApp: (11)98393-3692 /
                <v-icon color="white">mdi-car</v-icon>
                Frete grátis
            </v-card-text>
        </v-card>
        <img src="../imagens/header_wallpaper.jpg" id="header">
        <v-toolbar  class="pink darken-1">
            <template>
                <v-tabs
                v-model="tab"
                centered
                background-color="transparent"
                >
                    <v-tabs-slider color="pink lighten-4"></v-tabs-slider>
                    <v-tab v-for="item in menu" :key="item" >
                        <a style="color: white; text-decoration: none;" :href="'#' + item">
                            <v-btn text 
                            large
                            color="white">
                                {{ item }}
                            </v-btn>
                        </a>
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
            menu: ['Boticario', 'Natura', 'Hinode', 'Eudora', 'Contato'],
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
    
</style>