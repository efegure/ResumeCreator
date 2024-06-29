<template>
  <div class="bg-white rounded-xl p-3 px-6 shadow">
    <!-- NAME -->
    <div class="flex flex-row  pb-1">
      <img class="h-14 rounded-full mr-2 " :src="require(`~/assets/images/${profileImg}`)" />
      <p class="grow align-middle self-center rounded-full text-gray-500 bg-gray-100 flex-1 p-2 pl-4 ">
        {{ name }}
      </p>
    </div>
    <div>
      <p class="text-xs p-2 text-gray-500">{{ profileSummary }}</p>
    </div>
    <!-- ICONS-->
    <div class="grid grid-cols-3 pt-4">
      <div class="flex flex-row  ">
        <img class="h-7 rounded-full mr-2 self-center" :src="cityIcon" />
        <p class="text-sm grow align-middle self-center">
          {{ city }}
        </p>
      </div>
      <div class="flex flex-row ">
        <img class="h-7 rounded-full mr-2 self-center" :src="phoneIcon" />
        <p class="text-sm grow align-middle self-center">
          {{ phone }}
        </p>
      </div>
      <div class="flex flex-row">
        <img class="h-7 rounded-full mr-2 self-center" :src="emailIcon" />
        <p class="text-sm grow align-middle self-center">
          {{ email }}
        </p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'ContactInfo',
  props: {
    name: {
      type: String,
      default: "Name"
    },
    city: {
      type: String,
      default: "City"
    },
    phone: {
      type: String,
      default: "Phone"
    },
    email: {
      type: String,
      default: "Email"
    },
    profileImg: {
      type: String,
      default: () => "https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_1280.png"
    },
    cityIcon: {
      type: String,
      default: () => "https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_1280.png"
    },
    phoneIcon: {
      type: String,
      default: () => "https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_1280.png"
    },
    emailIcon: {
      type: String,
      default: () => "https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_1280.png"
    },
    profileSummary: {
      type: String,
      default: ""
    }
  }
}
</script>
<style></style>


