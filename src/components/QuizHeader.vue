<script setup>
import { defineProps } from "vue"

const { questionProgressionStatus, barProgression } = defineProps(["questionProgressionStatus", "barProgression"])
console.log(barProgression)
</script>

<template>
    <header>
        <h4> Question {{ questionProgressionStatus }}</h4>
        <div class="bar">
            <div class="completion" :style="{ width: barProgression }">

            </div>
        </div>
    </header>
</template>

<style scoped>
header {
    margin-top: 20px;

}

header h4 {
    font-size: 30px;

}

.bar {
    width: 300px;
    height: 50px;
    border: 3px solid bisque;
}

.completion {
    height: 100%;

    background-color: bisque;

}
</style>