<template>
  <div class="pb-2">
    <span class="inline-block w-40">
      {{ name }}
    </span>
    <input type="range" min="1" max="5" v-model="rank" class="rounded-lg overflow-hidden appearance-none bg-gray-400 h-3 w-128 mr-4" />
      {{ rankEmoji }}
  </div>
</template>

<script>
export default {
  name: "Slider",
  props: [
    "name",
    "rank"
  ],
  computed: {
    rankEmoji: function() {
      switch (this.rank) {
        case 1:
          return '🥱'
        case 2:
          return '😒'      
        case 3:
          return '🙂'      
        case 4:
          return '😀'      
        case 5:
          return '😍'      
        default:
          return '🙂';
      }
    }
  }
}
</script>

<style>

</style>