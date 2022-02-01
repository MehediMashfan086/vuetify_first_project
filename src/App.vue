<template>
  <v-app>
    <Header></Header>

    <v-main>

    </v-main>
  </v-app>
</template>

<script>

import Header from "./components/Header"
export default {
  name: 'App',
  components: {Header},
  data() {
            return {
                menus: [
                    {title:'Home',      route:'home'},
                    {title:'About Us',  route:'about-us'},
                    {title:'Protfolio', route:'protfolio'},
                    {title:'Project',   route:'project'},
                    {title:'Gallery',   route:'gallery'},
                    {title:'Contact',   route:'contact'},
      ]
    }
  }
};
</script>
