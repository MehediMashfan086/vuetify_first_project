<template>
<v-container class="my-15">
    <v-row justify="center">
        <v-col lg="12" class="text-center">
            <v-subheader class="text-h4 justify-center">Project</v-subheader>
            <p>This is all Projects of my app PhotoGallery</p>
        </v-col>

        <v-col lg="12" v-for="project in 1" :key="project">
            <v-card class="mx-auto my-12" max-width="374">
            <v-img height="250" src="./../assets/project/wedding.jpg"></v-img>

            <v-card-title>Wedding Photography</v-card-title>

            <v-card-text>
                <div>Contact with us for Wedding Photography.
                    <p>Packages start from <b>$500</b> only.</p>
                </div>
            </v-card-text>

            <v-divider class="mx-4"></v-divider>

            <v-card-actions>
                <v-btn color="success" rounded>View Details</v-btn>
                <v-spacer />
                <v-rating 
                    :value="4.5" 
                    color="amber" 
                    dense 
                    half-increments 
                    readonly 
                    size="14">
                </v-rating>
            </v-card-actions>
            
        </v-card>
        </v-col>
    </v-row>
</v-container>
</template>

<script>
    export default {
        name: "Project"
    }
</script>

<style scoped>

</style>
