<script setup lang="ts">
import Accordion from './components/Accordion.vue'

</script>

<template  >
    <div class="p-8 mx-8 bg-white rounded-xl max-w-96 md:max-w-screen-sm bg">
        <div class="flex gap-4 mb-8">
            <img src="/src/assets/images/icon-star.svg" class="inline">
            <h1 class="inline">FAQs</h1>
        </div>
        <ul>
            <Accordion>
                <template #title>
                    What is Frontend Mentor, and how will it help me?
                </template>
                Frontend Mentor offers realistic coding challenges to help developers improve their
                frontend coding skills with projects in HTML, CSS, and JavaScript. It's suitable for
                all levels and ideal for portfolio building.
            </Accordion>
            <Accordion>
                <template #title>
                    Is Frontend Mentor free?
                </template>
                Yes, Frontend Mentor offers both free and premium coding challenges, with the free
                option providing access to a range of projects suitable for all skill levels.
            </Accordion>

            <Accordion>
                <template #title>
                    Can I use Frontend Mentor projects in my portfolio?
                </template>
                Yes, you can use projects completed on Frontend Mentor in your portfolio. It's an excellent
                way to showcase your skills to potential employers!
            </Accordion>


            <Accordion>
                <template #title>
                    How can I get help if I'm stuck on a Frontend Mentor challenge?
                </template>
                The best place to get help is inside Frontend Mentor's Discord community. There's a help
                channel where you can ask questions and seek support from other community members.
            </Accordion>
        </ul>
    </div>
</template>

<style scoped>

</style>
