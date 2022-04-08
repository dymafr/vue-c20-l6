<template>
  <div class="d-flex flex-fill">
    <input type="text" class="mr-20 flex-fill" />
    <button @click="emit('update', input)" class="btn btn-primary mr-20">
      Sauvegarder
    </button>
    <button @click="emit('cancel')" class="btn btn-danger">Annuler</button>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{ content: string }>();

const emit = defineEmits<{
  (e: 'cancel');
  (e: 'update', updatedContent: string);
}>();

const input = ref<string>(props.content);
</script>

<style lang="scss"></style>
