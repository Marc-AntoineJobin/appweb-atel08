<script setup lang="ts">
import { ref } from "vue"
const periods = ["Aujourd'hui", "Cette semaine", "Ce mois"]

let selectedPeriod = ref("Aujourd'hui")

function selectPeriod(period: string) {
console.log(period)
selectedPeriod.value = period
}
</script>


<template>
    <nav>
        <span>
            <a href="#" v-for="period of periods" v-bind:key="period" v-on:click="selectPeriod(period)" v-bind:class="{ 'bg-primary': period === selectedPeriod}">
                {{ period }}
            </a>
        </span>
    </nav>
    {{ selectedPeriod }}
</template>


<style>

</style>