<script setup lang="ts">
import moment from 'moment-timezone'

const countdown = ref(calculateRemainingTime())

function calculateRemainingTime() {
  const now = moment().tz('Asia/Bangkok')
  const endOfMonth = now.clone().endOf('month')
  return endOfMonth.diff(now, 'seconds')
}

const months = computed(() => {
  return moment.duration(countdown.value, 'seconds').months()
})

const days = computed(() => {
  return moment.duration(countdown.value, 'seconds').days()
})

const hours = computed(() => {
  return moment.duration(countdown.value, 'seconds').hours()
})

const minutes = computed(() => {
  return moment.duration(countdown.value, 'seconds').minutes()
})

const seconds = computed(() => {
  return moment.duration(countdown.value, 'seconds').seconds()
})

onMounted(() => {
  const interval = setInterval(() => {
    countdown.value--
    if (countdown.value === 0) {
      clearInterval(interval)
      countdown.value = calculateRemainingTime()
    }
  }, 1000)
})
</script>

<template>
    <div class="text-black font-bold rounded-lg p-4 m-2 z-50">
        <span id="days" class="text-3xl md:text-4xl lg:text-7xl">{{ days }}</span><br />Days
    </div>
    <div class="text-black font-bold rounded-lg p-4 m-2">
        <span id="hours" class="text-3xl md:text-4xl lg:text-7xl">{{ hours }}</span><br />Hours
    </div>
    <div class="text-black font-bold rounded-lg p-4 m-2">
        <span id="minutes" class="text-3xl md:text-4xl lg:text-7xl">{{ minutes }}</span><br />Minutes
    </div>
    <div class="text-black font-bold rounded-lg p-4 m-2">
        <span id="seconds" class="text-3xl md:text-4xl lg:text-7xl">{{ seconds }}</span><br />Seconds
    </div>
</template>