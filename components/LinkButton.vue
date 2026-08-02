<template>
  <a class="button" :href="link">
    <h3 class="button-text">{{ text }}</h3>
  </a>
</template>

<script lang="ts">
export default {
  name: 'LinkButton',
  props: {
    text: {
      type: String,
      required: true,
    },
    link: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.button {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0.9vw 2.2vw;
  border-radius: 30px;
  background-color: #ac3828;
  border: 4px solid #e9cb9d;
  transition: 0.3s;
  width: fit-content;
  margin: 0 auto;
  margin-top: 1vw;
  margin-bottom: 1vw;
}

.button:hover {
  background-color: #c9432f;
  transform: translateY(-2px);
  transition: 0.3s;
}

.button-text {
  font-family: Aleo;
  font-weight: bold;
  font-size: 1.8rem;
  white-space: nowrap;
}

/* mobile view */
@media (max-width: 768px) {
  .button {
    margin-top: 17px;
    padding: 3vw 6vw;
    width: fit-content;
  }

  .button-text {
    font-size: 2.6rem;
  }
}
</style>
