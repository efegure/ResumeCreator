<template>
<div class="bg-white rounded-xl shadow pt-3">
    <div class="flex flex-col mx-6 mt-3 justify-items-start" v-for="(section,$index) of sections">
      <p class="text-lg mb-1 font-semibold">{{section.title}}</p>
      <p v-for="(skill,$i) of section.skills" class="grow align-middle text-base text-gray-500 pb-1" :class="{'mb-3':$i+1=== section.skills.length}">{{skill}}</p>
      <div class="border-b flex" v-if="$index+1!== sections.length"></div>
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
