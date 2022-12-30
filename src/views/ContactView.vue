<script setup>
import WordSphere from 'wordsphere';

</script>

<template>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Raleway:wght@100;300;500&display=swap" rel="stylesheet">
  <main>
    <div class="contact_content">
      <div class="email_me">
        <div class="email_header">
          Get in touch
        </div>
        <a href="mailto:dylan@dylanstevens.ca">
        <div class="mail_icon mail">
            <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24"><path d="M0 3v18h24v-18h-24zm6.623 7.929l-4.623 5.712v-9.458l4.623 3.746zm-4.141-5.929h19.035l-9.517 7.713-9.518-7.713zm5.694 7.188l3.824 3.099 3.83-3.104 5.612 6.817h-18.779l5.513-6.812zm9.208-1.264l4.616-3.741v9.348l-4.616-5.607z"/></svg>
            <p class="email_text">
              Email Me
            </p>
        </div>
        </a>
      </div>
      <div class="word_sphere">
        <WordSphere
        :items_list="['Vue', 'Python', 'React', 'Java', 'C/C++', 'SQL Databases', 'Azure', 'React Native', 'REST APIs', 'Git', 'Bash']"
        :text_color="'#000000'"
        :update_interval="10"
        :radius="12"
        />
      </div>
      <div class="contact_desc">
        <div class="email_desc">
          Please reach out with any questions or inquiries
        </div>
        <div class="my_email">
          dylan@dylanstevens.ca
        </div>
      </div>
    </div>
  </main>
</template>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Raleway:wght@100;300;500&display=swap');
  .mail_icon {
        background-color: white;
        margin: 20px;
        width: 120px;
        height: 80px;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 50px;
        fill: rgb(32, 37, 46);
        box-shadow: 0 0 20px 0 rgba(25, 25, 25, 0.35);
        transition: 0.3s;
    }

    .mail_icon.mail:hover {
      fill: #3b9892;
      box-shadow: 0 0 24px 0 #3b9892;
      transition: 0.3s;
      width: 200px;
    }

    a {
      text-decoration: none;
    }

    .email_text {
      text-decoration: none;
      font-family: 'Raleway', sans-serif;
      font-weight: 500;
      color:black;
      font-size: 0%;
      transition: 1s;
      margin-left: 0px;
    }

    .mail_icon.mail:hover .email_text{
      transition: 1s;
      font-size: 18px;
      margin-left: 10px;
    }

    main {
      height: 100%;
    }

    .contact_content {
      display: flex;
      justify-content:space-between;
      flex-direction: row;
      height: 100%;
        -webkit-animation: fadeIn2 4s; /* Safari, Chrome and Opera > 12.1 */
        -moz-animation: fadeIn2 4s; /* Firefox < 16 */
        -ms-animation: fadeIn2 4s; /* Internet Explorer */
        -o-animation: fadeIn2 4s; /* Opera < 12.1 */
        animation: fadeIn2 4s;
    }

    @media only screen and (max-width: 960px) {
    .contact_content {
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
    }



    .email_header {
        font-family: 'Raleway', sans-serif;
        font-size: 48px;
        font-weight: 200;
        color: black;
        text-align: center;
    }

    @media only screen and (max-width: 960px) {
    .email_header {
      font-size: 48px;
      margin-top: 20px;
    }
    }

    @media only screen and (max-width: 768px) {
    .email_header {
      font-size: 36px;
      margin-top: 20px;
    }
    }

    .email_desc {
        font-family: 'Raleway', sans-serif;
        font-size: 36px;
        font-weight: 100;
        color: black;
        padding: 10px;
    }

    @media only screen and (max-width: 768px) {
    .email_desc {
      font-size: 24px;
    }
    }
    

    .my_email {
        font-family: 'Raleway', sans-serif;
        font-size: 18px;
        font-weight: 300;
        color: black;
        padding: 10px;
    }

    @keyframes fadeIn2 {
        from { opacity: 0; }
        to   { opacity: 1; }
    }

    /* Firefox < 16 */
    @-moz-keyframes fadeIn2 {
        from { opacity: 0; }
        to   { opacity: 1; }
    }

    /* Safari, Chrome and Opera > 12.1 */
    @-webkit-keyframes fadeIn2 {
        from { opacity: 0; }
        to   { opacity: 1; }
    }

    /* Internet Explorer */
    @-ms-keyframes fadeIn2 {
        from { opacity: 0; }
        to   { opacity: 1; }
    }

    /* Opera < 12.1 */
    @-o-keyframes fadeIn2 {
        from { opacity: 0; }
        to   { opacity: 1; }
    }

    .email_me {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      width: 400px;
    }

    @media only screen and (max-width: 768px) {
    .email_me {
      width: 300px;
    }
    }


    .contact_desc {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      width: 400px;
    }

    @media only screen and (max-width: 768px) {
    .contact_desc {
      width: 300px;
    }
    }

    .word_sphere {
      transform: scale(0.8);
      position: relative;
      max-height: 500px;
      background-size: contain;
    }

    @media only screen and (max-width: 1100px) {
      .word_sphere {
      transform: scale(0.7);
      max-width: 70%;
    }
    }

    @media only screen and (max-width: 1000px) {
      .word_sphere {
      transform: scale(0.55);
      max-width:55%;
    }
    }

    @media only screen and (max-width: 960px) {
      .word_sphere {
      transform: scale(0.7);
      max-width:100%;
    }
    }


    @media only screen and (max-width: 768px) {
      .word_sphere {
      transform: scale(0.55);
      max-width: 500%;
      max-height: 100%;
    }
    }


</style>
