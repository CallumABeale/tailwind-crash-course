<script setup>
const navLinks = ['Pricing', 'Product', 'About', 'Careers', 'Community']
</script>

<template>
	<a v-for="link in navLinks" href="#" class="hover:text-darkGrayishBlue">{{
		link
	}}</a>
</template>

<script></script>
