<template>
    <v-bottom-sheet v-model="sheet">
      <template v-slot:activator="{ props }">
        <div class="text-center">
          <v-btn v-bind="props" color="#fb7e7e" size="x-large" text="Click Me"></v-btn>
        </div>
      </template>
  
      <v-list>
        <v-list-subheader>Open in</v-list-subheader>
  
        <v-list-item v-for="tile in tiles" :key="tile.title" :prepend-avatar="`/img/${tile.img}`" :title="tile.title" @click="openLink(tile.link)"></v-list-item>
      </v-list>
    </v-bottom-sheet>
  </template>

<script>
    export default {
        data: () => ({
            sheet: false,
            tiles: [{
                img: 'github.png',
                title: 'GitHub',
                link: 'https://github.com/Huguete18',
            }, {
                img: 'linkedin.png',
                title: 'LinKedin',
                link: 'https://www.linkedin.com/in/sergi-huguet-986b3071/',
            }, {
                img: 'protonmail.png',
                title: 'ProtonMail',
                link: 'mailto:serhuguet@protonmail.com',
                email: 'serhuguet@protonmail.com',
            }, {
                img: 'instagram.png',
                title: 'Instagram',
                link: 'https://www.instagram.com/huguete_18/',
            }, {
                img: 'whatsapp.png',
                title: 'WhatsApp',
                link: 'https://wa.me/34693783999',
            }, ],
        }),
        methods: {
            openLink(link) {
            window.open(link, '_blank');
            this.sheet = false;
            },
        },
    }
</script>

<style>
</style>