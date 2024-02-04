<script>
  import { onMount } from "svelte";
  let navbarStyle = "width: 30rem; overflow: hidden;"; // Default style
  let menuButtonOpacity = 0;

  function updateNavbar() {
    const st = window.scrollY; // Updated from window.pageYOffset to window.scrollY
    const width = document.body.offsetWidth;
    if (width > 991) {
      const isScrollingUp = st < lastScrollTop;
      const condition = isScrollingUp ? 500 : 100;
      if (window.scrollY > condition) {
        // Updated here as well
        navbarStyle = "width: 39rem; overflow: visible;";
        menuButtonOpacity = 1;
      } else {
        navbarStyle = "width: 30rem; overflow: hidden;";
        menuButtonOpacity = 0;
      }
      lastScrollTop = st <= 0 ? 0 : st; // Prevent negative scroll values
    }
  }

  let lastScrollTop = 0;
  onMount(() => {
    window.addEventListener("scroll", updateNavbar);
    // return () => {
    //   window.removeEventListener('scroll', updateNavbar);
    // };
  });

  let showIcon = false; // Controls the state of the icon

  function toggleIcon() {
    showIcon = !showIcon; // Toggle the icon state on hover
  }
</script>

<svelte:head>
  <link
    href="css/agency-landing-page-a76d1e.webflow.css"
    rel="stylesheet"
    type="text/css"
  />
  <link href="https://fonts.googleapis.com" rel="preconnect" />
  <link
    href="https://fonts.gstatic.com"
    rel="preconnect"
    crossorigin="anonymous"
  />
</svelte:head>

<div
  data-animation="default"
  class="navbar_component w-nav"
  data-easing2="ease"
  fs-scrolldisable-element="smart-nav"
  data-easing="ease"
  data-collapse="medium"
  data-w-id="2503f5d2-c0e0-792d-68fc-322d2b056fec"
  role="banner"
  data-no-scroll="1"
  data-duration="400"
  bind="2503f5d2-c0e0-792d-68fc-322d2b056fec"
      on:mouseenter={toggleIcon}
  on:mouseleave={toggleIcon}
>
  <div class="navbar_container">
    <a
      href="/"
      id="w-node-_2503f5d2-c0e0-792d-68fc-322d2b056fee-b19dbc34"
      data-w-id="2503f5d2-c0e0-792d-68fc-322d2b056fee"
      target="_blank"
      aria-current="page"
      class="navbar_logo-link w-nav-brand w--current"
    >
      <div class="navbar_logo-image-wrapper">
        <img
          class="navbar_logo"
          src="images/joe-webb-selfie.png"
          alt=""
          sizes="(max-width: 479px) 71vw, 64px"
          loading="eager"
          srcset="
                  images/joe-webb-selfie-p-500.png 500w,
                  images/joe-webb-selfie.png       639w
                "
        /><img
          class="navbar_logo is-icon"
          src="images/webclip.png"
          alt=""
           style="transform: translateY({showIcon ? 0 : '-110%'});"
          sizes="(max-width: 479px) 71vw, 64px"
          loading="eager"
          srcset="images/webclip-p-500.png 500w, images/webclip.png 600w"
        />
      </div>
      <div class="navbar_text-wrapper">
        <div class="navbar_text">Joe Webb Designs</div>
      </div>
    </a>
    <nav role="navigation" class="navbar_menu is-page-height-tablet w-nav-menu">
      <a href="#work" class="navbar_link w-nav-link">Work</a>
      <a href="#capability" class="navbar_link w-nav-link">Capabilities</a>
      <a href="#process" class="navbar_link w-nav-link">Process</a>
      <a href="#testimonial" class="navbar_link w-nav-link">Testimonial</a>
      <a
        href="https://form.jotform.com/lissanh95/project-requirements"
        class="button is-navbar-button menu_button w-inline-block"
      >
        <div class="button_circle menu_button-circle"></div>
        <div class="button_text-regular is-menu-button-text">Hire me</div>
      </a>
    </nav>
    <div
      id="w-node-_2503f5d2-c0e0-792d-68fc-322d2b057003-b19dbc34"
      class="navbar_button-wrapper"
    >
      <a
        href="/landing"
        class="button is-navbar-button hide-tablet w-inline-block"
      >
        <div class="button_circle"></div>
        <div class="button_text-small">Hire me</div>
      </a>
      <div class="navbar_menu-button w-nav-button">
        <div class="menu-icon">
          <div class="menu-icon_line-top"></div>
          <div class="menu-icon_line-middle">
            <div class="menu-icon_line-middle-inner"></div>
          </div>
          <div class="menu-icon_line-bottom"></div>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .is-icon {
    display: inline-block;
    transform: translateY(-110%);
    transition: transform 500ms ease; /* Precisely 300ms */
  }
  .navbar_component:hover .is-icon {
    transform: translateY(0);
  }
</style>
