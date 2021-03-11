<template>
  <div class="text-left mx-auto">
    
  <div v-for="item of items" :key="item.name">
    <span class="inline-block w-40">{{item.name}}</span>
    <input :id="item.name" :name="item.name" type="range" max="5" min="1" v-model.number="item.rank" class="rounded-lg overflow-hidden appearance-none bg-pink-200 h-3 w-128 mr-4"/>
    <span class="text-2xl">{{ rankEmoji(item.rank) }}</span>
  </div>
  </div>
</template>

<script>
export default {
  name: 'SliderRanking',
  data: function () {
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
  },
  methods: {
    rankEmoji (foo) {
      switch (foo) {
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
input[type=range]::-webkit-slider-thumb {
    width: 14px;
    -webkit-appearance: none;
    appearance: none;
    height: 12px;
    cursor: ew-resize;
    background: rgb(157, 23, 77);
    box-shadow: -405px 0 0 400px rgb(157, 23, 77);
    border-radius: 6px;
}
input[type=range]::-moz-range-thumb {
    border: none;
    height: 12px;
    width: 24px;
    border-radius: 6px;
    background: rgb(157, 23, 77);
}
</style>