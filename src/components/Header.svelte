<script>
  import Logo from './Logo.svelte';
</script>

<header class="header">
  <div class="header-content">
    <div class="left">
      <Logo />
    </div>
    <div class="center">
      <button class="get-started">Get started</button>
    </div>
    <div class="right">
      <nav class="nav">
        <ul class="nav-links">
          <li><a href="/">Home</a></li>
          <li><a href="/coaches">Our Coaches</a></li>
          <li><a href="/blog">Blog</a></li>
          <li><a href="/contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </div>
</header>

<style>
  .header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 100;
    padding: 1rem 2rem;
    background-color: #1a2332;
  }

  .header-content {
    max-width: 1440px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    align-items: center;
    gap: 2rem;
  }

  .left {
    justify-self: start;
  }

  .center {
    justify-self: center;
  }

  .right {
    justify-self: end;
  }

  .nav-links {
    display: flex;
    gap: 2rem;
    list-style: none;
    margin: 0;
    padding: 0;
  }

  .nav-links a {
    color: white;
    text-decoration: none;
    font-size: 0.9375rem;
    font-weight: 500;
    transition: color 0.2s;
  }

  .nav-links a:hover {
    color: #ff5631;
  }

  .get-started {
    background-color: #ff5631;
    color: white;
    border: none;
    padding: 0.625rem 1.25rem;
    border-radius: 6px;
    font-weight: 500;
    font-size: 0.9375rem;
    cursor: pointer;
    transition: background-color 0.2s;
    white-space: nowrap;
  }

  .get-started:hover {
    background-color: #e64e2c;
  }
</style> 