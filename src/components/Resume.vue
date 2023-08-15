<script lang="ts" setup>
// import { ref } from 'vue'

</script>

<template id="resume">
	<div class="lg:w-[900px] w-full border rounded py-4 px-8 mx-4 lg:mx-0 bg-gray-200">
		<div class="flex flex-col items-center w-full md:h-24">
			<h2 class="flex text-3xl text-cyan-600 font-semibold">Theron Joe</h2>
			<span class="font-semibold">Full Stack Developer</span>
			<div class="flex flex-col md:flex-row w-full md:space-x-8 justify-center items-center h-24">
				<a href="mailto:theronj@joetwebdev.io" class="hover:font-semibold hover:text-cyan-600">theronj@joetwebdev.io</a>
				<a href="https://twitter.com/joeT_60" target="_blank" class="hover:font-semibold hover:text-cyan-600">Twitter</a>
				<a href="https://github.com/theronj60" target="_blank" class="hover:font-semibold hover:text-cyan-600">Github</a>
				<!-- <a href="https://joetwebdev.io/" target="_blank" class="hover:font-semibold hover:text-cyan-600">joetwebdev.io</a> -->
			</div>
		</div>
		<div class="flex-col md:flex-row flex justify-center md:space-x-4 mt-4">
			<div class="flex flex-col md:w-2/3 space-y-4 text-gray-900">
				<h3 class="text-2xl text-cyan-600 font-semibold -mb-2">Revelant Experience</h3>
				<div>
					<h4 class="text-base text-gray-600"><span class="text-gray-900 font-semibold">Full Stack Developer</span> at Pro Market Consulting LLC</h4>
					<span class="text-sm">March 2023 - Current <span class="text-base">||</span> St George, Utah</span>
					<ul class="list-inside list-disc">
						<li>Experience with Hubspot API and Stripe</li>
						<li>Manage DNS and provide maintenance for several websites, ensuring optimal performance and uptime.</li>
						<li>Update and maintain project code through Laravel framework.</li>
						<li>Manage servers and databases through DigitalOcean and Laravel Forge, ensuring reliable and efficient server performance.</li>
					</ul>
				</div>
				<div>
					<h4 class="text-base text-gray-600"><span class="text-gray-900 font-semibold">Web Developer</span> at Holbrook Asphalt</h4>
					<span class="text-sm">Nov 2020 - Dec 2022 <span class="text-base">||</span> St George, Utah</span>
					<ul class="list-inside list-disc">
						<li>Wrote modern, performant, and robust code for a saas project</li>
						<li>Managed multiple tasks and authored code for the project</li>
						<li>Managed multiple tasks and authored code for the project</li>
						<li>Utilized Mysql and Docker for local development</li>
					</ul>
				</div>
				<div>
					<h4 class="text-base text-gray-600"><span class="text-gray-900 font-semibold">Front-End Developer</span> at Big Click Media</h4>
					<span class="text-sm">March 2020 - May 2020 <span class="text-base">||</span> Remote</span>
					<ul class="list-inside list-disc">
						<li>Refactored existing code and replaced it with Vuetify</li>
						<li>Building the UI for tables, lists, tabs for an admin dashboard</li>
						<li>Organized code structure for new framework</li>
					</ul>
				</div>
				<div>
					<h4 class="text-base text-gray-600"><span class="text-gray-900 font-semibold">Front-End Developer</span> at Spacelander.io</h4>
					<span class="text-sm">Oct 2019 <span class="text-base">||</span> St George, Utah</span>
					<ul class="list-inside list-disc">
						<li>Enabled the use of task management (teamwork.com), and guided team on software use.</li>
						<li>Reorganized tables and card containers using VueJS</li>
						<li>Improved UI by implenting Vuetify Framework</li>
						<li>Version control (github)</li>
					</ul>
				</div>
				<div>
					<h4 class="text-base text-gray-600"><span class="text-gray-900 font-semibold">Front-End Developer</span> at Oracle Learning Center</h4>
					<span class="text-sm">Jan 2019 - Jan 2020 <span class="text-base">||</span> St George, Utah</span>
					<ul class="list-inside list-disc">
						<li>Organized and developed code and improving the UI</li>
						<li>Use Version control with projects (gitlab)</li>
						<li>Coded with Laravel and vue</li>
					</ul>
				</div>
			</div>
			<div class="flex flex-col space-y-2 md:w-1/3 text-gray-900 text-sm">
				<h3 class="text-2xl text-cyan-600 font-semibold -mb-2">Skills</h3>
				<div>
					<p class="font-semibold">Programing Languages</p>
					<p>Javascript, PHP, Go, Python</p>
				</div>
				<div>
					<p class="font-semibold">Libraries/Frameworks</p>
					<p>Laravel, Vue, NuxtJs, Vuetify, AstroJs, NextJs, React, Tailwindcss</p>
				</div>
				<div>
					<p class="font-semibold">Tools & Platforms</p>
					<p>Git, Vite, Webpack, Docker, Stripe, Hubspot</p>
				</div>
				<div>
					<p class="font-semibold">Task Management</p>
					<p>Asana, Trello, Jira</p>
				</div>
				<div>
					<p class="font-semibold">Design</p>
					<p>Figma, Affinity Designer, Adobe XD</p>
				</div>
				<h3 class="text-2xl text-cyan-600 font-semibold">Education</h3>
				<div>
					<p class="font-semibold">Skillcrush </p>
					<span class="text-gray-600 font-normal">Front-end Developer Blueprint || 2018 - 2019</span>
					<ul class="list-item">
						<li class="">Git, Html, CSS, Javascript</li>
					</ul>
				</div>
				<div>
					<p class="font-semibold">Southern Utah University</p>
					<span class="text-gray-600 font-normal">General Studies || 2010 - 2011</span>
				</div>
				<h3 class="text-2xl text-cyan-600 font-semibold">Projects</h3>
				<div>
					<a href="https://github.com/theronj60/im-bored" target="_blank" class="font-semibold hover:text-cyan-600">im-bored</a>
					<p>go, tui project, consumed bored api</p>
				</div>
				<div>
					<a href="https://github.com/theronj60/portfolio-joe" target="_blank" class="font-semibold hover:text-cyan-600">Portfolio</a>
					<p>Built with astroJs and Vue</p>
				</div>
				<div>
					<a href="https://github.com/theronj60" target="_blank" class="font-semibold hover:text-cyan-600">Github</a>
					<p>My github Profile</p>
				</div>
				<h3 class="text-2xl text-cyan-600 font-semibold">Hobbies</h3>
				<div>
					<p>Reading, Cooking, Welding</p>
				</div>
			</div>
		</div>
	</div>
</template>
