<template>
  <div class="featured">
    <div class='card-title'>
      <h2>Download the latest version!</h2>
    </div>
    <div class='card-actions'>
      <button class='button-accent' @click="handleDownload('windows')">
        <FontAwesomeIcon size='2x' :icon='faDownload' />
        <h3>Windows 1.0.0 version</h3>
      </button>
      <button class="button-accent" @click="handleDownload('linux')">
        <FontAwesomeIcon size='2x' :icon='faDownload' />
        <h3>Linux 1.0.0 version</h3>
      </button>
    </div>
  </div>
</template>

<script setup>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { faDownload } from '@fortawesome/free-solid-svg-icons';

function downloadFile(url, filename) {
  const link = document.createElement('a');
  link.href = url;
  link.download = filename;
  document.body.appendChild(link);
  link.click();
  document.body.removeChild(link);
}
function downloadFileDirect(url) {
  window.open(url, '_blank');
}

function handleDownload(os) {
  let path = '/todownload/';
  let fileName = '';

  if (os === 'windows') {
    fileName = 'STOCKMACHINE-1.0.0 Setup.exe';
    downloadFileDirect('https://drive.google.com/file/d/1gwdSMtp-WZ3bszkH6BmHBqSMitV_aLix/view?usp=sharing');
  } else {
    fileName = 'stockmachine_1.0.0_amd64.deb';
    downloadFile(`${path}${fileName}`, fileName);
  }


}
</script>

<style>
/* Add your styles here */
</style>
