<script setup lang="ts">
import { useToggle } from '@vueuse/core'
import 'uno.css'

const [show, toggle] = useToggle(false)
</script>

<template>
  <div class="fixed right-0 bottom-0 m-5 z-100 flex items-end font-sans select-none leading-1em">
    <div
      class="bg-white text-gray-800 rounded-lg shadow w-max h-min"
      p="x-4 y-2"
      m="y-auto r-2"
      transition="opacity duration-300"
      :class="show ? 'opacity-100' : 'opacity-0'"
    >
      <h1 class="text-lg">
        Vitesse WebExt
      </h1>
      <div>buttons</div>
      <div class="mb-4">
        <el-button>Default</el-button>
        <el-button type="primary">
          Primary
        </el-button>
        <el-button type="success">
          Success
        </el-button>
        <el-button type="info">
          Info
        </el-button>
        <el-button type="warning">
          Warning
        </el-button>
        <el-button type="danger">
          Danger
        </el-button>
      </div>
      <SharedSubtitle />
    </div>
    <button
      class="flex w-10 h-10 rounded-full shadow cursor-pointer border-none"
      bg="teal-600 hover:teal-700"
      @click="toggle()"
    >
      <pixelarticons-power class="block m-auto text-white text-lg" />
    </button>
  </div>
</template>
