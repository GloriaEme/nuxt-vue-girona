<template>
    <v-app>
        <v-container>
            <v-row>
                <v-col>
                    <h2>
                        <nuxt-link to="/porfoli">
                            JORDI GASAU
                        </nuxt-link>
                    </h2>
                </v-col>
                <v-col align="end">
                    <nuxt-link to="/sobre-mi">Sobre mi</nuxt-link>
                    <nuxt-link to="/contacte">Contacte</nuxt-link>
                    <nuxt-link to="/portafoli">Portafoli</nuxt-link>
                    <nuxt-link to="/shop">Shop</nuxt-link>
                </v-col>
            </v-row>
        </v-container>
        <v-main>
            <v-container>
                <v-row>
                    <v-col 
                        cols="12"
                        md="8"
                    
                    >
                        <nuxt/>
                    </v-col>
                    <v-col
                        cols="12"
                        md="4"
                    
                    >
                        <v-img
                            src="https://images.pexels.com/photos/355863/pexels-photo-355863.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
                            height="100vh"
                            >
                        </v-img>
                    </v-col>
                </v-row>
            </v-container>
        </v-main>
        <v-footer>
            <v-container>
                <v-row>
                    <v-col align="center">
                        Tots els drets reservats Jordi Gasau 2022
                    </v-col>
                </v-row>
            </v-container>
        </v-footer>
    </v-app> 
</template>