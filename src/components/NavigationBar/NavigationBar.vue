<script setup>
import Logo from './Logo.vue'
import NavLinks from './NavLinks.vue'
import GetStartedBtn from './GetStartedBtn.vue'
import MobileMenu from './MobileMenu.vue'
import Hamburger from './Hamburger.vue'
</script>

<template>
	<nav class="relative container mx-auto p-6">
		<div class="flex items-center justify-between">
			<Logo />
			<div class="hidden space-x-6 md:flex">
				<NavLinks />
			</div>
			<GetStartedBtn />
			<Hamburger />
		</div>
		<MobileMenu />
	</nav>
</template>

<script></script>
