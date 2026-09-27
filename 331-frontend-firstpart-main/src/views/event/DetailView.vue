<script setup lang="ts">
import { toRefs } from 'vue';
import type { Event } from '@/types.ts';

const props = defineProps<{
    event: Event
    id?: string | number
}>()

const { event } = toRefs(props)
</script>

<template>
    <div>
        <p>{{ event.time }} @ {{ event.location }}</p>
        <p>{{ event.description }}</p>
    </div>
</template>