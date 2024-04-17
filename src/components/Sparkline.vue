<template>
  <v-container class="fill-height">
    <v-sparkline
      :gradient="selectedGradient"
      :line-width="lineWidth"
      :model-value="value"
      :padding="padding"
      :smooth="smooth"
      auto-draw="false"
      :autoDrawDuration="10000"
    ></v-sparkline>
  </v-container>
</template>

<script>
const gradients = [  
  ["green", "red"],  
];

export default {
  data: () => ({
    fill: true,
    selectedGradient: gradients[0],
    gradients,
    padding: 8,
    smooth: true,
    value: [0, 2, 5, 9, 5, 10, 3, 5, 0, 0, 1, 8, 2, 9, 0],
    lineWidth: 2,
  }),
};
</script>
