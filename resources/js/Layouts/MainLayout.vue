<template>
    <Link href="/">Home</Link>&nbsp;
    <Link href="/show">Show</Link>

    <p>this is the timer: {{ timer }}</p>

    <slot>default</slot> 
</template>

<script setup>
import {ref} from 'vue'
  import {Link} from '@inertiajs/vue3'

  const timer = ref(0);

setInterval(() => {
    timer.value++
}, 1000)
</script>