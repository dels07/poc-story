<template>
  <Stories
    :stories="items"
    :loop="true"
    :interval="5000"
  >
    <template #header="">
      <story-header :label="Talenta" />
    </template>
  </Stories>
</template>

<script>
import { Stories } from "vue-insta-stories";
import StoryHeader from "./StoryHeader"
export default {
  components: { Stories, StoryHeader },
  data: () => ({
    items: [
      require("../assets/1.png"),
      require("../assets/2.png"),
      require("../assets/3.png"),
      require("../assets/4.png"),
    ]
  })
};
</script>
