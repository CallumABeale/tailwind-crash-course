<script setup>
const toggleBtn = () => {
	const btn = document.getElementById('menu-btn')
	const nav = document.getElementById('menu')
	btn.classList.toggle('open')
	nav.classList.toggle('flex')
	nav.classList.toggle('hidden')
}
</script>

<template>
	<button
		id="menu-btn"
		class="block hamburger md:hidden focus:outline-none"
		@click="toggleBtn"
	>
		<span class="hamburger-top"></span>
		<span class="hamburger-middle"></span>
		<span class="hamburger-bottom"></span>
	</button>
</template>
