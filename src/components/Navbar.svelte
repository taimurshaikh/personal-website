<script lang="ts">
  let isOpen = false;

  function toggleMenu() {
    isOpen = !isOpen;
  }

  function scrollToComponent(componentId: string) {
    const component = document.getElementById(componentId);
    if (component) {
      component.scrollIntoView({ behavior: "smooth" });
    }
  }
</script>

<nav
  class="bg-white bg-gradient-to-b from-gray-100 to-white text-gray-800 shadow-md px-4 py-3 md:flex md:items-center md:justify-between"
>
  <div class="flex justify-between items-center">
    <div class="text-2xl font-bold">
      <a href="/">Brand</a>
    </div>
    <button class="md:hidden" on:click={toggleMenu}>
      <svg
        class="w-6 h-6"
        fill="none"
        stroke="currentColor"
        viewBox="0 0 24 24"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M4 6h16M4 12h16m-7 6h7"
        ></path>
      </svg>
    </button>
  </div>
  <div class={`md:flex md:items-center ${isOpen ? "block" : "hidden"}`}>
    <a
      href="#"
      on:click|preventDefault={() => scrollToComponent("about")}
      class="block mt-4 md:inline-block md:mt-0 md:ml-6 hover:text-gray-600"
      >About</a
    >
    <a
      href="#"
      on:click|preventDefault={() => scrollToComponent("projects")}
      class="block mt-4 md:inline-block md:mt-0 md:ml-6 hover:text-gray-600"
      >Projects</a
    >
    <a
      href="#"
      on:click|preventDefault={() => scrollToComponent("contact")}
      class="block mt-4 md:inline-block md:mt-0 md:ml-6 hover:text-gray-600"
      >Contact</a
    >
  </div>
</nav>

<style>
  nav a {
    transition: color 0.3s ease;
  }
</style>
