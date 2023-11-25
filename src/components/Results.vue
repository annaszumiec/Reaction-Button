<template>
  <p>Your reflex time is:{{ score }} ms</p>
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
    if (this.score < 250) {
      this.rank = "Jambo Jet";
    } else if (this.score < 400) {
      this.rank = "Rocket ";
    } else {
      this.rank = "Snail pace....";
    }
  },
};
</script>
  
  <style>
.rank {
  font-size: 1.4em;
  color: #ffc300;
  font-weight: bold;
}
</style>