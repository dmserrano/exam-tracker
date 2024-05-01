<script setup>
import AddQuestionButton from '@/components/QuestionList/AddQuestionButton.vue'
import QuestionList from '@/components/QuestionList/QuestionList.vue'
</script>

<template>
  <div class="container my-4">
    <div class="flex justify-between">
      <div class="text-xl">All Questions</div>
      <AddQuestionButton />
    </div>

    <div>
      <QuestionList />
    </div>
  </div>
</template>
