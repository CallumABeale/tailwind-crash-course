<script setup>
import { ref } from 'vue'
const leftTitle = `What's different about manage`
const leftContent = `Manage provides all the functionality your team needs, without the complexity. Our software is tailor-made for modern digital product teams`
const listItems = ref([
	{
		title: `Track company-wide progress`,
		content: `See how your day-today tasks fit into the wider vision. Go from tracking
				progress at the milestone level all the way down to the smallest of
				details. Never lose sight of the bigger picture again.`,
	},
	{
		title: `Advanced built-in reports`,
		content: `Set internal delivery estimates and track progress toward company goals. Our customisable dashboard helps you build out the reports you need to keep key stakeholders informed.`,
	},
	{
		title: `Everything you need in one place`,
		content: `Stop jumping from one service to another to communicate, store files, track tasks and share documents. Manage offers an all-in-one team productivity solution.`,
	},
])
</script>

<template>
	<section id="features">
		<div
			class="container flex flex-col px-4 mx-auto mt-10 space-y-12 md:space-y-0 md:flex-row"
		>
			<!-- What's different -->
			<div class="flex flex-col space-y-12 md:w-1/2">
				<h2 class="max-w-md text-4xl font-bold text-center lg:text-left">
					{{ leftTitle }}
				</h2>
				<p class="max-w-sm text-center text-darkGrayishBlue lg:text-left">
					{{ leftContent }}
				</p>
			</div>
			<!-- Numbered list -->
			<div class="flex flex-col space-y-8 md:w-1/2">
				<div
					v-for="(item, index) in listItems"
					class="flex flex-col space-y-3 md:space-y-0 md:space-x-6 md:flex-row"
				>
					<div class="rounded-l-full bg-brightRedSupLight md:bg-transparent">
						<div class="flex items-center space-x-2">
							<div
								class="px-4 py-2 text-white rounded-full md:py-1 bg-brightRed"
							>
								0{{ index + 1 }}
							</div>
							<h3 class="text-base font-bold md:mb-4 md:hidden">
								{{ item.title }}
							</h3>
						</div>
					</div>
					<div>
						<h3 class="hidden mb-4 text-lg font-bold md:block">
							{{ item.title }}
						</h3>
						<p class="text-darkGrayishBlue">
							{{ item.content }}
						</p>
					</div>
				</div>
				<!-- LI-end -->
			</div>
		</div>
	</section>
</template>
