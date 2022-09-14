<script lang="ts" setup>
import Logo from '../../../imgs/mnts.png';
</script>

<template id="nav-bar">
	<nav class="flex justify-between items-center mx-8 py-4 border bg-gray-300">
		<div id="logo" class="mx-4">
			<div class="border rounded-lg">
				<img id="" :src="Logo" alt="" class="w-8 h-8">
			</div>
		</div>
		<div>
			<ul class="flex space-x-4">
				<li>
					<a href="/" class="hover:bg-gray-400 hover:text-white rounded px-4 py-2">Home</a>
				</li>
				<li>
					<a href="" class="hover:bg-gray-400 hover:text-white rounded px-4 py-2">About</a>
				</li>
				<li>
					<a href="/blog" class="hover:bg-gray-400 hover:text-white rounded px-4 py-2">Blog</a>
				</li>
				<li>
					<a href="" class="hover:bg-gray-400 hover:text-white rounded px-4 py-2">Projects</a>
				</li>
				<li>
					<a href="" class="hover:bg-gray-400 hover:text-white rounded px-4 py-2">Contact</a>
				</li>
			</ul>
		</div>
	</nav>
</template>
