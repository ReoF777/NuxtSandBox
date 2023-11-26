<!-- components/Sidebar.vue -->

<template>
  <aside class="bg-blue-500 w-1/4 p-4 h-screen" id="all">
    <!-- Sidebar content goes here -->
    <ul>
      <li>リスト１</li>
      <li>Menu Item 2</li>
      <li>Menu Item 3</li>
    </ul>
  </aside>
</template>

<style scoped>
.all {
  background-color: #4c4141;
  color: #876ed9;
  padding: 1rem;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin-bottom: 0.5rem;
}

a {
  text-decoration: none;
  color: #333;
  font-weight: bold;
}
</style>
