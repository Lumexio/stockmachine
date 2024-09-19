<template>
  <footer>
    <div>
      <h3>Contact:</h3>
      <ul>
        <li>
          <a href="https://github.com/Lumexio" target="_blank">
            <FontAwesomeIcon size="2x" :icon="faGithubAlt" />
          </a>
          <a href="https://www.linkedin.com/in/francisco-salazar-mendoza/" target="_blank">
            <FontAwesomeIcon size="2x" :icon="faLinkedin" />
          </a>
        </li>
      </ul>
    </div>
    <div>
      <h3>Powered By:</h3>
      <ul>
        <li>
          <a href="https://svelte.com">
            <Icon icon="ri:svelte-fill" width='2rem' height="2rem" />
          </a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<script setup>
import { Icon } from '@iconify/vue';
import { faGithubAlt, faLinkedin } from '@fortawesome/free-brands-svg-icons';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
</script>
