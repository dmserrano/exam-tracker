<script setup>
import { ref } from 'vue'

defineProps(['questionExplanation', 'questionText', 'answers'])

const showAnswer = ref(false)

const toggleShowAnswer = (shouldShowAnswer) => {
  showAnswer.value = shouldShowAnswer
}

const isAnswerCorrect = ({ isCorrectAnswer }) => {
  return isCorrectAnswer && showAnswer.value
}

const correctAnswerClass = (answer) => {
  return isAnswerCorrect(answer) ? 'text-green-600' : ''
}
</script>

<template>
  <div class="bg-gray-100 border-t border-b border-gray-500 text-white-700 px-4 py-3" role="alert">
    <span class="font-bold">{{ questionText }}</span>

    <div class="grid grid-cols-2">
      <span :class="`my-2 text-sm ${correctAnswerClass(answer)}`" v-for="answer in answers">
        {{ answer.answerText }}
      </span>
    </div>

    <div v-if="showAnswer" class="mb-2">
      <span class="font-medium">Explanation: {{ questionExplanation }}</span>
    </div>

    <div>
      <span
        class="text-xs hover:underline hover:text-blue-500 hover:cursor-pointer"
        @click="toggleShowAnswer(!showAnswer)"
      >
        {{ showAnswer ? 'Hide Answer' : 'Click for answer' }}
      </span>
    </div>
  </div>
</template>
