<script setup>
import { ref } from 'vue'
import logo from '../../assets/img/logo-white.svg'
import fbIcon from '../../assets/img/icon-facebook.svg'
import ytIcon from '../../assets/img/icon-youtube.svg'
import twitterIcon from '../../assets/img/icon-twitter.svg'
import pinterestIcon from '../../assets/img/icon-pinterest.svg'
import instaIcon from '../../assets/img/icon-instagram.svg'
const socialsLinks = ref([
	{ img: fbIcon },
	{ img: ytIcon },
	{ img: twitterIcon },
	{ img: pinterestIcon },
	{ img: instaIcon },
])
const linksListLeft = ref(['Home', 'Pricing', 'Products', 'About'])
const linksListRight = ref(['Careers', 'Community', 'Privacy Policy'])
</script>

<template>
	<footer class="bg-veryDarkBlue">
		<!-- Flex container -->
		<div
			class="container flex flex-col-reverse justify-between px-6 py-10 mx-auto space-y-8 md:flex-row md:space-y-0"
		>
			<!-- Logo and social links container -->
			<div
				class="flex flex-col-reverse items-center justify-between space-y-12 md:flex-col md:space-y-0 md:items-start"
			>
				<div class="mx-auto my-6 text-center text-white md:hidden">
					Copyright &copy; 2022, All Rights Reserved
				</div>
				<!-- Logo -->
				<div>
					<img :src="`${logo}`" class="h-8" alt="" />
				</div>
				<!-- Social Links Container -->
				<div class="flex justify-center space-x-4">
					<!-- Links -->
					<a v-for="link in socialsLinks" href="#">
						<img :src="`${link.img}`" alt="" class="h-8" />
					</a>
				</div>
			</div>
			<!-- List Container -->
			<div class="flex justify-around space-x-32">
				<div class="flex flex-col space-y-3 text-white">
					<a
						v-for="link in linksListLeft"
						href="#"
						class="hover:text-brightRed"
						>{{ link }}</a
					>
				</div>
				<div class="flex flex-col space-y-3 text-white">
					<a
						v-for="link in linksListRight"
						href="#"
						class="hover:text-brightRed"
						>{{ link }}</a
					>
				</div>
			</div>
			<!-- Input Container -->
			<div class="flex flex-col justify-between">
				<form>
					<div class="flex space-x-3">
						<input
							type="text"
							class="flex-1 px-4 rounded-full focus:outline-none"
							placeholder="Updated in your inbox"
						/>
						<button
							class="px-6 py-2 text-white rounded-full bg-brightRed hover:bg-brightRedLight focus:outline-none"
						>
							Go
						</button>
					</div>
				</form>
				<div class="hidden text-white md:block">
					Copyright &copy; 2022, All Rights Reserved
				</div>
			</div>
		</div>
	</footer>
</template>
