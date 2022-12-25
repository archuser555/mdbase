<style>
    .container {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
  
    .title {
      font-size: 36px;
      margin: 32px 0 16px;
    }
  
    .input-container {
      display: flex;
      flex-direction: column;
      align-items: stretch;
      width: 80%;
      max-width: 500px;
    }
  
    .input-label {
      font-size: 18px;
      margin-bottom: 8px;
    }
  
    .input-field {
      font-size: 16px;
      padding: 12px;
      border: 1px solid #ccc;
      border-radius: 4px;
      box-sizing: border-box;
      width: 100%;
    }
  
    .button-container {
      display: flex;
      justify-content: space-between;
      width: 80%;
      max-width: 500px;
      margin-top: 16px;
    }
  
    .button {
      font-size: 16px;
      padding: 12px 24px;
      border: none;
      border-radius: 4px;
      background-color: #007bff;
      color: #fff;
      cursor: pointer;
    }
  
    .button:hover {
      background-color: #0069d9;
    }
  
    .output-container {
      display: flex;
      flex-direction: column;
      align-items: stretch;
      width: 80%;
      max-width: 500px;
      margin-top: 16px;
    }
  
    .output-label {
      font-size: 18px;
      margin-bottom: 8px;
    }
  
    .output-field {
      font-size: 16px;
      padding: 12px;
      border: 1px solid #ccc;
      border-radius: 4px;
      box-sizing: border-box;
      width: 100%;
      height: 100px;
    }

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
  
    @media (max-width: 768px) {
      .container {
        flex-direction: column;
        align-items: center;
      }
  
      .input-container {
        width: 90%;
        max-width: none;
      }
  
      .button-container {
        width: 90%;
        max-width: none;
      }
  
      .output-container {
        width: 90%;
        max-width: none;
      }
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
  
  <div class="container">
      <div class="title">Base64 Decoder/Encoder</div>
      <div class="input-container">
        <div class="input-label">Input</div>
        <textarea class="input-field" bind:value={input} placeholder="Enter text to encode or decode"></textarea>
      </div>
      <div class="button-container">
        <button class="button" on:click={encode}>Encode</button>
        <button class="button" on:click={decode}>Decode</button>
      </div>
      <div class="output-container">
        <div class="output-label">Output</div>
        <textarea class="output-field" bind:value={output} placeholder="Output"></textarea>
      </div>
    </div>
    
  <script>
      let input = '';
      let output = '';
    
      function encode() {
        output = btoa(input);
      }
    
      function decode() {
        output = atob(input);
      }
  </script>
    