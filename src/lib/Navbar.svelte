<script>
  let showIcon = false; // Controls the state of the icon

  function toggleIcon() {
    showIcon = !showIcon; // Toggle the icon state on hover
  }
</script>

<style>  .is-icon {
    display: inline-block;
    transform: translateY(-110%);
    transition: transform 500ms ease; /* Precisely 300ms */
  }
  .navbar_component:hover .is-icon {
    transform: translateY(0);
  }
</style>

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
    <script type="text/javascript">
      !(function (o, c) {
        var n = c.documentElement,
          t = " w-mod-";
        (n.className += t + "js"),
          ("ontouchstart" in o ||
            (o.DocumentTouch && c instanceof DocumentTouch)) &&
            (n.className += t + "touch");
      })(window, document);
    </script>
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
        id="w-node-_2503f5d2-c0e0-792d-68fc-322d2b056fee-f97f54c1"
        data-w-id="2503f5d2-c0e0-792d-68fc-322d2b056fee"
        class="navbar_logo-link w-nav-brand"
      >
        <div class="navbar_logo-image-wrapper">
          <img
            class="navbar_logo"
            src="images/joe-webb-selfie.png"
            alt=""
            sizes="(max-width: 479px) 18vw, 64px"
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
            sizes="(max-width: 479px) 18vw, 64px"
            loading="eager"
            srcset="images/webclip-p-500.png 500w, images/webclip.png 600w"
          />
        </div>
        <div class="navbar_text-wrapper">
          <div class="navbar_text">Joe Webb Designs</div>
        </div>
      </a>
      <div
        id="w-node-_2503f5d2-c0e0-792d-68fc-322d2b057003-f97f54c1"
        class="navbar_button-wrapper"
      >
        <a href="#" class="button is-navbar-button hide-tablet w-inline-block">
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
