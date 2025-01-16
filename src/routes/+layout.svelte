<script>
    import "../app.css";
    import Header from "../components/Header.svelte";
    import Footer from "../components/Footer.svelte";
  
    let y = 0;
    let innerHeight = 0;
    let innerWidth = 0;
  
    function goTop() {
      document.body.scrollIntoView();
    }
  </script>
  
  <div class="relative flex flex-col max-w-[1920px] mx-auto w-full text-sm sm:text-base min-h-screen">
      <Header y={y}/>
      <slot />
      <!-- <Footer /> -->
  </div>
  
  <svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />