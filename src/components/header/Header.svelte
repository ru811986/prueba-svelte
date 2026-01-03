<script>
  import { Link } from "svelte-routing";

  let showMenu = false;

  function toggleNavbar() {
    showMenu = !showMenu;
  }
</script>

<div class="w-full blue shadow">
  <nav
    class="container px-6 py-8 mx-auto md:flex md:justify-between md:items-center"
  >
    <div class="flex items-center justify-between">
      <a
        class="text-xl font-bold text-white md:text-2xl hover:text-black"
        href="/home"
        >Mi Sitio Web
      </a>
      <!-- Mobile menu button -->
      <button
        type="button"
        class="flex text-white hover:text-gray-300 focus:outline-none focus:text-gray-300 md:hidden"
        on:click={toggleNavbar}
        title="Menú"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
          />
        </svg>
      </button>
    </div>

    <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
    <div
      class="flex-col mt-8 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-10 md:mt-0 {showMenu
        ? 'flex'
        : 'hidden'}"
    >
      <Link to="/home" class="text-white hover:text-black">Home</Link>
      <Link to="/blog" class="text-white hover:text-black">Blogs</Link>
      <Link to="/contact" class="text-white hover:text-black">Contact US</Link>
      <Link to="/about" class="text-white hover:text-black">About Us</Link>
    </div>
  </nav>
</div>
