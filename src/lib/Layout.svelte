<script>
  import Navbar from "./components/Navbar.svelte";
  import Title from "./components/Title.svelte";
  import Article from "./components/Article.svelte";
  import Section from "./components/Section.svelte";
</script>
<Navbar />
  <Title/>
  <Article />
  <Section />


  <div>
    <p class="attribution">
      Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
      <!-- svelte-ignore a11y-invalid-attribute -->
      Coded by <a href="https://github.com/gsuSUPREME/">gsuSUPREME</a>.
    </p>
  </div>

<style>
    .attribution {font-family: "Raleway", sans-serif; font-weight: 700; font-size: 0.8em; text-align: center; }
    .attribution a { color: hsl(228, 45%, 44%); }
    
</style>
