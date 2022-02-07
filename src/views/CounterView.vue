<template>
    <h1>
        Counter View: {{ counterStore.counter }}!!!!
    </h1>

    <button @click="counterStore.incrementBy(1)">+1</button>
    <button @click="counterStore.incrementBy(2)">+2</button>
    <button @click="increaseBy(5)">+5</button>
</template>

<script lang="ts" setup>
import { useCounterStore } from '../stores/counter';

const counterStore = useCounterStore();

const increaseBy = ( value: number ) => {
    counterStore.incrementBy( value );
};

</script>