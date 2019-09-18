<template>
    <div id="footer">
        <v-footer padless id="Contato">
            <v-card width="100%" style="background-color: lightpink">
                <v-card-text class="text-center">
                    <strong><b> Caso queira realizar algum pedido, entre em contato no telefone abaixo ou através das nossas redes sociais<br>
                    Telefone: 5852-9044<br>
                    WhatsApp: (11)98393-3692<br>
                    </b>
                    </strong>
                    <v-btn
                        v-for="icon in icons"
                        :key="icon"
                        class="mx-3"
                        dark
                        icon
                        @click="goToOurSocialNetworks(icon)">
                        <v-icon color="black" size="24px">{{ icon }}</v-icon>
                    </v-btn>
                </v-card-text>
                <v-card-actions class="justify-center pink darken-1" >
                    &copy;2019 — <strong> Leandro Gilberto Silva | leandrogslva@gmail.com | WhatsApp: 97636-6281</strong>
                </v-card-actions>
            </v-card>
        </v-footer>
    </div>
</template>

<script>
export default {
    data () {
        return{
             icons: [
                'fab fa-facebook',
                'fab fa-twitter',
                'fab fa-instagram'
            ]
        }
    },

    methods:{
        goToOurSocialNetworks(icon){
            if(icon == 'fab fa-facebook'){
                window.location.assign('https://www.facebook.com/rosalinda.santos.5095')
            }else if(icon == 'fab fa-twitter'){
                window.location.assign('https://www.twitter.com')
            }else{
                window.location.assign('https://www.instagram.com')
            }
        }
    }
}
</script>

<style scoped>
    #footer{
        height: 100px;
        width: 100%;
    }
</style>
