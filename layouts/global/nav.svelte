
      <script>
        let y, navActive;
          const toggleMenu = () => {
          navActive = !navActive;
          }
          const scroll = e => {
               document.getElementById(e.target.hash.substring(1)).scrollIntoView();
          }
      </script>
     <svelte:window bind:scrollY={y}/>
      <a href="." class="logo">
        <ion-icon name="barbell-sharp" aria-hidden="true" role="img" class="md hydrated"></ion-icon>

        <span class="span">Fitlife</span>
      </a>
   
      <nav class="navbar {navActive ? ' active' : ''} {y > 20 ? ' sticky' : ''}" on:click={toggleMenu} data-navbar="">

        <button class="nav-close-btn" aria-label="close menu" data-nav-toggler="">
          <ion-icon name="close-sharp" aria-hidden="true" role="img" class="md hydrated"></ion-icon>
        </button>

        <ul class="navbar-list">

          <li>
            <a on:click|preventDefault={e => scroll(e)} href="#home" class="navbar-link active" data-nav-link="">Home</a>
          </li>

          <li>
            <a on:click|preventDefault={e => scroll(e)} href="#about" class="navbar-link" data-nav-link="">About Us</a>
          </li>

          <li>
            <a on:click|preventDefault={e => scroll(e)} href="#class" class="navbar-link" data-nav-link="">Classes</a>
          </li>

          <li>
            <a on:click|preventDefault={e => scroll(e)} href="#blog" class="navbar-link" data-nav-link="">Blog</a>
          </li>

          <li>
            <a on:click|preventDefault={e => scroll(e)} href="." class="navbar-link" data-nav-link="">Contact Us</a>
          </li>

        </ul>

      </nav>

      <a href="." class="btn btn-secondary">Join Now</a>

      <button class="nav-open-btn" on:click={toggleMenu} aria-label="open menu" data-nav-toggler="{navActive ? ' active' : ''}">
        <span class="line"></span>
        <span class="line"></span>
        <span class="line"></span>
      </button>