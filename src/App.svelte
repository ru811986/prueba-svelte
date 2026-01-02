<script>
  import "./app.css";
  import Header from "./components/header/Header.svelte";
  import Footer from "./components/footer/Footer.svelte";
</script>

<div class="min-h-screen flex flex-col">
  <Header />
  <div class="grow container mx-auto p-4">
    <slot />
  </div>
  <Footer />
</div>
