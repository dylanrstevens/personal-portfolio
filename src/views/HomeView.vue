<script setup>
</script>

<template>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Raleway:wght@100;300&display=swap" rel="stylesheet">
  <main>
    <div class="body_content">
      <div class="links">
          <div class="social_icon github">
              <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
          </div>
          <div class="social_icon linkedin">
              <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
          </div>
      </div>
      <div class="photo_and_text">
          <div class="items">
              <div class="photo">
                  <transition name="slide1" appear>
                      <img src="../assets/faceshot2.png" alt="My image">
                  </transition>
              </div>

              <div class="paragraphs">
                  <transition name="slide2" appear>
                      <div class="name_header">
                          <p>
                              Software, design, technology.
                          </p>
                      </div>
                  </transition>
                  
                  <transition name="slide3" appear>
                      <div class="desc">
                          <p>
                              Hi! My name is Dylan Stevens. Thanks for checking out my portfolio.
                          </p>
                      </div>
                  </transition>
              </div>
          </div>
      </div>
    </div>
  </main>
</template>

<style> 
  @import url('https://fonts.googleapis.com/css2?family=Raleway:wght@100;300&display=swap');
  main {
    height: 100%;
  }

  .body_content {
    display: flex;
    flex-direction: row;
    height: 100%;
  }

  @media screen and (max-width: 800px) {
  .body_content {
    display: flex;
    flex-direction: column-reverse;
    height: 100%;
  }
  }

  .social_icon {
      background-color: white;
      margin: 20px;
      width: 80px;
      height: 80px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 50px;
      fill: rgb(32, 37, 46);
      box-shadow: 0 0 20px 0 rgba(25, 25, 25, 0.35);
      transition: 0.3s;
  }

  .social_icon.linkedin:hover {
      fill: #3b5998;
      box-shadow: 0 0 24px 0 #3b5998;
      transition: 0.3s;
  }

  .social_icon.github:hover {
      fill: #6d3b98;
      box-shadow: 0 0 24px 0 #6d3b98;
      transition: 0.3s;
  }

  .links {
      background: rgb(240, 240, 240);
      display: flex;
      flex-direction: column;
      justify-content: center;
  }


  @media screen and (max-width: 800px) {
  .links {
      display: flex;
      flex-direction: row;
  }
  }

  img {
        height: 350px;
        width: 350px;
    }

    @media screen and (max-width: 1000px) {
    img {
        height: 250px;
        width: 250px;
    }
    }

    @media screen and (max-width: 390px) {
    img {
        height: 150px;
        width: 150px;
    }
    }

    .items {
        overflow: hidden;
        display: flex;
        flex-direction: row;
        align-items: center;
    }
    .photo_and_text {
        flex: 1; 
        display: flex;
        justify-content: center;
        background: url("../assets/graph.png") 50% 0% no-repeat fixed;
        -webkit-animation: fadein 4s; /* Safari, Chrome and Opera > 12.1 */
        -moz-animation: fadein 4s; /* Firefox < 16 */
        -ms-animation: fadein 4s; /* Internet Explorer */
        -o-animation: fadein 4s; /* Opera < 12.1 */
        animation: fadein 4s;
    }

    @keyframes fadein {
        from { opacity: 0; }
        to   { opacity: 1; }
    }

    /* Firefox < 16 */
    @-moz-keyframes fadein {
        from { opacity: 0; }
        to   { opacity: 1; }
    }

    /* Safari, Chrome and Opera > 12.1 */
    @-webkit-keyframes fadein {
        from { opacity: 0; }
        to   { opacity: 1; }
    }

    /* Internet Explorer */
    @-ms-keyframes fadein {
        from { opacity: 0; }
        to   { opacity: 1; }
    }

    /* Opera < 12.1 */
    @-o-keyframes fadein {
        from { opacity: 0; }
        to   { opacity: 1; }
    }
    
    .photo {
        width: 450px;
        text-align: center;
        margin: 10px;
    }

    @media screen and (max-width: 1000px) {
    .photo {
        width: 300px;
        text-align: center;
    }
    }

    .paragraphs {
        width: 350px;
        text-align: center;
        margin: 10px;
    }

    .name_header {
        font-family: 'Raleway', sans-serif;
        font-size: 48px;
        font-weight: 200;
        color: black;
    }

    @media screen and (max-width: 700px) {
    .name_header {
        font-size: 36px;
    }
    }

    @media screen and (max-width: 390px) {
    .name_header {
        font-size: 24px;
    }
    }

    .desc {
        font-family: 'Raleway', sans-serif;
        font-weight: 300;
        color: black;
        font-size: 20px;
    }

    @media screen and (max-width: 600px) {
    .desc {
        font-size: 16px;
    }
    }

    @media screen and (max-width: 390px) {
    .desc {
        font-size: 12px;
    }
    }
    
    .slide1-enter-from {
        transform: translateY(20px);
    }

    .slide1-enter-active {
        transition: all 2s ease;
    }

    .slide2-enter-from {
        transform: translateX(30px);
        
    }

    .slide2-enter-active {
        transition: all 2s ease;
    }

    .slide3-enter-from {
        transform: translateY(50px);
        
    }

    .slide3-enter-active {
        transition: all 2s ease;
    }
</style>