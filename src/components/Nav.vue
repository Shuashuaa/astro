<template>
    <h1>this is Nav!</h1>
    <div v-for="champs in list">
        <p>{{ champs.champion }}</p>
    </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
    setup() {
        const list = ref([
            { id: 1, champion: 'maokai'},
            { id: 2, champion: 'lee sin'},
            { id: 3, champion: 'asdasd'}
        ]);

        return { list }
    },
})
</script>
