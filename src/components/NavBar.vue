<template>
    <v-app-bar app color="black" dark flat class="px-12">
        <v-btn>
            <v-icon color="red" left class="mr-2">fas fa-signature</v-icon>Sergi
        </v-btn>
        <v-space></v-space>
        <v-btn text @click="scroll('home')" class="text-red ml-auto">Home</v-btn>
        <v-btn text @click="scroll('about')" >About</v-btn>
        <v-btn text @click="scroll('portfolio')" >Portofolio</v-btn>
        <v-btn text @click="scroll('services')" >Services</v-btn>
        <v-btn text @click="scroll('page')" >Page</v-btn>
        <v-btn text @click="scroll('blog')" >Blog</v-btn>
        <v-btn text @click="scroll('contact')" >Contact</v-btn>
    </v-app-bar>
</template>

<script>
export default {
    methods: {
        scroll(refName) {
            const element = document.getElementById(refName);
            element.scrollIntoView({behavior: "smooth"});
        }
    }
}
</script>

<style>

</style>