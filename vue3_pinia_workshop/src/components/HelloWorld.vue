<template>
  <h1>Pinia State Management</h1>
  <div
    style="padding: 30px; background-color: yellow"
    @click="counterV1Store.add"
  >
    {{ counterV1Store.count }}
  </div>
  <hr />
  <div
    style="padding: 30px; background-color: greenyellow"
    @click="counterV2Store.add"
  >
    {{ counterV2Store.count }}
  </div>
</template>

<script lang="ts">
import { useCounterV1Store } from "../store/useCounterV1Store";
import { useCounterV2Store } from "../store/useCounterV2Store";
export default {
  setup() {
    const counterV1Store = useCounterV1Store();
    const counterV2Store = useCounterV2Store();
    return { counterV1Store, counterV2Store };
  },
};
</script>

<style></style>
