<template>
  <div class="home w-5/6 mx-auto my-5">
    <div class="flex space items-center">
      <div class="flex-1">
        <h1 class="heading-text">
          Place where you can learn and place where you can earn
        </h1>
      </div>
      <div class="flex-1 images flex items-center">
        <div class="img-1">
          <div class="img">
            <img src="../assets/images/img-1.jpeg" alt="" srcset="" />
          </div>
        </div>
        <div class="img-2">
          <div class="img">
            <img src="../assets/images/img-2.jpeg" alt="" srcset="" />
          </div>
          <div class="img">
            <img src="../assets/images/img-3.jpeg" alt="" srcset="" />
          </div>
        </div>
      </div>
    </div>
    <JobListing :jobs="jobs" />
  </div>
</template>

<script>
import Search from "@/components/Search.vue";
import JobListing from "@/components/JobListing.vue";

export default {
  name: "HomeView",
  components: {
    Search,
    JobListing,
  },
  data() {
    return {
      jobs: [
        {
          id: 1,
          title: "Teacher",
          tag: "Education",
        },

        {
          id: 2,
          title: "Software Developer",
          tag: "Tech",
        },
        {
          id: 3,
          title: "Writer",
          tag: "Content",
        },
        {
          id: 4,
          title: "Assistant",
          tag: "Helper",
        },
        {
          id: 5,
          title: "Transcripts",
          tag: "Content",
        },
        {
          id: 6,
          title: "Mental Health Counselor",
          tag: "Psychology",
        },
      ],
    };
  },
};
</script>

<style>
.heading-text {
  font-size: 4.8rem;
  font-weight: 700;
}

.img {
  margin: 1rem;
}

img {
  height: 276px;
  width: 245px;
}
</style>
