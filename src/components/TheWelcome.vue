<template>
  <div>
    <div class="container">
      <header>
        <div class="search">
          <i>签</i>
          <input type="text" placeholder="请输入商品名称" />
        </div>
      </header>
      <section></section>
      <footer></footer>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
}
.search {
  max-width: 720px;
  background-color: #fb3950;
  border-radius: 0 0 1rem 1rem;
  padding: 1rem 0;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.search i {
  color: #fff;
  margin-left: 0.5rem;
}
.search input {
  flex: 1;
  border-radius: 1rem;
  padding: 0.5rem 0;
  margin: 0 1rem;
  text-align: center;
  color: #777;
  border: none;
}
</style>
