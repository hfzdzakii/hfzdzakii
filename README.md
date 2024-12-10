<!-- ## Hi there 👋 -->

<div align="center">
  <h1>
    <span id="typing"></span>
  </h1>
</div>

<script>
  const phrases = ["Hello", "World", "How are you"];
  let i = 0;
  let j = 0;
  let isDeleting = false;
  const speed = 150; // Typing speed
  const delay = 1000; // Delay before typing next phrase
  
  function typeEffect() {
    const target = document.getElementById("typing");

    if (i < phrases.length) {
      const currentPhrase = phrases[i];

      if (!isDeleting) {
        target.innerHTML = currentPhrase.substring(0, j + 1);
        j++;

        if (j === currentPhrase.length) {
          isDeleting = true;
          setTimeout(typeEffect, delay);
          return;
        }
      } else {
        target.innerHTML = currentPhrase.substring(0, j - 1);
        j--;

        if (j === 0) {
          isDeleting = false;
          i++;
          if (i === phrases.length) {
            i = 0; // Loop back to the first phrase
          }
        }
      }
    }
    setTimeout(typeEffect, speed);
  }

  document.addEventListener("DOMContentLoaded", typeEffect);
</script>


<!--
**hfzdzakii/hfzdzakii** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
