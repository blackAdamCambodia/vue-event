<script setup>
import {ref, reactive} from 'vue';
const fullImage =ref('https://media.istockphoto.com/id/979331510/photo/vivid-sunrise-on-palm-beach-florida.webp?s=170667a&w=0&k=20&c=MB2l9s2RX-48RowSjsc1jjO3qobkTxXsu_V3nynIKcU=')
const Images= [
  {
    thumb: "https://images.unsplash.com/photo-1532274402911-5a369e4c4bb5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80",
    full: "https://images.unsplash.com/photo-1532274402911-5a369e4c4bb5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80"
  },
  {
    thumb: "https://media.istockphoto.com/id/483614146/zh/%E7%85%A7%E7%89%87/child-girl-standing-in-floral-field-of-lavender.jpg?s=612x612&w=0&k=20&c=8uOrgnCLbXKgLO3Ov6_znoKmwBpH_tpC2CW3ZSMYe-E=",
    full: "https://media.istockphoto.com/id/483614146/zh/%E7%85%A7%E7%89%87/child-girl-standing-in-floral-field-of-lavender.jpg?s=612x612&w=0&k=20&c=8uOrgnCLbXKgLO3Ov6_znoKmwBpH_tpC2CW3ZSMYe-E="
  },
  {
    thumb: "https://images.unsplash.com/photo-1563718944-758794a56b34?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80",
    full: "https://images.unsplash.com/photo-1563718944-758794a56b34?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80"
  },
  {
    thumb: "https://media.istockphoto.com/id/979331510/photo/vivid-sunrise-on-palm-beach-florida.webp?s=170667a&w=0&k=20&c=MB2l9s2RX-48RowSjsc1jjO3qobkTxXsu_V3nynIKcU=",
    full: "https://media.istockphoto.com/id/979331510/photo/vivid-sunrise-on-palm-beach-florida.webp?s=170667a&w=0&k=20&c=MB2l9s2RX-48RowSjsc1jjO3qobkTxXsu_V3nynIKcU="
  }
]

function setImage(image) {
  fullImage.value = image.full
}
</script>

<template>
   <section class="container mx-auto flex items-center flex-col">
        <h1 class="text-center text-2xl py-10">Events & Reactivity</h1>
        <div class="">
            <div  class="flex space-x-2">
                <img @click="setImage(image)"  class="cursor-pointer thumb" :src="image.thumb" alt="" v-for="image in  Images" :key="image.thumb">                
            </div>
            <div class="mt-10">
                <img class="cursor-pointer fullImage w-full" :src="fullImage" alt="">
            </div>
        </div>
    </section>
</template>

<style scoped>
.thumb {
  width:300px;
  height: 250px;
}
.fullImage {
  width: 100%;
  height:800px;
}
</style>
