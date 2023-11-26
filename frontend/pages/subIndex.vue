<template>
  <div class="flex bg-blue-100">
    <Sidebar />
    <div class="flex-1 flex flex-col items-center justify-center h-screen">
      <h1 class="text-4xl font-bold text-center text-indigo-700 mb-4">Nuxt</h1>
      <button @click="fetchData" class="text-4xl font-bold text-center">データを取得</button>
      <p class="text-4xl text-center">取得データ: {{ data }}</p>
    </div>
  </div>
</template>

<script>
import Sidebar from '~/components/Sidebar.vue';

export default {
  components: {
    Sidebar,
  },
  data() {
    return {
      message: '',
      data: null,
    };
  },
  methods: {
    async fetchData() {
      try {
        const response = await this.$axios.get('http://localhost:5000');
        const result = response.data;
        this.data = result;
      } catch (error) {
        console.error('データの取得中にエラーが発生しました:', error);
      }
    },
  },
};
</script>
