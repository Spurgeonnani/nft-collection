<template>
    <footer class="my-footer">
      <div class="footer-content">
        <p>© 2024 <strong>NFT Collection</strong></p>
        <p>Proudly powered by blockchain technology and Digital World.</p>
        <div class="footer-links">
          <a href="https://discord.gg/qYVF7amk" target="_blank" rel="noopener noreferrer">
            Join our Discord
          </a>
          |
          <a href="https://opensea.io/" target="_blank" rel="noopener noreferrer">
            Learn more
          </a>
        </div>
        <p class="footer-tagline">
          "Own a piece of the future, one token at a time."
        </p>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: "MyFooter",
  };
  </script>
  
  <style scoped>
  .my-footer {
    background-color: #1a1a1a;
    color: #f2f2f2;
    text-align: center;
    padding: 20px 10px;
    font-family: 'Arial', sans-serif;
  }
  
  .footer-content {
    max-width: 800px;
    margin: 0 auto;
  }
  
  .footer-links {
    margin: 10px 0;
  }
  
  .footer-links a {
    color: #4caf50;
    text-decoration: none;
    margin: 0 5px;
  }
  
  .footer-links a:hover {
    text-decoration: underline;
  }
  
  .footer-tagline {
    font-style: italic;
    margin-top: 10px;
  }
  </style>
  