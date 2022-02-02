<template>
    <v-container class="pt-15">
        <v-row>
            <v-col lg="6">
                <h2 class="intro-text">Welcome to PhotoGallery.</h2>
                <p class="description">A welcome message for new visitors to your website is a big attraction point for action.
                    If you can’t hook their interest with a prominent welcome message then you will probably 
                    lose them. Your homepage messaging is critical because you want your visitors to be intrigued
                    enough to venture further onto your website and not just click off.</p>

                <v-btn color="success" class="white--text mr-10" rounded>Get Started</v-btn>
                <v-btn color="indigo" class="white--text" rounded>
                    <v-icon>mdi-play-circle</v-icon>Watch Video
                </v-btn>
            </v-col>
                <img src="./../assets/hero_img.png" alt="" width="100%">
            <v-col>

            </v-col>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        name: "HeaderComponent"
    }
</script>

<style scoped>
    h2.intro-text {
        font-size: 60px;
        font-weight: bold;
        font-family: cursive;
        color: #444;
    }

    p.description {
        font-size: 19px;
        font-family: cursive;
        margin: 32px 0px;
        color: #444444ba;
    }
</style>