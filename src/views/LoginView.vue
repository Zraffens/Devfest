<template>
<div>
  <div class="w-full h-screen flex items-center justify-center ">
  <form class="w-full md:w-1/3 rounded-lg">
	<div class="flex font-bold justify-center mt-6">
	  <img class="h-20 w-20 mb-3" src="../assets/images/logo.png" />
	</div>
	<h2 class="text-2xl text-center text-gray-500 mb-8">Login</h2>
	<div class="px-12 pb-10">
	  <div class="w-full mb-2">
		<div class="flex items-center">
		  <input
			type="text"
			placeholder="Email Address"
			class="
			  w-full
			  border
			  rounded
			  px-3
			  py-2
			  text-gray-700
			  focus:outline-none
			"
		  />
		</div>
	  </div>
	  <div class="w-full mb-2">
		<div class="flex items-center">
		  <input
			type="password"
			placeholder="Password"
			class="
			  w-full
			  border
			  rounded
			  px-3
			  py-2
			  text-gray-700
			  focus:outline-none
			"
		  />
		</div>
	  </div>
	  <button
		type="submit"
		class="
		  w-full
		  py-2
		  mt-8
		  rounded-full
		  bg-green-500
		  text-gray-100
		  focus:outline-none
		"
	  >
		Login
	  </button>
    <a href="/signup"><p class="text-gray-400 mt-8">Register Now !!</p></a>
	</div>
  </form>
</div>
</div>
</template>

<script>
export default {
  name: "LoginView",
  scripts: {
    submit(e) {
      e.preventDefault();
    },
  },
};
</script>

<style scoped></style>
