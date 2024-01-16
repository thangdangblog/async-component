<script setup>
import { ref,defineAsyncComponent } from 'vue';
import SayHiModal from './components/SayHiModal.vue'
import Loading from './components/Loading.vue'
import Error from './components/Error.vue'

const showModal = ref(false);
const showModalAsync = ref(false);

const SayAsyncModal = defineAsyncComponent({
  loader: () => import('./components/SayAsyncModal.vue'),
  loadingComponent: Loading,
  errorComponent: Error,
})

const openModal = () => {
  showModal.value = true;
};

const openModalAsync = () => {
  showModalAsync.value = true;
};
</script>

<template>
  <div class="center-screen">
    <button class="btn-primary" @click="openModal" style="margin-right: 16px;">Open SayHi Modal</button>
    <button class="btn-primary" @click="openModalAsync">Open Async Modal</button>
    <SayHiModal v-if="showModal" />
    <SayAsyncModal v-if="showModalAsync" />
  </div>
</template>

<style scoped>
.center-screen {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.btn-primary {
  color: #fff;
  background-color: #007bff;
  border-color: #007bff;
  padding: .375rem .75rem;
  font-size: 1rem;
  line-height: 1.5;
  border-radius: .25rem;
  cursor: pointer;
  text-align: center;
  user-select: none;
  vertical-align: middle;
  transition: color .15s ease-in-out, background-color .15s ease-in-out, border-color .15s ease-in-out, box-shadow .15s ease-in-out;
}
</style>
