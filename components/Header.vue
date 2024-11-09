<!-- components/Header.vue -->
<template>
    <header class="header">
      <div class="header-left">
        <button>
          <span></span>
          <span></span>
          <span></span>
        </button>
        <figure>
          <img width="93px" alt="veronica logo" src="assets/images/veronica-logo.svg" />
        </figure>
        <nav>
          <ol>
            <li><a href="/">Home</a></li>
            <li><a href="/">Ontdek</a></li>
            <li><a href="/">Radio</a></li>
          </ol>
        </nav>
      </div>
      <div class="header-right">
        <!-- Use the Button component -->
        <Button title="App studio" label="App studio" />
      </div>
    </header>
  </template>
  
  <script>
  import Button from './Button.vue';
  
  export default {
    components: {
      Button
    }
  };
  </script>
  
  <style scoped>
  .header {
    padding: 1rem 2rem;
    background-color: var(--primary-color);
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .header-left {
    display: flex;
    align-items: center;
    gap: 4rem;
  }
  .header-left button {
    border: none;
    padding: 0;
  }
  .header-left button span {
    height: 2px;
    width: 24px;
    background-color: var(--light);
    position: absolute;
  }
  .header-left button span:nth-child(1) {
    margin-top: -10px;
  }
  .header-left button span:nth-child(2) {
    margin-top: -2px;
  }
  .header-left button span:nth-child(3) {
    margin-top: 6px;
  }
  .header-left nav ol {
    display: flex;
    gap: 2rem;
  }
  .header-left nav ol li a {
    color: var(--light);
    font-size: 1em;
    text-transform: uppercase;
    text-decoration: none;
  }
  .header-right {
    display: flex;
    align-items: center;
    position: absolute;
    right: 2em;
  }
  </style>
  