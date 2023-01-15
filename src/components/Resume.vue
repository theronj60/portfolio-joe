<script lang="ts" setup>
import { ref } from 'vue'

let exp =  ref([
	{ name: 'Holbrook', dates: 'November - 2020', desc: ['design', 'laravel', 'vue'], current: true },
	{ name: 'Twisted Noodle', dates: '', desc: ['design', 'laravel', 'vue'], current: false },
	{ name: 'Blog', dates: '', desc: ['design', 'laravel', 'vue'], current: false },
	{ name: 'Resume', dates: '', desc: ['design', 'laravel', 'vue'], current: false },
	{ name: 'Projects', dates: '', desc: ['design', 'laravel', 'vue'], current: false },
	{ name: 'Contact', dates: '', desc: ['design', 'laravel', 'vue'], current: false },
])
</script>

<template id="resume">
	<div class="w-full flex flex-col space-y-4 pt-24 mx-4">
		<h2>Theron Joe</h2>
		<div class="flex w-full h-24 md:space-x-4">
			<div class="flex border w-full h-24">cover</div>
			<div class="flex border w-full h-24">social</div>
		</div>
		<div class="flex border">
			<div class="flex flex-col justify-self-end items-center text-gray-900">
				<div v-for="job in exp" :key="job.name">
					<div class="flex">
						<h2>{{ job.name }}</h2>
						<div>
							<li v-for="item in job.desc">{{ item }}</li>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="flex border h-24">education</div>
	</div>
</template>
