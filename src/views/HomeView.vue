<template>
  <div>
    <div class="h-[90vh] md:flex w-5/6 mx-auto">
      <div class="left md:flex md:w-1/2">
        <div class="my-auto sm:mt-20">
          <h1
            class="font-[600] leading-[100px] text-7xl pt-6 md:text-6xl md:leading-[70px]"
          >
            Place where you can <span class="text-green-500">learn</span> and
            <span class="text-green-500">earn</span>.
          </h1>
          <p class="text-gray-400 mt-8">
            Love what you Do and Do what you Love ❤️.
          </p>
          <Search class="sm:mb-8" />
        </div>
      </div>
      <div class="right_img md:flex md:gap-4 md:mx-auto sm:hidden hidden">
        <div class="img1 flex my-auto">
          <img
            class="my-auto rounded-lg h-[17.18em] w-[15.3em]"
            src="../assets/images/img-1.jpeg"
            alt=""
          />
        </div>
        <div class="img2 flex flex-col gap-4 mt-6 md:mt-20">
          <img
            class="rounded-lg h-[12.18rem] w-[10.3rem]"
            src="../assets/images/img-2.jpeg"
            alt=""
          />
          <img
            class="rounded-lg h-[12.18rem] w-[10.3rem]"
            src="../assets/images/img-3.jpeg"
            alt=""
          />
        </div>
      </div>
    </div>
    <div id="jobs">
      <JobListing :jobs="jobs" />
    </div>
    <div id="learning">
      <Learning :skills="skills" />
    </div>
  </div>
</template>

<script>
import Search from "@/components/Search.vue";
import JobListing from "@/components/JobListing.vue";
import Learning from "@/components/Learning.vue";

export default {
  name: "HomeView",
  components: {
    Search,
    JobListing,
    Learning,
  },
  data() {
    return {
      jobs: [
        {
          id: 1,
          title: "Teacher",
          tag: "Education",
          img: "teacher",
        },

        {
          id: 2,
          title: "Software Developer",
          tag: "Tech",
          img: "software",
        },
        {
          id: 3,
          title: "Writer",
          tag: "Content",
          img: "writer",
        },
        {
          id: 4,
          title: "Assistant",
          tag: "Helper",
          img: "assistant",
        },
        {
          id: 5,
          title: "Transcripts",
          tag: "Content",
          img: "transcript",
        },
        {
          id: 6,
          title: "Health Counselor",
          tag: "Health",
          img: "counselor", 
        },
      ],
      skills: [
        {
          id: 1,
          title: 'Programming'
        },
        {
          id: 2,
          title: 'Media Developer'
        },
        {
          id: 3,
          title: 'Business'
        },
        {
          id: 4,
          title: 'Taxi Driving'
        },

      ]
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
