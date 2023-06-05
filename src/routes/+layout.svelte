<nav>

    <div class="nav-container">
        <a href="/" class="nav-logo" title="Back to Homepage">
          Главная страница
        </a>
        <div class="nav-links">
            {#each nav as link}
                {#if link.isShow}
                 <a href={link.href} class="link">{link.title}</a>
                {/if}
            {/each}
          

        </div>
    </div>
  </nav>
  <div class="container">
    <!-- Pages will be injected below -->
    <slot></slot>
  </div>
  
  <style>
    .container {
      max-width: 1400px;
      margin: 50px auto;
    }
  </style>

  <!--скрипт-->
  <script>
    const nav = [
    {
      title: 'О нас',
      href: '/about',
      isShow: true,
    },
    {
      title: 'Блог',
      href: '/blog',
      isShow: false,
    },
    {
      title: 'Портфолио',
      href: '/project',
      isShow: false,
    },
    {
      title: 'Контакты',
      href: '/contact',
      isShow: true,
    },
    {
      title: 'temp',
      href: '/temp',
      isShow: false,
    }
  ]
</script>
