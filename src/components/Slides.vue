<template>
  <Stories
    @seeMore="open"
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
import { saveAs } from "file-saver";
import StoryHeader from "./StoryHeader";

export default {
  components: { Stories, StoryHeader },
  data: () => ({
    items: [
      {
        url: require("../assets/1.png"),
        type: 'image',
        seeMore: { label: 'Download', url: require("../assets/1.png") },
      },
      {
        url: require("../assets/2.png"),
        type: 'image',
        seeMore: { label: 'Download', url: require("../assets/2.png") },
      },
      {
        url: require("../assets/3.png"),
        type: 'image',
        seeMore: { label: 'Download', url: require("../assets/3.png") },
      },
      {
        url: require("../assets/4.png"),
        type: 'image',
        seeMore: { label: 'Download', url: require("../assets/4.png") },
      },
    ]
  }),
  methods: {
    open(story) {
      const { url } = story.seeMore;
      const filename = url.split('/');

      saveAs(url, filename[filename.length - 1]);
    }
  }
};
</script>
