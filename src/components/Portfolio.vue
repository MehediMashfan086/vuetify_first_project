<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
                <v-subheader class="text-h4 justify-center">Portfolio</v-subheader>
                <p>This is the portfolio of my app PhotoGallery</p>
            </v-col>

            <v-col lg="12">
                <div class="text-center">
                    <v-chip @click="activePortfolio = 'naturephoto'" :color="activePortfolio == 'naturephoto'? 'success': ''" class="mx-5">Nature's Photo</v-chip>
                    <v-chip @click="activePortfolio = 'flowerphoto'" :color="activePortfolio == 'flowerphoto'? 'success': ''" class="mx-5">Flower's Photo</v-chip>
                    <v-chip @click="activePortfolio = 'fruitphoto'" :color="activePortfolio == 'fruitphoto'? 'success': ''" class="mx-5">Fruit's Photo</v-chip>
                </div>
            </v-col>
            <slot v-if="activePortfolio == 'naturephoto' ">
                <v-col lg="3" v-for="(nature, natureindex) in naturePhotos" :key="natureindex">
                    <v-card>
                        <v-img
                            :src="nature.image"
                            class="white--text align-end"
                            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                            height="200px"
                        >
                            <v-card-title>{{nature.title}}</v-card-title>
                        </v-img>
                    </v-card>
                </v-col>
            </slot>

            <slot v-if="activePortfolio == 'flowerphoto' ">
                <v-col lg="3" v-for="(flower, flowerindex) in flowerPhotos" :key="flowerindex">
                    <v-card>
                        <v-img
                            :src="flower.image"
                            class="white--text align-end"
                            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                            height="200px"
                        >
                            <v-card-title>{{flower.title}}</v-card-title>
                        </v-img>
                    </v-card>
                </v-col>
            </slot>

            <slot v-if="activePortfolio == 'fruitphoto' ">
                <v-col lg="3" v-for="(fruit, fruitindex) in fruitPhotos" :key="fruitindex">
                    <v-card>
                        <v-img
                            :src="fruit.image"
                            class="white--text align-end"
                            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                            height="200px"
                        >
                            <v-card-title>{{fruit.title}}</v-card-title>
                        </v-img>
                    </v-card>
                </v-col>
            </slot>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        name: "Portfolio",
        data() {
            return {
                activePortfolio: 'naturephoto',
                naturePhotos: [
                    {title: 'Nature Photo 1', image:'https://wi.wallpapertip.com/wsimgs/195-1950441_sunset-mountain-picture-nature.jpg'},
                    {title: 'Nature Photo 2', image:'https://picsum.photos/id/1015/367/267'},
                    {title: 'Nature Photo 3', image:'https://nuforest.com/static/d679ff2d5ba99ce98e1f942470b4486c/866ea/picsum-4.jpg'},
                    {title: 'Nature Photo 4', image:'https://wallpapercave.com/wp/oYulxe9.jpg'},
                    {title: 'Nature Photo 5', image:'https://diabetebsl.com/wp-content/uploads/2019/09/lorem-picsum-1920-1080-3.jpg'},
                    {title: 'Nature Photo 6', image:'https://cdn.wallpapersafari.com/11/43/yub9DP.jpg'}
                ],
                flowerPhotos: [
                    {title: 'Flower Photo 1', image:'https://picsum.photos/id/152/3888/2592'},
                    {title: 'Flower Photo 2', image:'https://picsum.photos/1600/800?image=360'},
                    {title: 'Flower Photo 3', image:'https://shapeyourpath.com/code-support/images/bootstrap/rose-flower.jpg'},
                    {title: 'Flower Photo 4', image:'https://images.unsplash.com/photo-1491929007750-dce8ba76e610?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxleHBsb3JlLWZlZWR8MXx8fGVufDB8fHx8&w=1000&q=80'},
                    {title: 'Flower Photo 5', image:'https://zenmountainmonastery.secure.retreat.guru/wp-content/uploads/sites/245/2018/11/lotus-flower.jpg'},
                    {title: 'Flower Photo 6', image:'https://besthqwallpapers.com/Uploads/12-8-2020/139534/thumb2-blue-rose-bokeh-blue-flowers-beautiful-flowers-blue-buds.jpg'}
                ],
                fruitPhotos: [
                    {title: 'Fruit Photo 1', image:'https://static.vecteezy.com/system/resources/previews/000/903/067/large_2x/strawberry-berries-isolated-on-white-background-photo.jpg'},
                    {title: 'Fruit Photo 2', image:'https://images.pexels.com/photos/257840/pexels-photo-257840.jpeg?cs=srgb&dl=agriculture-apple-blur-257840.jpg&fm=jpg'},
                    {title: 'Fruit Photo 3', image:'https://media.istockphoto.com/photos/mango-on-a-white-background-picture-id186018991?k=20&m=186018991&s=612x612&w=0&h=iUmXyoajsZAEaJEk52-coOMWqrryxcH83wAo4YeI3cA='},
                    {title: 'Fruit Photo 4', image:'https://images.all-free-download.com/images/graphiclarge/orange_oranges_fruit_264991.jpg'},
                    {title: 'Fruit Photo 5', image:'https://wallpaper.dog/large/5551064.jpg'},
                    {title: 'Fruit Photo 6', image:'https://picsum.photos/seed/https:wectopertkl.com20912/500/325'}
                ],

            }
        }
    }
</script>

<style scoped>

</style>