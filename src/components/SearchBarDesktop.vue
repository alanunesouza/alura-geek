<template id="search-bar">
  <form>
    <div class="container">
      <input
        type="search"
        id="input-search"
        class="input"
        placeholder="O que você deseja encontrar?"
        required
      />
      <button type="submit">
        <svg
          aria-hidden="true"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
          ></path>
        </svg>
      </button>
    </div>
  </form>
</template>

<style scoped>
.container {
  display: flex;
  flex: 1;
  align-items: center;
  position: relative;
}

.container input {
  height: 40px;
  width: 272px;
  padding: 8px 16px;
  border-radius: 20px;
  background-color: #f5f5f5;
  font-size: 14px;
  border: none;
  outline: none;
}

.container button {
  position: absolute;
  right: 0.875rem;
  background-color: #f5f5f5;
  outline: none;
  border: none;
  padding: 0px;
}

.container button > svg {
  width: 24px;
  height: 24px;
  color: #a2a2a2;
}
</style>

<script>
export default {
  name: "SearchBarDesktop",
  methods: {},
};
</script>
