<script>
    export let title, subtitle, body, coach, images, link;
</script>
<section class="section about" id="about" aria-label="about">
    <div class="container">

      <div class="about-banner has-after">
        <img src="assets{images.banner.url}" width="660" height="648" loading="lazy" alt="{images.banner.alt}" class="w-100">

        <img src="assets{images.circle1.url}" width="660" height="534" loading="lazy" aria-hidden="true" alt="{images.circle1.alt}" class="circle circle-1">
        <img src="assets{images.circle2.url}" width="660" height="534" loading="lazy" aria-hidden="true" alt="{images.circle2.alt}" class="circle circle-2">

        <img src="assets{images.fitness.url}" width="650" height="154" loading="lazy" alt="{images.fitness.alt}" class="abs-img w-100">
      </div>

      <div class="about-content">

        <p class="section-subtitle">{subtitle}</p>

        <h2 class="h2 section-title">{title}</h2>

        <p class="section-text">
          {@html body}
        </p>

        <div class="wrapper">

          <div class="about-coach">

            <figure class="coach-avatar">
              <img src="assets{images.coach.url}" width="65" height="65" loading="lazy" alt="{images.coach.alt}">
            </figure>

            <div>
              <h3 class="h3 coach-name">{coach.name}</h3>

              <p class="coach-title">{coach.title}</p>
            </div>

          </div>

          <a href="{link.url}" class="btn btn-primary">{link.title}</a>

        </div>

      </div>

    </div>
  </section>