<script>
    export let title, link, image;
</script>
<section class="section video" aria-label="video">
    <div class="container">

      <div class="video-card has-before has-bg-image" style="background-image: url('assets{image.url}')">

        <h2 class="h2 card-title">{title}</h2>

        <button class="play-btn" aria-label="play video">
          <ion-icon name="play-sharp" aria-hidden="true" role="img" class="md hydrated"></ion-icon>
        </button>

        <a href="{link.url}" class="btn-link has-before">{link.title}</a>

      </div>

    </div>
  </section>