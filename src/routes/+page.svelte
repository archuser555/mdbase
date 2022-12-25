<style>
    /* add styles for the navbar here */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 60px;
      background-color: white;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }
  
    .navbar-logo {
      font-size: 1.5rem;
      font-weight: bold;
      margin-left: 1rem;
    }
  
    .navbar-menu {
      display: flex;
      align-items: center;
    }
  
    .navbar-menu-item {
      margin: 0 1rem;
    }
  
    .navbar-menu-item a {
      text-decoration: none;
      color: #333;
    }
  
    .navbar-menu-item a:hover {
      color: #0070f3;
    }
  
    .title {
      text-align: center;
      font-size: 3rem;
      color: #333;
    }

    .text {
        text-align: center;
    }
  
    @media (max-width: 768px) {
      .navbar-menu {
        display: none;
      }
    }
  </style>
  
<nav class="navbar">
    <div class="navbar-logo">
      <a href="/">MdBase</a>
    </div>
    <div class="navbar-menu">
      <div class="navbar-menu-item">
        <a href="/">Home</a>
      </div>
      <div class="navbar-menu-item">
        <a href="/base64">Base64</a>
      </div>
      <div class="navbar-menu-item">
        <a href="/md5">Md5</a>
      </div>
    </div>
</nav>
  
<h1 class="title">Your new tools of Decryption/Encryption</h1>
<p class="text">mdbase is a project that i made in 1 day, to make who haven't openssl in his computer more productive instead of writing his own base64 enc/dec or md5 enc software!</p>