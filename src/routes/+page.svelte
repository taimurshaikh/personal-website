<script lang="ts">
  import Intro from "../components/Intro.svelte";
  import About from "../components/About.svelte";
  import Projects from "../components/Projects.svelte";
  import Contact from "../components/Contact.svelte";
</script>

<div class="relative max-w-screen-xl mx-auto p-8">
  <Intro
    name="Taimur Shaikh"
    bio="I'm a third-year student at Columbia studying Computer Science and Operations Research. I'm interested in software engineering, data science, and machine learning. This website is a collection of my projects, blog posts, and resume."
    imageUrl="/images/profile-pic.jpeg"
  />

  <!-- Sections -->
  <div class="flex flex-col items-center w-full">
    <About />
    <Projects />
    <Contact />
  </div>
</div>
