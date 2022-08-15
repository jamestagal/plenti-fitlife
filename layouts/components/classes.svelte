
<script>
    export let title, subtitle, items;
</script>
<section class="section class bg-dark has-bg-image" id="class" aria-label="class" style="background-image: url('./assets/images/classes-bg.png')">
    <div class="container">

      <p class="section-subtitle">{subtitle}</p>

      <h2 class="h2 section-title text-center">{title}</h2>
  
          <ul class="class-list has-scrollbar">
            {#each items as item}
            <li class="scrollbar-item">
              <div class="class-card">

                <figure class="card-banner img-holder" style="--width: 416; --height: 240;">
                  <img src="assets{item.image.url}" width="416" height="240" loading="lazy" alt="{item.image.alt}" class="img-cover">
                </figure>

                <div class="card-content">

                  <div class="title-wrapper">
                    <img src="assets{item.icon.url}" width="52" height="52" aria-hidden="true" alt="item.icon.alt" class="title-icon">

                    <h3 class="h3">
                      <a href="{item.class.url}" class="card-title">{item.class.name}</a>
                    </h3>
                  </div>

                  <p class="card-text">
                    {item.body}
                  </p>

                  <div class="card-progress">

                    <div class="progress-wrapper">
                      <p class="progress-label">{item.bars.label}</p>

                      <span class="progress-value">{item.bars.percent}</span>
                    </div>

                    <div class="progress-bg">
                      <div class="progress-bar" style="width: 85%"></div>
                    </div>

                  </div>

                </div>

              </div>
            </li>
          {/each}
        </ul>
    </div>
  </section>