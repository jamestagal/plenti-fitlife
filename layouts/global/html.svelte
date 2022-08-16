<script>
  import Footer from './footer.svelte';
  import Head from './head.svelte';
  import Nav from "./nav.svelte";
  export let content, layout, allContent, allLayouts;
  let y;
</script>
<svelte:window bind:scrollY={y}/>
<html lang="en">
<Head title={content.filename} />
<body>
  <div class="data-back-top-btn {y > 100 ? ' active' : ''}">
  <header class="header{y > 100 ? ' active' : ''}" data-header="">
    <div class="container">
        <Nav />
    </div>
  </header>
  <svelte:component this={layout} {...content.fields} {allContent} {allLayouts} {content}/>
  <Footer />
  <a href="#top" class="back-top-btn" aria-label="back to top" data-back-top-btn>
    <ion-icon name="caret-up-sharp" aria-hidden="true"></ion-icon>
  </a>
</body>
</html>