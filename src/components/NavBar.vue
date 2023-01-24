<script lang="ts" setup>
import { onMounted, nextTick, ref } from 'vue';
import Logo from '../../src/imgs/mnts.png';

let navItems =  ref([
	{ name: 'Home', link: '/', active: true },
	{ name: 'About', link: '/about', active: false },
	{ name: 'Blog', link: '/blog', active: false },
	{ name: 'Resume', link: '/resume', active: false },
	{ name: 'Projects', link: '#projects', active: false },
	{ name: 'Contact', link: '#contact', active: false },
])

let mobileNav = false

onMounted(() => {
	nextTick(() => {
		setNav()
	})
})

 async function setNav() {
	navItems.value.forEach((nav) => {
		if (window.location.pathname == nav.link) {
			nav.active = true
		} else {
			nav.active = false
		}
	})
}
</script>

<template id="nav-bar">
	<nav class="flex justify-between min-w-full items-center px-6 py-4 bg-gray-800 text-gray-100">
		<div id="logo" class="mx-4">
			<div class="border rounded-lg">
				<img id="" :src="Logo" alt="" class="w-12 h-12">
			</div>
			
		</div>
		<div class="flex md:hidden">
				X
		</div>
		<div class="md:flex hidden">
			<ul class="md:flex justify-self-end items-center text-gray-100 hidden">
				<li v-for="nav in navItems" :key="nav.name" :class="['mx-2 font-black', { 'border-b-4': nav.active }]">
					<a :href="nav.link">
						{{ nav.name }}
					</a>
				</li>
			</ul>
		</div>
	</nav>
	<div class="w-full bg-gray-800 fixed">
		<ul>
			<li v-for="nav in navItems" :key="nav.name" :class="['mx-2 text-center text-gray-100 font-black', { 'bg-gray-600': nav.active }]">
				<a :href="nav.link" class="w-full text-center">
					{{ nav.name }}
				</a>
			</li>
		</ul>
	</div>
</template>
