<template>
    <div id="body">
        <section>
            <h1>Sobre</h1>
            <v-container grid-list-xs>
                <v-layout row wrap class="text-center mr-12">
                    <v-flex xs4> 
                        <h2> <v-icon x-large>mdi-map</v-icon> Onde atuamos </h2>
                        <p>Atuo na região zona sul de São Paulo, no bairro Jardim São Francisco de Assis.</p>
                    </v-flex>
                    <v-flex xs4>
                        <h2> <v-icon x-large>mdi-briefcase</v-icon> Como atuamos </h2>
                        <p>Atualmente atendo por redes sociais ou pessoalmente, onde, após a realização do pedido, a entrega 
                        é realizada pessoalmente tendo um local de encontro combinado por ambos.</p>
                    </v-flex>
                    <v-flex xs4>
                        <h2> <v-icon x-large>mdi-bank</v-icon> O que valorizamos </h2>
                        <p>Eficiência na entrega e a ótima qualidade do produto são os pilares do serviço.</p>
                    </v-flex>
                </v-layout>
            </v-container>
        </section>
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
                        <a style="text-decoration: none; color: black" href="https://firebasestorage.googleapis.com/v0/b/cosmeticos-rose.appspot.com/o/boticario_ciclo14.pdf?alt=media&token=8f34ab3a-607b-472f-8159-8a7a0ee3abeb" target="_blank"> 
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
                        <a style="text-decoration: none; color: black" href="https://firebasestorage.googleapis.com/v0/b/cosmeticos-rose.appspot.com/o/natura_ciclo16.pdf?alt=media&token=7b245c47-f8a8-42b2-ac53-bf086b5adfd9" target="_blank"> 
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
                        <a style="text-decoration: none; color: black" href="https://firebasestorage.googleapis.com/v0/b/cosmeticos-rose.appspot.com/o/hinode_ciclo3.pdf?alt=media&token=65beb1dd-0a38-4012-8f64-63b6c411634a" target="_blank"> 
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
                        <a style="text-decoration: none; color: black" href="https://firebasestorage.googleapis.com/v0/b/cosmeticos-rose.appspot.com/o/eudora_ciclo13.pdf?alt=media&token=00a860d0-0902-4e1d-a3fc-2127ae57be8f" target="_blank"> 
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
    h2{
        font-size: 25px;
        font-family: 'Times New Roman';
    }
    p{
        font-size: 20px;
        margin-left: 20px;
        font-family: 'Times New Roman';
        
    }
    section{
        min-height: 300px;
        margin-left: 35px;
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