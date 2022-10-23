<script setup>
defineProps(["inicio","fin","maxLength"]);

const emit = defineEmits(['next','prev'])

</script>
<template>
  <div class="btn-group" role="group" aria-label="Basic Example">
    <button type="button"  @click="$emit('prev')" class="btn btn-outline-primary"
    :disabled="inicio <= 0"
    
    >Previous {{inicio}}

    </button>
    <button type="button" @click="$emit('next')" class="btn btn-outline-primary"
    :disabled="fin >= maxLength"
    
    >Next  {{fin}}

    </button>
  </div>
</template>
