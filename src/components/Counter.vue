<template>
  <div class="root">
    <p>
    </p>
    <button
        type="button"
        @click="decrementCount"
    >
      Уменьшить
    </button>
    <input
        type="number"
        :value="count"
        :min="minCount"
    >
    <button
        type="button"
        @click="incrementCount"
    >
      Увеличить
    </button>
  </div>
</template>

<script>
export default {
  name: 'MyComponent',
  data() {
    return {
      count: 1,
      minCount: 0
    }
  },
  methods: {
    incrementCount() {
      this.count++
    },
    decrementCount() {
      if (this.count > this.minCount) {
        this.count--
      }
    }
  }
}
</script>
