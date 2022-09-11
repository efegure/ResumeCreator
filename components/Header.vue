<template>
  <div class="grid grid-cols-2 bg-white rounded-t-xl items-center p-1 px-9 shadow">
    <!-- NAME -->
    <div class="flex flex-row ">
      <img class="h-12 rounded-full mr-2 "
        :src="logo" />
      <p class="align-middle self-center rounded-full text-gray-500 text-slate-400 bg-gray-100 p-2 pl-4 w-56">
        {{jobTitle}}
      </p>
    </div>
    <!-- ICONS-->
    <div class="grid grid-cols-3">
      <div class="flex flex-row rounded-full bg-blue-50 p-1 px-2 ">
        <img class="h-9 rounded-full mr-2 self-center"
        :src="profileImg" />
        <p class="tracking-normal align-middle self-center text-blue-600">
        {{name}}
        </p>
      </div>
      <div class="flex justify-center items-center space-x-2">
        <a href="https://github.com/efegure" target="_blank"><svg
            class="w-6 h-6 text-gray-600 hover:text-gray-800 button--github" xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="32" height="32"
            preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24">
            <path
              d="M12 2.247a10 10 0 0 0-3.162 19.487c.5.088.687-.212.687-.475c0-.237-.012-1.025-.012-1.862c-2.513.462-3.163-.613-3.363-1.175a3.636 3.636 0 0 0-1.025-1.413c-.35-.187-.85-.65-.013-.662a2.001 2.001 0 0 1 1.538 1.025a2.137 2.137 0 0 0 2.912.825a2.104 2.104 0 0 1 .638-1.338c-2.225-.25-4.55-1.112-4.55-4.937a3.892 3.892 0 0 1 1.025-2.688a3.594 3.594 0 0 1 .1-2.65s.837-.262 2.75 1.025a9.427 9.427 0 0 1 5 0c1.912-1.3 2.75-1.025 2.75-1.025a3.593 3.593 0 0 1 .1 2.65a3.869 3.869 0 0 1 1.025 2.688c0 3.837-2.338 4.687-4.563 4.937a2.368 2.368 0 0 1 .675 1.85c0 1.338-.012 2.413-.012 2.75c0 .263.187.575.687.475A10.005 10.005 0 0 0 12 2.247z"
              fill="currentColor" />
          </svg></a>
      </div>

      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'NameCard',
  props:{
    name:{
      type:String,
      default: "Name"
    },
    jobTitle:{
      type:String,
      default: "Name"
    },
    logo:{
      type:String,
      default:()=> "https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_1280.png"
    },
    profileImg:{
      type:String,
      default:()=> "https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_1280.png"
    },
    gitLink: {
      type:String,
      default :""
    }
  }
}

</script>
<style>
</style>


