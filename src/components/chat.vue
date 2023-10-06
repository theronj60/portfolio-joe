<script setup lang="ts">
import axios from 'axios'
import { computed, reactive, ref } from 'vue';

let responseT = <Object>reactive({message: null})
let question = ref()

function onSubmit() {
	// need to fix
	axios
		.post('http://api.digitalhogan.com/api/financial-assistant', { question: question.value }, {
			headers: {
				'Content-Type': 'multipart/form-data'
			}
		}
		)
		.then(response => (
			responseT.message = response.data.message
		))
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
