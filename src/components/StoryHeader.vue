<template>
  <div class="story-header">
    <div
      class="story-icon"
    >
      <img src="https://www.talenta.co/wp-content/themes/talenta/images/favicon.png">
    </div>
    <div class="story-user">Talenta</div>
  </div>
</template>

<style scoped>
.story-header {
    display: flex;
    justify-items: center;
}

.story-icon {
    height: 28px;
    width: 28px;
    padding: 4px;
    border-radius: 100%;
    background-color: #FFF;
    display: flex;
    justify-content: center;
}

.story-icon img {
    height: 28px;
    width: 28px;
}

.story-user {
    font-weight: bold;
    color: #FFF;
    margin-left: 8px;
    margin-top: 8px;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}
</style>

<script>
export default {
  name: "Story Header",
};
</script>