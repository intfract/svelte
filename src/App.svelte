<script>
  import logo from './assets/int.svg'
  import Counter from './lib/Counter.svelte'
</script>

<main>
  <div class="splash">
    <span class="bang">
      <img src={logo}>
    </span>
  </div>
  <div class="content">
    <span>
      <h1>Int Fract</h1>
    </span>
    <span>
      <p>
        I'm a young software developer and math enthusiast. I started writing <a href="https://github.com/intfract/defract" target="_blank">JavaScript</a> code in 2018, but now I code in <a href="https://github.com/intfract/python" target="_blank">Python</a>, <a href="https://dart.dev" target="_blank">Dart</a>, and <a href="https://github.com/intfract/defract" target="_blank">TypeScript</a>. Although my favourite web framework is <a href="https://github.com/intfract/vue" target="_blank">Vue</a>, I have experience using <a href="https://github.com/intfract/svelte" target="_blank">Svelte</a> and <a href="https://github.com/intfract/react" target="_blank">React</a>. I also use <a href="https://socket.io" target="_blank">Socket.io</a> to add cool features to my website. 
      </p>
      <p>
        In my free time, I play chess and table tennis. When I feel bored, I <a href="https://github.com/intfract/polytangent">tinker</a> with calculus. 
      </p>
    </span>
    <span>
      <a href="https://github.com/intfract" target="_blank">
        <svg role="img" viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12">         </path>
        </svg>
      </a>
    </span>
  </div>
</main>

<style>
  main {
    display: flex;
    justify-content: space-between;
    width: 100%;
    height: 100%;
  }

  .splash {
    background: var(--accent);
    display: flex;
    justify-content: center;
    align-items: center;
    width: 50%;
  }

  .content {
    width: 480px;
    margin: auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  h1 {
    color: var(--accent); 
    font-size: 48px;
    margin: 0;
    animation: wipe 0.5s;
  }

  a {
    color: var(--accent);
    text-decoration: none;
    transition: 0.2s;
  }

  p a:hover {
    color: var(--accent);
    text-decoration: none;
    opacity: 0.75;
  }

  span {
    font-size: 0px;
    overflow: hidden;
  }

  p {
    font-size: 16px;
    line-height: 1.5;
    animation: wipe 0.5s;
  }

  .bang {
    width: 144px;
    height: 144px;
    background: var(--accent);
    border-radius: 50%;
    animation: grow 1s;
  }

  svg {
    transition: 0.2s;
  }

  a > svg {
    width: 20px;
    animation: wipe 0.5s;
  }

  a > svg:hover {
    fill: var(--accent);
  }

  img {
    width: 100%;
    animation: spin 5s 0.5s infinite linear;
  }

  @keyframes turn {
    0% {
      transform: rotateX(45deg);
    }
    100% {
      transform: rotateX(0deg);
    }
  }

  @keyframes wipe {
    0% {
      transform: translateY(48px);
    }
    100% {
      transform: translateY(0px);
    }
  }

  @keyframes grow {
    0% {
      transform: scale(0);
    }
    50% {
      transform: scale(0);
    }
    100% {
      transform: scale(1);
    }
  }

  @keyframes spin {
    0% {
      transform: rotateZ(0deg);
    }
    100% {
      transform: rotateZ(360deg);
    }
  }

  @media screen and (max-width: 1200px) {
    main {
      flex-direction: column;
    }

    .splash {
      width: 100%;
      height: 50%;
    }
  }

  @media screen and (max-width: 800px) {
      
    .content {
      width: auto;
      height: 50%;
      margin: 0 80px;
    }
  }

  @media screen and (max-width: 600px) {
    
    .splash {
      height: 100%;
    }
      
    .content {
      width: auto;
      height: auto;
      margin: 80px 80px;
    }
  }
</style>
