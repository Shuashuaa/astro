<template>
    <div class="flex">
        <button class="border px-3 py-1 rounded-md" @click="sayHello">Say hello</button>
        <p v-show="isVisible" class="text-bold text-blue-500">{{ hello }}</p>
    </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
    setup() {
        const isVisible = ref(false);
        const hello = ref('Hello, There!');

        const sayHello = () => {
            isVisible.value = !isVisible.value;
            console.log(isVisible.value);
        }

        return { isVisible, hello, sayHello };
    },
});
</script>