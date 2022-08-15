<script>
    export let title, subtitle, items;
</script>
<section class="section blog" id="blog" aria-label="blog">
    <div class="container">

      <p class="section-subtitle">{subtitle}</p>

      <h2 class="h2 section-title text-center">{title}</h2>
 
      <ul class="blog-list has-scrollbar">
        {#each items as item}
        <li class="scrollbar-item">
          <div class="blog-card">

            <div class="card-banner img-holder" style="--width: 440; --height: 270;">
              <img src="assets{item.image.url}" width="440" height="270" loading="lazy"
                alt="{item.image.alt}" class="img-cover">

              <time class="card-meta" datetime="2022-07-07">{item.date}</time>
            </div>

            <div class="card-content">

              <h3 class="h3">
                <a href="{item.blog.url}" class="card-title">{item.blog.title}</a>
              </h3>

              <p class="card-text">
                {item.blog.body}
              </p>

              <a href="{item.link.url}" class="btn-link has-before">{item.link.title}</a>

            </div>

          </div>
        </li>
        {/each}
      </ul>
    </div>
  </section>
