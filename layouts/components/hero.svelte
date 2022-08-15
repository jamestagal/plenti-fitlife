<script>
    export let title, subtitleA, subtitleB, body, link, images, background;
</script>
<section class="section hero bg-dark has-after has-bg-image" id="home" aria-label="hero" data-section="" style="background-image: url('assets{background.url}')">
    <div class="container">

      <div class="hero-content">

        <p class="hero-subtitle">
          <strong class="strong">{subtitleA}</strong>
          {subtitleB}
        </p>

        <h1 class="h1 hero-title">{title}</h1>

        <p class="section-text">
         {body}
        </p>

        <a href="{link.url}" class="btn btn-primary">{link.title}</a>

      </div>

      <div class="hero-banner">

        <img src="assets{images.banner.url}" width="660" height="753" alt="{images.banner.alt}" class="w-100">

        <img src="assets{images.circle1.url}" width="666" height="666" aria-hidden="true" alt="{images.circle1.alt}" class="circle circle-1">
        <img src="assets{images.circle2.url}" width="666" height="666" aria-hidden="true" alt="{images.circle2.alt}" class="circle circle-2">

        <img src="assets{images.heartrate.url}" width="255" height="270" alt="{images.heartrate.alt}" class="abs-img abs-img-1">
        <img src="assets{images.calories.url}" width="348" height="224" alt="{images.calories.alt}" class="abs-img abs-img-2">

      </div>
    </div>
  </section>