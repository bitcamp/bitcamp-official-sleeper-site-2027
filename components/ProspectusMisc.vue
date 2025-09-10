<template>
  <div
    class="Rtable-cell Rtable-category-cell"
    :class="'Rtable-misc-category-cell-' + type"
  >
    <a
      v-if="perk !== 'Add-Ons'"
      class="tooltips direction"
      :title="perk"
      :description="description"
    >
      <img
        src="../assets/img/icons/question-mark-black.svg"
        alt="Question Mark"
      />
    </a>
    <div :style="perk === 'Add-Ons' ? 'margin-left: 1rem': ''">
      <span v-if="bolded" style="color: var(--color-dark-text)"
        ><b>{{ perk }}</b></span
      >
      <span v-else style="font-size: 15.5px; color: var(--color-dark-text)">{{
        perk
      }}</span>
      <div
        v-if="note"
        style="
          margin-top: 4px;
          font-size: 0.85em;
          color: var(--color-dark-text);
        "
      >
        {{ note }}
      </div>
    </div>
  </div>

  <div
    class="Rtable-cell Rtable-cell-misc"
    :class="'Rtable-misc-cell-' + type"
    style="color: var(--color-dark-text)"
  >
    {{ price }}
  </div>
  <div class="Rtable-cell Rtable-cell-blank"></div>
  <div class="Rtable-cell Rtable-cell-blank"></div>
  <div class="Rtable-cell Rtable-cell-blank"></div>
  <div class="Rtable-cell Rtable-cell-blank"></div>
  <div class="Rtable-cell Rtable-cell-blank"></div>
</template>

<script>
export default {
  name: "ProspectusFooter",
  props: {
    perk: {
      type: String,
      required: true,
    },
    bolded: {
      type: Boolean,
      required: true,
    },
    price: {
      type: String,
      required: true,
    },
    type: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    note: {
      type: String,
      required: false,
      default: "",
    },
  },
};
</script>

<style scoped>
.boldClass {
  font-weight: bold;
}
</style>
