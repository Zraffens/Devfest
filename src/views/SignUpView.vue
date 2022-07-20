<template>
  <div>
  <div class="w-full h-screen flex items-center justify-center ">
  <form class="w-full md:w-1/3 rounded-lg mt-5">
	<div class="flex font-bold justify-center mt-6">
	  <img class="h-20 w-20 mb-3" src="../assets/images/logo.png" />
	</div>
	<h2 class="text-2xl text-center text-gray-500 mb-8">Register</h2>
	<div class="px-12 pb-10">
	  <div class="w-full mb-2">
		<div class="flex items-center">
		  <input
			type="text"
			placeholder="Name"
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
		Register
	  </button>
    <a href="/login"><p class="text-gray-400 mt-8">Already Registered ?? </p></a>
	</div>
  </form>
</div>
</div>
</template>

<script>
export default {
  name: "SignUpView",
  data() {
    return {
      password: "",
      confirm: "",
    };
  },
  methods: {
    submit(e) {
      e.preventDefault();
    },
    checkPass() {
      if (this.password.length < 6) {
        const err = document.getElementById("error");
        err.innerHTML = "Password should be more than 6 characters";
      }
    },
    verifyPass() {
      if (this.passsword != this.confirm) {
        err.innerHTML = "The Passwords don't match";
      }
    },
  },
};
</script>

<style scoped></style>
