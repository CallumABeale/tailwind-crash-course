<script setup>
import { ref } from 'vue'
const links = ref(['Pricing', 'Product', 'About Us', 'Careers', 'Community'])
</script>

<template>
	<div class="md:hidden">
		<div
			id="menu"
			class="absolute flex-col items-center hidden self-end py-8 mt-10 space-y-6 font-bold bg-white sm:w-auto sm:self-center left-6 right-6 drop-shadow-md"
		>
			<a class="hover:text-darkGrayishBlue" v-for="link in links" href="#">{{
				link
			}}</a>
		</div>
	</div>
</template>
