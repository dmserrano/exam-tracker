<script setup>
import QuestionInfo from './QuestionInfo.vue'

const questions = [
  {
    id: '1234',
    questionText: 'What is a requirement of a Joint Tenants By Entirety account?',
    answers: [
      {
        id: '1234',
        answerText: 'Account owners must be spouses',
        isCorrectAnswer: true
      },
      {
        id: '1234',
        answerText: 'Account owners must be non-spouses',
        isCorrectAnswer: false
      },
      {
        id: '1234',
        answerText: 'Account owners must be unrelated',
        isCorrectAnswer: false
      },
      {
        id: '1234',
        answerText: 'Account owners must be engaged to be married',
        isCorrectAnswer: false
      }
    ],
    explanationText:
      'A tenancy by the entirety is a form of joint ownership that con only exist between a husband and wife.'
  }
]
</script>

<template>
  <div v-for="question in questions" class="my-4">
    <QuestionInfo
      :answers="question.answers"
      :question-text="question.questionText"
      :question-explanation="question.explanationText"
    />
  </div>
</template>
