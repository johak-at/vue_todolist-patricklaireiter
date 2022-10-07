<script setup>
import { ref, computed} from "vue";
const nummer = ref(10);
let number_quadrat = computed(() => nummer.value * nummer.value);
</script>
<template>
    <p>
        <h1>Computed Demo</h1>
        <p>Zahl: {{ nummer }}</p>
        <p>Quadrat: {{ number_quadrat }}</p>	
    </p>
</template>