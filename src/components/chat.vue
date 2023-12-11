<script setup lang="ts">
import { computed, reactive, ref } from 'vue';

let responseT = <Object>reactive({ message: null })
let question = ref()

async function onSubmit() {
	// gpt response
	const formData = new FormData();
	formData.append('question', question.value);

	await fetch('http://127.0.0.1:8885/api/financial-assistant', {
		method: 'POST',
		// headers: {
		// 	'Content-Type': 'application/x-www-form-urlencoded'
		// },
		body: formData
		// { question: question.value }
	})
		.then(response => {
			if (!response.ok) {
				throw new Error('Network response was not ok');
			}
			return response.json(); // Parsing the JSON response
		})
		.then(data => {
			responseT.message = data.message;
		})
		.catch(error => {
			console.error('There was a problem with your fetch operation:', error);
		});
}

const responseMessage = computed(() => {
	return responseT.message
})
</script>

<template>
	<div class="flex flex-col space-y-4">
		<p>Response:</p>
		<!-- <label for="response">Response:</label> -->
		<p for="test" class="" v-if="responseT" v-html="responseMessage"></p>
		<form action="" @submit.prevent="onSubmit" class="flex flex-col space-y-4">
			<input v-model="question" id="chat-question" class="p-2 border border-black rounded-lg" placeholder="Ask away" />
			<button type="submit" class="bg-green-500 text-white mx-auto px-6 py-2 rounded-lg">Enter</button>
		</form>
	</div>
</template>
