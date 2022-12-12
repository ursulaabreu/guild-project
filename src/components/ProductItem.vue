<template>
  <div>
    {{ item.type }}
  </div>
  <div>
    {{ item.name }}
  </div>
  <div>
    {{ item.description }}
  </div>
  <div>
    {{ item.stock }}
  </div>
</template>

<script>
export default {
  name: 'ProductItem',
  props: {
    item: null,
  },
};
</script>

<style scoped></style>
