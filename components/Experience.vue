<template>
  <div class="bg-white rounded-xl py-2 px-6 shadow mt-3">
    <!-- NAME -->
    <div class="flex flex-row border-b">
      <img class="h-14 rounded-full " :src="require(`~/assets/images/${companyLogo}`)" />
      <div class="grow align-middle self-center rounded-full text-slate-400  flex-1  pl-4 ">
        <p class="font-semibold text-base text-black">
          {{ title }}
        </p>
        <div class="flex flex-row text-xs">
          <span class="mr-1 text-gray-500">{{ company }}</span>
          <span class="mr-1 text-gray-500">-</span>
          <span class="mr-1 text-gray-500">{{ location }}</span>
          <span class="mr-1 text-gray-500">-</span>
          <span class="mr-1 text-gray-500">{{ job }}</span>

        </div>
        <span class="text-xs text-gray-800">{{ date }}</span>
      </div>

    </div>
    <!-- ICONS-->
    <div class="pt-2 pb-1 border-b">
      <div class="flex flex-row" v-for="text in body.slice(0, body.length - 1)">
        <p class="text-xs">
          {{ text }}
        </p>
      </div>

    </div>
    <!-- <div class="grid grid-cols-3 pt-2 pb-1 border-b">
      <div class="flex flex-row  ">
        <img class="h-6 rounded-full mr-1 self-center" :src="likeIcon" />
        <p class="grow align-middle self-center text-sm text-gray-500">
          {{ like }}
        </p>
      </div>
      <div class="flex flex-row ">
        <img class="h-5 mr-2 self-center" :src="commentIcon" />
        <p class="grow align-middle self-center text-sm text-gray-500">
          {{ comment }}
        </p>
      </div>
      <div class="flex flex-row">
        <img class="h-6 rounded-full mr-1 self-center" :src="shareIcon" />
        <p class="grow align-middle self-center text-sm text-gray-500">
          {{ share }}
        </p>
      </div>
    </div> -->
    <div class="flex flex-row pt-2 pb-1 items-center gap-2  ">
      <p class="text-gray-500 text-xs">Tech Stack:</p>
      <p class="grow align-middle text-sm self-center rounded-full text-gray-400 bg-gray-100 flex-1 p-1 pl-4 ">
        {{ body[body.length - 1] }}
      </p>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Experience',
  props: {
    title: {
      type: String,
      default: "Title"
    },
    company: {
      type: String,
      default: "Company"
    },
    location: {
      type: String,
      default: "Location"
    },
    job: {
      type: String,
      default: "Job"
    },
    date: {
      type: String,
      default: "Date"
    },
    body: {
      type: String,
      default: "Body"
    },
    like: {
      type: String,
      default: "Like"
    },
    comment: {
      type: String,
      default: "Comment"
    },
    share: {
      type: String,
      default: "Share"
    },
    write: {
      type: String,
      default: "Write a comment..."
    },
    companyLogo: {
      type: String,
      default: () => "https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_1280.png"
    },
    profileImg: {
      type: String,
      default: () => "https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_1280.png"
    },
    likeIcon: {
      type: String,
      default: "https://kmidii.stripocdn.email/content/guids/CABINET_1154ef987a3f887ce59a7fdb008c50d6/images/59831617975283573.png"
    },
    commentIcon: {
      type: String,
      default: "https://www.seekpng.com/png/full/119-1196181_comment-comment-icon-png-gray.png"
    },
    shareIcon: {
      type: String,
      default: "https://icons-for-free.com/iconfiles/png/512/send+share+icon-1320196063551611178.png"
    },
  }
}
</script>
<style></style>
