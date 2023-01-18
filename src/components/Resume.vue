<script lang="ts" setup>
// import { ref } from 'vue'
import Image from '../imgs/monument-day.jpeg';

const bgImg = `background-image: url(${Image}); background-size: cover;`

</script>

<template id="resume">
	<section class="min-h-screen w-full flex justify-center pt-24 pb-4" :style=bgImg>
		<div class="w-[800px] border rounded p-4 bg-gray-200">
			<div class="border border-black flex flex-col items-center w-full h-24">
				<h2 class="flex text-3xl font-semibold">Theron Joe</h2>
				<span class="font-semibold">Web Developer</span>
				<div class="flex w-full space-x-8 justify-center items-center border border-red-600 h-24">
					<a href="mailto:theronj@joetwebdev.io" class="hover:font-semibold">theronj@joetwebdev.io</a>
					<a href="https://twitter.com/joeT_60" target="_blank" class="hover:font-semibold">Twitter</a>
					<a href="https://github.com/theronj60" target="_blank" class="hover:font-semibold">Github</a>
					<a href="https://joetwebdev.io/" target="_blank" class="hover:font-semibold">joetwebdev.io</a>
				</div>
			</div>
			<div class="flex justify-between mt-4">
				<div class="flex flex-col border border-blue-500 w-2/3 space-y-4 text-gray-900">
					<h3 class="text-2xl text-cyan-600 font-semibold border-b -mb-2 border-black">Revelant Experience</h3>
					<div>
						<h4 class="text-base text-gray-600"><span class="text-gray-900 font-semibold">Web Developer</span> at Holbrook Asphalt</h4>
						<span class="text-sm">Nov 2020 - Dec 2022 <span class="text-base">||</span> St George, Utah</span>
						<ul class="list-inside list-disc">
							<li>Write modern, performant, and robust code for a saas project</li>
						</ul>
					</div>
					<div>
						<h4 class="text-base text-gray-600"><span class="text-gray-900 font-semibold">Front-End Developer</span> at Big Click Media</h4>
						<span class="text-sm">March 2020 - May 2020 <span class="text-base">||</span> Remote</span>
						<ul class="list-inside list-disc">
							<li>Writing Vue code</li>
						</ul>
					</div>
					<div>
						<h4 class="text-base text-gray-600"><span class="text-gray-900 font-semibold">Front-End Developer</span> at Spacelander.io</h4>
						<span class="text-sm">Oct 2019 <span class="text-base">||</span> St George, Utah</span>
						<ul class="list-inside list-disc">
							<li>Vuetify</li>
						</ul>
					</div>
					<div>
						<h4 class="text-base text-gray-600"><span class="text-gray-900 font-semibold">Front-End Developer</span> at Oracle Learning Center</h4>
						<span class="text-sm">Jan 2019 - Jan 2020 <span class="text-base">||</span> St George, Utah</span>
						<ul class="list-inside list-disc">
							<li>Vuetify</li>
						</ul>
					</div>
				</div>
				<div class="border border-red-500 flex flex-col space-y-4 w-1/3 text-gray-900 text-sm">
					<h3 class="text-2xl font-semibold -mb-2">Skills</h3>
					<div>
						<p class="font-semibold">Programing Languages</p>
						<p>Javascript, PHP, Go, Python</p>
					</div>
					<div>
						<p class="font-semibold">Libraries/Frameworks</p>
						<p>Laravel, Vue, NuxtJs, Vuetify, NextJs, React, Tailwindcss</p>
					</div>
					<div>
						<p class="font-semibold">Tools & Platforms</p>
						<p>Git, Vite, Webpack, Docker</p>
					</div>
					<div>
						<p class="font-semibold">Design</p>
						<p>Figma, Affinity Designer, Adobe XD</p>
					</div>
					<h3 class="text-2xl font-semibold">Education</h3>
					<h3 class="text-2xl font-semibold">Projects</h3>
					<h3 class="text-2xl font-semibold">Hobbies</h3>
				</div>
			</div>
			<div class="flex border h-24">education</div>
		</div>
	</section>
</template>
