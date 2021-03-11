<template>
  <draggable v-model="items" group="people" @start="drag=true" @end="drag=false" class="w-60">
   <div v-for="item in items" :key="item.name" class="text-left dragdiv p-2 m-2 border rounded bg-pink-500 border-pink-900 text-white font-bold"><span class="text-2xl leading-none">&#9776;</span> {{item.name}}</div>
  </draggable>
</template>

<script>
import draggable from 'vuedraggable'

export default {
  name: "DragRanking",
  components: {
    draggable
  },
  data: () => {
    return {
      items: [
        {
          name: 'Symptom',
          rank: 3
        },
        {
          name: 'Patientfördelar',
          rank: 3
        },
        {
          name: 'Prisfördelar',
          rank: 3
        },
        {
          name: 'Biverkningar',
          rank: 3
        },
        {
          name: 'Lösningar',
          rank: 3
        }
      ]

    }
  }
}
</script>

<style>
.dragdiv {
  cursor: move;
}
</style>