<template>
    <div id="body">

        <section id="Boticario">
            <v-container grid-list-xs>
                <h1>Boticario</h1>
                <v-layout row wrap>
                    <v-flex  v-for="numero in numeroDosItens" :key="numero">
                        <a :href="urlBoticario(numero)">
                            <img :src="urlBoticario(numero)">
                        </a>
                    </v-flex>
                </v-layout>
                <div class="text-center mt-4">
                    <v-btn text>
                        <a style="text-decoration: none; color: black" href="https://firebasestorage.googleapis.com/v0/b/cosmeticos-rose.appspot.com/o/catalogo_boticario.pdf?alt=media&token=58ddd4e8-c3f7-4b05-bf90-c006a88a6a29" target="_blank"> 
                            <v-icon >mdi-download</v-icon> Catálogo completo
                        </a>
                    </v-btn>
                    <v-btn text>
                        <a style="text-decoration: none; color: black" href="#">Voltar ao topo <v-icon>mdi-arrow-up</v-icon></a>
                    </v-btn>
                </div>
            </v-container>
        </section>
       
        <section id="Natura">
            <v-container grid-list-xs>
                <h1>Natura</h1>
                <v-layout row wrap>
                    <v-flex  v-for="numero in numeroDosItens" :key="numero">
                        <a :href="urlNatura(numero)">
                            <img :src="urlNatura(numero)">
                        </a>
                    </v-flex>
                </v-layout>
                <div class="text-center mt-4">
                    <v-btn text >
                        <a style="text-decoration: none; color: black" href="https://firebasestorage.googleapis.com/v0/b/cosmeticos-rose.appspot.com/o/catalogo_natura.pdf?alt=media&token=8d1df2e1-0628-4183-9841-4f8216506881" target="_blank"> 
                            <v-icon >mdi-download</v-icon> Catálogo completo
                        </a>
                    </v-btn>
                    <v-btn text>
                        <a style="text-decoration: none; color: black" href="#">Voltar ao topo <v-icon>mdi-arrow-up</v-icon></a>
                    </v-btn>
                </div>
            </v-container>
        </section>

        <section id="Hinode">
            <v-container grid-list-xs>
                <h1>Hinode</h1>
                <v-layout row wrap>
                    <v-flex v-for="numero in numeroDosItens" :key="numero">
                        <a :href="urlHinode(numero)">
                            <img :src="urlHinode(numero)">
                        </a>
                    </v-flex>
                </v-layout>
                <div class="text-center mt-4">
                    <v-btn text >
                        <a style="text-decoration: none; color: black" href="https://firebasestorage.googleapis.com/v0/b/cosmeticos-rose.appspot.com/o/catalogo_hinode.pdf?alt=media&token=418c9ab3-c134-485d-bdbf-cfadfd9a96d6" target="_blank"> 
                            <v-icon >mdi-download</v-icon>  Catálogo completo
                        </a>
                    </v-btn>
                    <v-btn text >
                        <a style="text-decoration: none; color: black" href="#">Voltar ao topo <v-icon>mdi-arrow-up</v-icon></a>
                    </v-btn>
                </div>
                
            </v-container>
        </section>

        <section id="Eudora">
            <v-container grid-list-xs>
                <h1>Eudora</h1>
                <v-layout row wrap>
                    <v-flex v-for="numero in numeroDosItens" :key="numero">
                        <a :href="urlEudora(numero)">
                            <img :src="urlEudora(numero)">
                        </a>
                    </v-flex>
                </v-layout>
                <div class="text-center mt-4">
                    <v-btn text >
                        <a style="text-decoration: none; color: black" href="https://firebasestorage.googleapis.com/v0/b/cosmeticos-rose.appspot.com/o/catalogo_eudora.pdf?alt=media&token=e5dbbe99-2ca2-40e0-bb3a-c9dbf0f76627" target="_blank"> 
                            <v-icon >mdi-download</v-icon> Catálogo completo
                        </a>
                    </v-btn>
                    <v-btn text >
                        <a style="text-decoration: none; color: black" href="#">Voltar ao topo <v-icon>mdi-arrow-up</v-icon></a>
                    </v-btn>
                </div>
            </v-container>
        </section>
        
    </div>
</template>
<script>
export default {
    data(){
        return{
            numeroDosItens: [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15],
        }
    },
    methods: {
        urlBoticario(numero) {
            return require(`../imagens/boticario/${numero}.jpg`);
        },
        urlNatura(numero) {
            return require(`../imagens/natura/${numero}.jpg`);
        },
        urlHinode(numero) {
            return require(`../imagens/hinode/${numero}.jpg`);
        },
        urlEudora(numero) {
            return require(`../imagens/eudora/${numero}.jpg`);
        }
    }
}
</script>
<style>
    #body{
        min-height: 500px;
        background-color: lightgrey;
    }
    h1{
        text-align: center;
        font-family: 'Times New Roman';
    }
    section{
        min-height: 300px;
    }
    img{
        margin-top: 5px; 
        height: 300px;
        width: 240px;
    }
    html{
        scroll-behavior: smooth;
    }
</style>