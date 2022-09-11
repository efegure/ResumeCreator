<template>
<div class="col-span-1 bg-white rounded-xl shadow">
    <div class="flex flex-col m-6 justify-items-start" v-for="section of sections">
      <p class="text-lg mb-1 font-semibold">{{section.title}}</p>
      <p v-for="skill of section.skills" class=" grow align-middle text-base text-gray-500">{{skill}}</p>
    </div>
  </div>
</template>
<script>
  export default{
    name:"Skills",
    props:{
      sections:{
        type:Array,
        default:()=>[]
      }
    }
  }
</script>
<style></style>
