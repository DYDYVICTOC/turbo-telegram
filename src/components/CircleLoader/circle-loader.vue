<script setup>
import CircleLoaderStyle from "~/components/CircleLoader/circle-loader.module.css";

defineProps({
  borderSize: {
    type: Number,
    required: false,
    default: 4
  },
  width: {
    type: Number,
    required: false,
    default: 30
  },
  height: {
    type: Number,
    required: false,
    default: 30
  },
  lineColor: {
    type: String,
    required: false,
    default: 'rgba(255, 255, 255, .15)'
  },
  fullColor: {
    type: String,
    required: false,
    default: 'rgba(255, 255, 255, .08)'
  },
})
</script>

<template>
  <div
      :class="{ [CircleLoaderStyle['loader']]: true }"
      :style="{
        '--circle-loader-border-size': borderSize + 'px',
        '--circle-loader-border-line-color': lineColor,
        '--circle-loader-border-full-color': fullColor,
        width: width + 'px',
        height: height + 'px'
  }"></div>
</template>