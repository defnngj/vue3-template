<script lang="ts" setup>
import { reactive } from 'vue'

// do not use same name with ref

import { ref } from 'vue'

const number = ref(1)

const data = reactive({
  input:1
})

const onSubmit = () => {
  number.value ++
  data.input ++
  console.log('submit!', number.value, data.input)
}

</script>

<template>
  <div class="about">
    <div>
      <h1>This is an about page! {{ number }}</h1>
    </div>
    <div>
      <!-- <el-input v-model="data.input" /> -->
      <el-button type="primary" @click="onSubmit"> + 1</el-button>
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
