<script lang="ts" setup>
import { onMounted, nextTick, ref } from 'vue';
import Logo from '../../src/imgs/mnts.png';

let navItems =  ref([
	{ name: 'Home', link: '/', active: true },
	{ name: 'About', link: '/about', active: false },
	{ name: 'Blog', link: '/blog', active: false },
	{ name: 'Resume', link: '#resume', active: false },
	{ name: 'Projects', link: '#projects', active: false },
	{ name: 'Contact', link: '#contact', active: false },
])

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
	<nav class="flex justify-between fixed min-w-full items-center px-6 py-4 bg-gray-800 text-gray-100 opacity-75">
		<div id="logo" class="mx-4">
			<div class="border rounded-lg">
				<img id="" :src="Logo" alt="" class="w-12 h-12">
			</div>
		</div>
		<div>
			<ul class="md:flex justify-self-end items-center text-gray-100 hidden">
				<li v-for="nav in navItems" :key="nav.name" :class="['mx-2 font-black', { 'border-b-4': nav.active }]">
					<a :href="nav.link">
						{{ nav.name }}
					</a>
				</li>
			</ul>
		</div>
	</nav>
</template>
