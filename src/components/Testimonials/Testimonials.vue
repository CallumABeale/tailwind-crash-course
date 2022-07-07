<script setup>
import { ref } from 'vue'
import anishaAvatar from '../../assets/img/avatar-anisha.png'
import aliAvatar from '../../assets/img/avatar-ali.png'
import richardAvatar from '../../assets/img/avatar-richard.png'
const testimonialTitle = `What's different about Manage`
const testimonials = ref([
	{
		name: `Anisha Li`,
		avatar: anishaAvatar,
		testimonial: `Manage has supercharged our team's workflow. The ability to maintain visibility on larger milestones at all times keeps everyone motivated.`,
	},
	{
		name: `Ali Bravo`,
		avatar: aliAvatar,
		testimonial: `We have been able to cancel so many other subscriptions since using Manage. There is no more cross-channel confusion and everyone is much more focused`,
	},
	{
		name: `Richard Watts`,
		avatar: richardAvatar,
		testimonial: `Manage has supercharged our team's workflow. The ability to maintain visibility on larger milestones at all times keeps everyone motivated`,
	},
])
</script>

<template>
	<section id="testimonials">
		<div class="max-w-6xl px-5 mx-auto mt-32 text-center">
			<!-- Heading -->
			<h2 class="text-4xl font-bold text-center">
				{{ testimonialTitle }}
			</h2>
			<!-- Testimonials -->
			<div class="flex flex-col mt-24 md:flex-row md:space-x-6">
				<div
					v-for="item in testimonials"
					class="flex flex-col items-center p-6 space-y-6 rounded-lg mt-16 bg-veryLightGray md:w-1/3 md:mt-0"
				>
					<img :src="`${item.avatar}`" class="w-16 -mt-14" alt="" />
					<h5 class="text-lg font-bold">{{ item.name }}</h5>
					<p class="text-sm text-darkGrayishBlue">
						{{ item.testimonial }}
					</p>
				</div>
			</div>
			<!-- Button -->
			<div class="my-16">
				<a
					href="#"
					class="p-3 px-6 pt-2 text-white bg-brightRed rounded-full baseline hover:bg-brightRedLight"
					>Get Started</a
				>
			</div>
		</div>
	</section>
</template>
