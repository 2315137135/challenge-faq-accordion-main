<template>
    <li class="flex flex-col py-6 ">
        <div class="relative font-bold text-md hover:text-purple-600">
            <!-- title -->
            <button @click="toogleOpen">
                <div class="pr-16 text-left">
                    <slot name="title"></slot>
                </div>
                <img class="absolute top-0 bottom-0 right-0 my-auto" :src="butonImg" />
            </button>
        </div>
        <div class="pr-8 overflow-hidden transition-all duration-300 max-h-0 text-neutral-500" :class="{ 'open': isOpen }">
            <!-- content -->
            <br>
            <slot></slot>
        </div>

    </li>
</template>

<script setup lang="ts">
import { computed, ref } from 'vue'
import minus from "@/assets/images/icon-minus.svg"
import plus from "@/assets/images/icon-plus.svg"

let isOpen = ref(false)

let butonImg = computed(() => {
    return isOpen.value ? minus : plus
})

let toogleOpen = () => {
    isOpen.value = !isOpen.value
}

</script>

<style scoped>
.open {
    max-height: 6rem;
}



li {
    @apply border-t border-gray-100
}

li:first-child {
    @apply border-opacity-0
}
</style>