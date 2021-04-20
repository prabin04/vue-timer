<template>
  <p>Reaction time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 200) {
      this.rank = "Prabinhood Achieved";
    } else if (this.score < 400) {
      this.rank = "Rapid fire";
    } else {
      this.rank = "Snail snail";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: green;
  font-weight: bold;
}
</style>