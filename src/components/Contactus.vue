<template>
<v-container class="my-15">
    <v-row justify="center">
        <v-col lg="12" class="text-center">
            <v-subheader class="text-h4 justify-center">Contact Us</v-subheader>
            <p>This is all Contact US part of my app PhotoGallery</p>
        </v-col>

        <v-col lg="6">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3650.4612453904238!2d90.2541028148912!3d23.802191984563837!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3755ebc21dfd5f95%3A0x4ab17f888ecc4d75!2sMashfan%20Mehedi%E2%80%99s%20Home!5e0!3m2!1sen!2sbd!4v1643806161569!5m2!1sen!2sbd" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
        </v-col>
        <v-col lg="6">
            <form>
                <v-form ref="form">
                    <v-text-field 
                    v-model="contactInfo.name" 
                    :counter="50"
                    label="Name" 
                    required>
                </v-text-field>

                <v-text-field 
                    v-model="contactInfo.email" 
                    label="E-mail" 
                    required>
                </v-text-field>

                <v-textarea label="Message" v-model="contactInfo.message">

                </v-textarea>

                <v-btn color="success" class="mr-4">
                    Send
                </v-btn>
                </v-form>
            </form>
        </v-col>
    </v-row>
</v-container>
</template>

<script>
export default {
    name: "Contactus",
    data() {
        return {
            contactInfo: {}
        }
    }
}
</script>

<style scoped>

</style>
