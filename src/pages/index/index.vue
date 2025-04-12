<template>
  <view class="flex flex-col items-center justify-center min-h-screen">
    <view class="flex justify-center">
      <text class="text-2xl font-bold text-gray-800 mb-8">
        {{ title }}
      </text>
    </view>
    <view class="flex justify-center mb-4">
      <text class="text-lg font-medium text-gray-600">Material Icons</text>
    </view>
    <view class="flex items-center space-x-4 mb-8">
      <text class="material-icons text-4xl text-blue-500">favorite</text>
      <text class="material-icons text-4xl text-green-500">star</text>
      <text class="material-icons text-4xl text-red-500">thumb_up</text>
    </view>
    <view class="m-4">
      <button
        class="px-4 py-2 text-sm font-medium text-white bg-blue-500 rounded-lg hover:bg-blue-600 transition-colors"
        @click="componentClick">
        Click Me
      </button>
    </view>
  </view>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const title = ref('Hello World')

const componentClick = () => {
  title.value = 'Button Clicked!'
}
</script>

<style lang="scss" scoped>
// No need for custom styles as we're using Tailwind
</style>
