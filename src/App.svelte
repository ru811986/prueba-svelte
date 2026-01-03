<script>
  import { Router, Route, Link } from "svelte-routing";
  import Header from "./components/header/Header.svelte";
  import Footer from "./components/footer/Footer.svelte";
  import Home from "./routes/home/Home.svelte";
  import Blog from "./routes/blog/Blog.svelte";
  import Contact from "./routes/contact/Contact.svelte";
  import About from "./routes/about/About.svelte";
</script>

<Router>
  <div class="min-h-screen flex flex-col">
    <Header />
    <main class="grow container mx-auto p-4">
      <Route path="/home">
        <Home />
      </Route>
      <Route path="/blog">
        <Blog />
      </Route>
      <Route path="/contact">
        <Contact />
      </Route>
      <Route path="/about">
        <About />
      </Route>
    </main>
    <Footer />
  </div>
</Router>
