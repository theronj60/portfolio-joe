<script lang="ts" setup>
import { onMounted, nextTick, ref } from 'vue';
import Logo from '../../src/imgs/mnts.png';

let navItems =  ref([
	{ name: 'Home', link: '/', active: true },
	{ name: 'About', link: '/about', active: false },
	// { name: 'Blog', link: '/blog', active: false },
	{ name: 'Resume', link: '/resume', active: false },
	{ name: 'Projects', link: '/projects', active: false },
	//{ name: 'Contact', link: '#contact', active: false },
])

let mobileNav = ref(false)

onMounted(() => {
	nextTick(() => {
		setNav()
	})
})

function toggleNav() {
	mobileNav.value = !mobileNav.value
}

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
			<button type="button" @click="toggleNav" class="text-white">
				<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-9 h-9">
				  <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
				</svg>
			</button>
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
	<div v-if="mobileNav" class="w-full bg-gray-800 fixed top-22">
		<ul>
			<li v-for="nav in navItems" :key="nav.name" :class="['flex text-center text-gray-100 font-black', { 'bg-gray-600': nav.active }]">
				<a :href="nav.link" class="w-full text-center py-4">
					{{ nav.name }}
				</a>
			</li>
		</ul>
	</div>
</template>
