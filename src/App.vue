<template>

  <div class="main-container">
    <div class="sidebar-container">
      <div class="icon-container tooltip "  @click="toggleSidebar('linked assets')" :class="{ 'selected': selectedContainer == 'linked assets' }">
        <span class="tooltiptext">Linked assets</span>
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" height="34" width="34"
          color="neutral600" name="navConnectedAssets">
          <path class="icon-path" fill="#2D2E2E" fill-rule="evenodd"
            d="M17 11a4 4 0 1 0 0-8 4 4 0 0 0 0 8Zm0-2a2 2 0 1 0 0-4 2 2 0 0 0 0 4ZM17 21a4 4 0 1 0 0-8 4 4 0 0 0 0 8Zm0-2a2 2 0 1 0 0-4 2 2 0 0 0 0 4ZM7 11a4 4 0 1 0 0-8 4 4 0 0 0 0 8Zm0-2a2 2 0 1 0 0-4 2 2 0 0 0 0 4ZM10.452 14.978a4 4 0 1 1-1.41-1.418l3.419-3.42 1.414 1.415-3.423 3.423ZM9 17a2 2 0 1 1-4 0 2 2 0 0 1 4 0Z"
            clip-rule="evenodd">
          </path>
        </svg>
      </div>
      <div class="icon-container tooltip"  @click="toggleSidebar('Details')"  :class="{ 'selected': selectedContainer == 'Details' }">
        <span class="tooltiptext">Details</span>
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" height="34" width="34" size="24"
          color="neutral600" name="actionZapDetails">
          <path class="icon-path" fill="#2D2E2E" d="M20 8V6.59L15.41 2H4v20h16V10h-2v10H6V4h8v4h6Z"></path>
          <path class="icon-path" fill="#2D2E2E" d="m10.75 18.858 4.809-5.729H13.25V9.067l-4.808 5.729h2.308v4.062Z">
          </path>
        </svg>
      </div>
      <div class="icon-container" @click="toggleSidebar('notes')" :class="{ 'selected': selectedContainer == 'notes' }">
        <span class="tooltiptext">Notes</span>
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" height="34" width="34" size="24"
          color="neutral600" name="commentBlank">
          <path class="icon-path" fill="#2D2E2E" d="M10 16H4V4h16v12h-5.47L9.5 22h2.61l3.36-4H22V2H2v16h8v-2Z"></path>
        </svg>
      </div>
      <div class="icon-container" @click="toggleSidebar('change History')" :class="{ 'selected': selectedContainer == 'change History' }">
        <span class="tooltiptext">Change Histroy</span>
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" height="34" width="34" size="24"
          color="neutral600" name="actionCalendar">
          <path class="icon-path" fill="#2D2E2E" d="M17 4V2h-2v2H9V2H7v2H3v2h4v2h2V6h6v2h2V6h2v13H5V7.5H3V21h18V4h-4Z">
          </path>
          <path class="icon-path" fill="#2D2E2E"
            d="M8 12.25a1.25 1.25 0 1 0 0-2.5 1.25 1.25 0 0 0 0 2.5ZM12 12.25a1.25 1.25 0 1 0 0-2.5 1.25 1.25 0 0 0 0 2.5ZM16 12.25a1.25 1.25 0 1 0 0-2.5 1.25 1.25 0 0 0 0 2.5ZM8 17.25a1.25 1.25 0 1 0 0-2.5 1.25 1.25 0 0 0 0 2.5ZM12 17.25a1.25 1.25 0 1 0 0-2.5 1.25 1.25 0 0 0 0 2.5ZM16 17.25a1.25 1.25 0 1 0 0-2.5 1.25 1.25 0 0 0 0 2.5Z">
          </path>
        </svg>
      </div>
      <div class="icon-container" @click="toggleSidebar('zap runs')" :class="{ 'selected': selectedContainer == 'zap runs' }">
        <span class="tooltiptext">Zap run</span>
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" height="34" width="34" size="24"
          color="neutral600" name="miscClock">
          <path class="icon-path" fill="#2D2E2E"
            d="M12 2a10 10 0 1 0 0 20 10 10 0 0 0 0-20Zm0 18a8 8 0 1 1 0-16 8 8 0 0 1 0 16Zm-1-8.47-3.22 2.7 1.29 1.54 3.93-3.3V7h-2v4.53Z">
          </path>
        </svg>
      </div>
      <div class="icon-container" @click="toggleSidebar('setting')" :class="{ 'selected': selectedContainer == 'setting' }">
        <span class="tooltiptext">Status</span>
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" height="34" width="34" size="24"
          color="neutral600" name="statusStatus">
          <path class="icon-path" fill="#2D2E2E" fill-rule="evenodd"
            d="M12 2C6.477 2 2 6.477 2 12s4.477 10 10 10 10-4.477 10-10S17.523 2 12 2Zm-7.9 8.735a8 8 0 1 1-.066 2h4.211l1.665-2.69 3.824 7.597 2.71-4.907h1.814v-2h-2.993l-1.449 2.623-3.726-7.404-2.959 4.781H4.099Z"
            clip-rule="evenodd"></path>
        </svg>
      </div>
      <div class="icon-container" @click="toggleSidebar('versions')" :class="{ 'selected': selectedContainer == 'versions' }">
        <span class="tooltiptext">Advanced Setting</span>
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" height="34" width="34" size="24"
          color="neutral600" name="navCog">
          <path class="icon-path" fill="#2D2E2E"
            d="M19.9 8.9a2.516 2.516 0 0 1-1.26-2.18l.01-2.42-3.29-1.9-2.09 1.22c-.78.45-1.74.45-2.52 0l-2.1-1.23-3.29 1.9.01 2.42c0 .9-.48 1.73-1.26 2.18L2 10.1v3.81l2.1 1.2c.78.45 1.26 1.28 1.26 2.18l-.01 1.63 2.01-1.18v-.44c.01-1.62-.86-3.12-2.27-3.93L4 12.74v-1.48l1.1-.63c1.41-.8 2.28-2.31 2.27-3.93V5.44l1.27-.74 1.09.64c1.4.82 3.14.82 4.54 0l1.09-.64 1.28.74V6.7c-.01 1.62.86 3.12 2.27 3.93l1.1.63v1.48l-1.1.63c-1.41.8-2.28 2.31-2.27 3.93v1.26l-1.28.74-1.09-.64a4.47 4.47 0 0 0-2.27-.61c-.79 0-1.57.2-2.27.61l-3.07 1.8 1.99 1.15 2.09-1.22a2.52 2.52 0 0 1 2.52 0l2.09 1.22 3.29-1.9-.01-2.42c0-.9.48-1.73 1.26-2.18l2.1-1.2V10.1L19.9 8.9Z">
          </path>
          <path class="icon-path" fill="#2D2E2E"
            d="M12 16.5c2.48 0 4.5-2.02 4.5-4.5S14.48 7.5 12 7.5 7.5 9.52 7.5 12s2.02 4.5 4.5 4.5Zm0-7a2.5 2.5 0 0 1 0 5 2.5 2.5 0 0 1 0-5Z">
          </path>
        </svg>
      </div>
      <div class="icon-container"  @click="toggleSidebar('help')"  :class="{ 'selected': selectedContainer == 'help' }">
        <span class="tooltiptext">Versions</span>
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" height="34" width="34" size="24"
          color="neutral600" name="navVersions">
          <path class="icon-path" fill="#2D2E2E" d="M6 2h12v2H6V2ZM4 6h16v2H4V6ZM3 10v8h2v-6h14v8H3v2h18V10H3Z"></path>
        </svg>
      </div>
      <div class="icon-container"  @click="toggleSidebar('question')"  :class="{ 'selected': selectedContainer == 'question' }">
        <span class="tooltiptext">Help</span>
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" height="34" width="34" size="24"
          color="neutral600" name="navHelp">
          <path class="icon-path" fill="#2D2E2E"
            d="M12 2C6.49 2 2 6.49 2 12s4.49 10 10 10 10-4.49 10-10S17.51 2 12 2Zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8Z">
          </path>
          <path class="icon-path" fill="#2D2E2E"
            d="M12.01 18.25a1.25 1.25 0 1 0 0-2.5 1.25 1.25 0 0 0 0 2.5ZM12.36 6.13c-1.18-.01-2.19.3-2.98.67v1.98c.62-.4 1.65-.9 2.92-.9h.05c1.3.01 2.07.72 2.14 1.38.08.88-.96 1.67-2.65 2.01l-.7.14.01 3.08h1.75v-1.68c2.64-.76 3.47-2.38 3.34-3.73-.18-1.68-1.81-2.93-3.88-2.95Z">
          </path>
        </svg>
      </div>
      <div class="icon-container sidebar-icon" @click="toggleSidebar('sidebar')"  :class="{ 'selected': selectedContainer == 'sidebar' }"  >
        <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
          x="0px" y="0px" viewBox="0 0 120.49 122.88" style="enable-background:new 0 0 120.49 122.88"
          xml:space="preserve" height="30" width="30" size="24">

          <g>
            <path fill="#2D2E2E"
              d="M33.76,62.78h-0.98c0-8.04-3.01-15.06-9.01-21.07c-6-6-13.03-9.01-21.07-9.01v-0.98 c8.04,0,15.07-3.01,21.07-9.02c6-6.03,9.01-13.06,9.01-21.07h0.98c0,8.04,3.01,15.07,9.01,21.07c6,6,13.03,9.01,21.07,9.01v0.98 c-8.04,0-15.07,3.01-21.07,9.01C36.77,47.72,33.76,54.74,33.76,62.78L33.76,62.78L33.76,62.78z M15.89,99.59h-0.45 c0-3.68-1.38-6.91-4.14-9.66c-2.75-2.75-5.98-4.14-9.66-4.14v-0.45c3.68,0,6.91-1.38,9.66-4.14c2.75-2.76,4.14-5.98,4.14-9.65h0.45 c0,3.68,1.38,6.91,4.14,9.66c2.75,2.75,5.97,4.14,9.66,4.14v0.45c-3.68,0-6.91,1.38-9.66,4.14C17.26,92.68,15.89,95.91,15.89,99.59 L15.89,99.59L15.89,99.59z M62.44,121.24h-0.45c0-3.68-1.38-6.91-4.14-9.66c-2.75-2.75-5.97-4.14-9.66-4.14v-0.45 c3.68,0,6.91-1.38,9.66-4.14c2.75-2.76,4.14-5.98,4.14-9.65h0.45c0,3.68,1.38,6.91,4.14,9.66c2.75,2.75,5.97,4.14,9.66,4.14v0.45 c-3.68,0-6.91,1.38-9.66,4.14C63.82,114.33,62.44,117.55,62.44,121.24L62.44,121.24L62.44,121.24z M93.6,87.19h-0.82 c0-6.74-2.52-12.64-7.56-17.68c-5.04-5.04-10.93-7.56-17.68-7.56v-0.82c6.74,0,12.64-2.52,17.68-7.57 c5.04-5.05,7.56-10.95,7.56-17.67h0.82c0,6.74,2.52,12.64,7.56,17.68c5.04,5.04,10.93,7.56,17.68,7.56v0.82 c-6.74,0-12.64,2.52-17.68,7.56C96.13,74.55,93.6,80.45,93.6,87.19L93.6,87.19L93.6,87.19z" />
            <path fill="#2D2E2E"
              d="M33.76,64.42h-0.98c-0.9,0-1.64-0.73-1.64-1.64c0-3.8-0.71-7.36-2.12-10.66c-1.42-3.31-3.55-6.4-6.41-9.25 l-0.08-0.09c-2.83-2.81-5.89-4.92-9.17-6.33c-3.3-1.41-6.86-2.12-10.66-2.12c-0.9,0-1.64-0.73-1.64-1.64v-0.98 c0-0.9,0.73-1.64,1.64-1.64c3.8,0,7.36-0.71,10.66-2.12c3.32-1.42,6.4-3.56,9.25-6.41c2.85-2.87,4.99-5.96,6.41-9.28 c1.41-3.3,2.12-6.85,2.12-10.63c0-0.9,0.73-1.64,1.64-1.64h0.98c0.9,0,1.64,0.73,1.64,1.64c0,3.8,0.71,7.36,2.12,10.66 c1.42,3.31,3.55,6.4,6.41,9.25c2.86,2.86,5.94,5,9.25,6.41c3.3,1.41,6.85,2.12,10.66,2.12c0.9,0,1.64,0.73,1.64,1.64v0.98 c0,0.9-0.73,1.64-1.64,1.64c-3.8,0-7.36,0.71-10.66,2.12c-3.31,1.42-6.4,3.55-9.25,6.41l-0.08,0.08c-2.81,2.84-4.92,5.9-6.33,9.19 c-1.41,3.3-2.12,6.86-2.12,10.66C35.4,63.69,34.66,64.42,33.76,64.42L33.76,64.42z M32.03,50.85c0.49,1.14,0.9,2.31,1.24,3.5 c0.34-1.19,0.75-2.36,1.24-3.51c1.57-3.67,3.91-7.08,7.02-10.21l0.09-0.09c3.15-3.15,6.58-5.51,10.29-7.1 c1.14-0.49,2.31-0.9,3.5-1.24c-1.19-0.34-2.36-0.75-3.5-1.24c-3.71-1.59-7.14-3.96-10.29-7.1s-5.51-6.58-7.1-10.29 c-0.49-1.15-0.91-2.32-1.25-3.52c-0.34,1.19-0.75,2.35-1.24,3.49c-1.58,3.7-3.95,7.14-7.1,10.31c-3.15,3.16-6.58,5.53-10.29,7.12 c-1.15,0.49-2.32,0.91-3.51,1.24c1.19,0.34,2.36,0.75,3.51,1.24c3.67,1.57,7.07,3.91,10.2,7.02l0.09,0.09 C28.07,43.7,30.44,47.14,32.03,50.85L32.03,50.85z M15.89,101.23h-0.45c-0.9,0-1.64-0.73-1.64-1.64c0-1.62-0.3-3.14-0.9-4.54 c-0.6-1.41-1.52-2.74-2.76-3.97c-1.23-1.23-2.56-2.15-3.97-2.76c-1.4-0.6-2.92-0.9-4.54-0.9C0.73,87.43,0,86.7,0,85.79v-0.45 c0-0.9,0.73-1.64,1.64-1.64c1.62,0,3.14-0.3,4.54-0.9c1.41-0.6,2.73-1.52,3.97-2.76l0.08-0.08c1.19-1.21,2.08-2.51,2.68-3.9 c0.6-1.4,0.9-2.91,0.9-4.53c0-0.9,0.73-1.64,1.64-1.64h0.45c0.9,0,1.64,0.73,1.64,1.64c0,1.62,0.3,3.14,0.9,4.54 c0.6,1.41,1.52,2.73,2.75,3.97s2.55,2.15,3.96,2.76c1.4,0.6,2.92,0.9,4.54,0.9c0.9,0,1.64,0.73,1.64,1.64v0.45 c0,0.9-0.73,1.64-1.64,1.64c-1.62,0-3.14,0.3-4.54,0.9c-1.41,0.6-2.73,1.52-3.97,2.76l-0.09,0.08c-1.19,1.2-2.08,2.49-2.67,3.87 c-0.6,1.4-0.9,2.92-0.9,4.55C17.53,100.49,16.79,101.23,15.89,101.23L15.89,101.23z M12.46,88.77c1.37,1.37,2.44,2.86,3.2,4.47 c0.75-1.57,1.79-3.02,3.13-4.37l0.08-0.09c1.37-1.37,2.86-2.44,4.47-3.2c-1.61-0.77-3.1-1.84-4.47-3.21 c-1.37-1.37-2.44-2.87-3.21-4.48c-0.75,1.56-1.79,3.02-3.11,4.37l-0.09,0.1c-1.37,1.37-2.86,2.44-4.47,3.21 C9.59,86.33,11.09,87.4,12.46,88.77L12.46,88.77z M62.44,122.88h-0.45c-0.9,0-1.64-0.73-1.64-1.64c0-1.62-0.3-3.14-0.9-4.54 c-0.6-1.41-1.52-2.73-2.76-3.97l-0.08-0.08c-1.21-1.19-2.5-2.08-3.89-2.67c-1.4-0.6-2.92-0.9-4.54-0.9c-0.9,0-1.64-0.73-1.64-1.64 v-0.45c0-0.9,0.73-1.64,1.64-1.64c1.62,0,3.14-0.3,4.54-0.9c1.41-0.6,2.74-1.52,3.97-2.76l0.08-0.08c1.19-1.21,2.08-2.51,2.68-3.9 c0.6-1.4,0.9-2.91,0.9-4.53c0-0.9,0.73-1.64,1.64-1.64h0.45c0.9,0,1.64,0.73,1.64,1.64c0,1.62,0.3,3.14,0.9,4.54 c0.6,1.41,1.52,2.73,2.75,3.97c1.23,1.23,2.55,2.15,3.96,2.76c1.4,0.6,2.92,0.9,4.54,0.9c0.9,0,1.64,0.73,1.64,1.64v0.45 c0,0.9-0.73,1.64-1.64,1.64c-1.62,0-3.14,0.3-4.54,0.9c-1.41,0.6-2.73,1.52-3.97,2.76l-0.09,0.08c-1.19,1.2-2.08,2.49-2.67,3.87 c-0.6,1.4-0.9,2.91-0.9,4.54C64.08,122.15,63.35,122.88,62.44,122.88L62.44,122.88z M59.01,110.42c1.37,1.37,2.44,2.86,3.2,4.47 c0.75-1.57,1.79-3.02,3.13-4.37l0.08-0.09c1.37-1.37,2.86-2.44,4.47-3.2c-1.61-0.77-3.1-1.84-4.47-3.21 c-1.37-1.37-2.44-2.87-3.21-4.48c-0.75,1.56-1.79,3.02-3.11,4.37l-0.09,0.1c-1.37,1.37-2.86,2.44-4.47,3.2 c1.57,0.75,3.03,1.79,4.37,3.12L59.01,110.42L59.01,110.42z M93.6,88.82h-0.82c-0.9,0-1.64-0.73-1.64-1.64 c0-3.15-0.59-6.1-1.76-8.84c-1.17-2.75-2.95-5.31-5.33-7.69c-2.38-2.38-4.94-4.15-7.68-5.33c-2.73-1.17-5.68-1.76-8.84-1.76 c-0.9,0-1.64-0.73-1.64-1.64v-0.82c0-0.9,0.73-1.64,1.64-1.64c3.16,0,6.1-0.59,8.84-1.76c2.75-1.18,5.31-2.96,7.68-5.33 c2.37-2.38,4.15-4.95,5.33-7.7c1.17-2.74,1.76-5.68,1.76-8.82c0-0.9,0.73-1.64,1.64-1.64h0.82c0.9,0,1.64,0.73,1.64,1.64 c0,3.15,0.59,6.1,1.76,8.84c1.18,2.75,2.95,5.32,5.32,7.69c2.37,2.37,4.93,4.15,7.69,5.32c2.74,1.17,5.68,1.76,8.84,1.76 c0.9,0,1.64,0.73,1.64,1.64v0.82c0,0.9-0.73,1.64-1.64,1.64c-3.15,0-6.1,0.59-8.84,1.76c-2.75,1.18-5.32,2.95-7.69,5.32 c-2.37,2.38-4.15,4.94-5.32,7.69c-1.17,2.74-1.76,5.68-1.76,8.84C95.24,88.09,94.51,88.82,93.6,88.82L93.6,88.82z M92.39,77.07 c0.3,0.7,0.57,1.42,0.8,2.14c0.23-0.72,0.5-1.44,0.8-2.14c1.35-3.15,3.35-6.06,6.02-8.72c2.68-2.67,5.58-4.67,8.72-6.02 c0.7-0.3,1.41-0.57,2.14-0.8c-0.72-0.23-1.44-0.5-2.14-0.8c-3.14-1.34-6.04-3.35-8.71-6.02l-0.01-0.01 c-2.67-2.67-4.67-5.57-6.02-8.71c-0.3-0.7-0.57-1.42-0.8-2.15c-0.23,0.72-0.5,1.43-0.8,2.13c-1.34,3.14-3.35,6.05-6.02,8.72 c-2.67,2.68-5.58,4.69-8.72,6.03c-0.7,0.3-1.42,0.57-2.14,0.8c0.72,0.23,1.44,0.5,2.14,0.8c3.15,1.35,6.05,3.35,8.72,6.02 C89.04,71.01,91.05,73.92,92.39,77.07L92.39,77.07z" />
          </g>
        </svg>
      </div>
    </div>

      <div class="sidebar" v-if="isVisible">

        <div class="header">
          <div class="header-body">
            <div style="display:flex; align-items:center">
              <span> Copilot </span>
              <div class="badge"> Beta</div>
            </div>
            <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"  height="30" width="30" size="24"
              viewBox="0 0 122.878 122.88" enable-background="new 0 0 122.878 122.88" xml:space="preserve" @click="toggleSidebar('cross')">
              <g>
                <path
                  d="M1.426,8.313c-1.901-1.901-1.901-4.984,0-6.886c1.901-1.902,4.984-1.902,6.886,0l53.127,53.127l53.127-53.127 c1.901-1.902,4.984-1.902,6.887,0c1.901,1.901,1.901,4.985,0,6.886L68.324,61.439l53.128,53.128c1.901,1.901,1.901,4.984,0,6.886 c-1.902,1.902-4.985,1.902-6.887,0L61.438,68.326L8.312,121.453c-1.901,1.902-4.984,1.902-6.886,0 c-1.901-1.901-1.901-4.984,0-6.886l53.127-53.128L1.426,8.313L1.426,8.313z" />
              </g>
            </svg>

          </div>

          <div class="para">
            Powered by AI
          </div>
        </div>


        <div class="main-body">

          <div class="sidebar-body">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" height="40" width="40" size="24"
              color="neutral600" name="navHelp" class="svg">
              <path class="icon-path" fill="#2D2E2E"
                d="M12 2C6.49 2 2 6.49 2 12s4.49 10 10 10 10-4.49 10-10S17.51 2 12 2Zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8Z">
              </path>
              <path class="icon-path" fill="#2D2E2E"
                d="M12.01 18.25a1.25 1.25 0 1 0 0-2.5 1.25 1.25 0 0 0 0 2.5ZM12.36 6.13c-1.18-.01-2.19.3-2.98.67v1.98c.62-.4 1.65-.9 2.92-.9h.05c1.3.01 2.07.72 2.14 1.38.08.88-.96 1.67-2.65 2.01l-.7.14.01 3.08h1.75v-1.68c2.64-.76 3.47-2.38 3.34-3.73-.18-1.68-1.81-2.93-3.88-2.95Z">
              </path>
            </svg>
            <span class="span1">Copilot</span>
            <div class="time">2 minutes ago</div>
          </div>

          <div>
            <div class="paras">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Repellat, iusto minima ad,
            </div>
            <div class="paras">Here is a list of consectetur adipisicing elit. Repellat, iusto minima ad: </div>
            <div class="paras">
              <ul>
                <li>Lorem, ipsum dolor sit amet consectetur.</li>
                <li>Lorem, ipsum dolor sit amet consectetur.</li>
                <li>Lorem, ipsum dolor sit amet consectetur.</li>
                <li>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</li>
                <li>Lorem, ipsum dolor sit amet consectetur.</li>
              </ul>
            </div>
          </div>
          <a href="#">Learn more about chatbot</a>
        </div>


        <div class="textarea-div">
          <textarea >
         </textarea>
          <div class="icons">
            <div class="three-icons">
              <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" height="40" width="40" size="24"
                viewBox="0 0 115.031 122.88" enable-background="new 0 0 115.031 122.88" xml:space="preserve">
                <g>
                  <path fill="#c8c5c5"
                    d="M46.097,0.053h41.845c3.675,0,7.14,0.683,10.395,1.995c3.203,1.313,6.144,3.308,8.769,5.933 c2.625,2.625,4.62,5.565,5.933,8.768c1.313,3.203,1.994,6.668,1.994,10.396V67.99c0,3.728-0.682,7.192-1.994,10.396 s-3.308,6.143-5.933,8.768s-5.565,4.568-8.769,5.933c-3.202,1.313-6.667,1.995-10.395,1.995H74.396 c-2.362,2.993-4.936,5.828-7.665,8.4c-3.256,3.045-6.721,5.775-10.448,8.19c-3.728,2.468-7.718,4.62-11.971,6.458 c-4.2,1.838-8.715,3.359-13.44,4.62c-1.365,0.367-2.835-0.053-3.833-1.155c-1.417-1.575-1.26-3.99,0.315-5.408 c2.205-1.942,4.095-3.938,5.618-5.932c1.47-1.943,2.678-3.938,3.57-5.986v-0.052c0.998-2.205,1.891-4.463,2.678-6.721 c0.262-0.787,0.525-1.627,0.788-2.467H27.091c-3.675,0-7.14-0.683-10.396-1.996c-3.203-1.312-6.143-3.307-8.768-5.933 c-2.625-2.625-4.62-5.564-5.933-8.768C0.683,75.078,0,71.613,0,67.938V27.091c0-3.675,0.683-7.141,1.995-10.396 c1.313-3.203,3.308-6.143,5.933-8.768c2.625-2.625,5.565-4.62,8.768-5.933S23.363,0,27.091,0h18.953L46.097,0.053L46.097,0.053z M65.572,31.489c-0.005-0.02,0.141-0.125,0.163-0.139c2.019-1.483,4.854-1.073,6.372,0.92c1.521,1.998,1.156,4.847-0.819,6.395 l-7.53,7.979l-0.014,0.016c2.847,2.532,5.87,5.257,9.555,8.669c0.02-0.005,0.125,0.141,0.139,0.164 c1.483,2.019,1.074,4.853-0.92,6.372c-1.997,1.521-4.847,1.157-6.395-0.819l-8.121-7.771l-7.575,8.725 c-1.367,2.104-4.174,2.718-6.297,1.378c-2.12-1.337-2.777-4.124-1.477-6.266c0.011-0.023,0.104-0.178,0.123-0.175 c3.345-3.693,6.028-6.722,8.537-9.565l-8.521-7.186c-2.105-1.368-2.718-4.174-1.378-6.298c1.337-2.119,4.125-2.777,6.266-1.477 c0.024,0.012,0.178,0.104,0.176,0.123c3.563,3.228,6.508,5.839,9.264,8.271C59.589,38.027,62.257,35.07,65.572,31.489 L65.572,31.489z M68.988,7.718H27.144c-2.73,0-5.25,0.473-7.508,1.418c-2.258,0.945-4.357,2.362-6.248,4.252 c-1.89,1.89-3.307,3.99-4.252,6.248c-0.945,2.258-1.417,4.777-1.417,7.508V67.99c0,2.73,0.473,5.25,1.417,7.508 c0.945,2.258,2.363,4.357,4.252,6.248c1.943,1.89,4.043,3.36,6.301,4.252c2.258,0.945,4.725,1.418,7.455,1.418h17.956 c2.101,0,3.833,1.732,3.833,3.833c0,0.473-0.105,0.893-0.21,1.313c-0.683,2.52-1.417,5.04-2.258,7.455 c-0.893,2.572-1.837,4.987-2.888,7.35c-0.525,1.208-1.155,2.363-1.837,3.57c3.675-1.627,7.14-3.518,10.343-5.617 c3.36-2.205,6.511-4.673,9.398-7.351c2.939-2.73,5.564-5.723,7.979-8.925c0.735-0.998,1.891-1.522,3.046-1.522h15.436 c2.729,0,5.197-0.473,7.455-1.418c2.258-0.944,4.357-2.362,6.301-4.253c1.89-1.89,3.307-3.99,4.252-6.248 c0.945-2.257,1.418-4.777,1.418-7.508V27.249c0-2.73-0.473-5.25-1.418-7.508c-0.945-2.258-2.362-4.358-4.252-6.248 c-1.891-1.89-3.991-3.308-6.248-4.252c-2.258-0.945-4.778-1.417-7.508-1.417H68.988V7.718L68.988,7.718z" />
                </g>
              </svg>

              <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 122.88 104.19"
                style="enable-background:new 0 0 122.88 104.19" xml:space="preserve" height="40" width="40" size="24">
                <g>
                  <path fill="#c8c5c5"
                    d="M62.63,6.25c0.56-2.85,2.03-4.68,4.04-5.61c1.63-0.76,3.54-0.83,5.52-0.31c1.72,0.45,3.53,1.37,5.26,2.69 c4.69,3.57,9.08,10.3,9.64,18.71c0.17,2.59,0.12,5.35-0.12,8.29c-0.16,1.94-0.41,3.98-0.75,6.1h19.95l0.09,0.01 c3.24,0.13,6.38,0.92,9.03,2.3c2.29,1.2,4.22,2.84,5.56,4.88c1.38,2.1,2.13,4.6,2.02,7.46c-0.08,2.12-0.65,4.42-1.81,6.87 c0.66,2.76,0.97,5.72,0.54,8.32c-0.36,2.21-1.22,4.17-2.76,5.63c0.08,3.65-0.41,6.71-1.39,9.36c-1.01,2.72-2.52,4.98-4.46,6.98 c-0.17,1.75-0.45,3.42-0.89,4.98c-0.55,1.96-1.36,3.76-2.49,5.35l0,0c-3.4,4.8-6.12,4.69-10.43,4.51c-0.6-0.02-1.24-0.05-2.24-0.05 l-39.03,0c-3.51,0-6.27-0.51-8.79-1.77c-2.49-1.25-4.62-3.17-6.89-6.01l-0.58-1.66V47.78l1.98-0.53 c5.03-1.36,8.99-5.66,12.07-10.81c3.16-5.3,5.38-11.5,6.9-16.51V6.76L62.63,6.25L62.63,6.25L62.63,6.25z M4,43.02h29.08 c2.2,0,4,1.8,4,4v53.17c0,2.2-1.8,4-4,4l-29.08,0c-2.2,0-4-1.8-4-4V47.02C0,44.82,1.8,43.02,4,43.02L4,43.02L4,43.02z M68.9,5.48 c-0.43,0.2-0.78,0.7-0.99,1.56V20.3l-0.12,0.76c-1.61,5.37-4.01,12.17-7.55,18.1c-3.33,5.57-7.65,10.36-13.27,12.57v40.61 c1.54,1.83,2.96,3.07,4.52,3.85c1.72,0.86,3.74,1.2,6.42,1.2l39.03,0c0.7,0,1.6,0.04,2.45,0.07c2.56,0.1,4.17,0.17,5.9-2.27v-0.01 c0.75-1.06,1.3-2.31,1.69-3.71c0.42-1.49,0.67-3.15,0.79-4.92l0.82-1.75c1.72-1.63,3.03-3.46,3.87-5.71 c0.86-2.32,1.23-5.11,1.02-8.61l-0.09-1.58l1.34-0.83c0.92-0.57,1.42-1.65,1.63-2.97c0.34-2.1-0.02-4.67-0.67-7.06l0.21-1.93 c1.08-2.07,1.6-3.92,1.67-5.54c0.06-1.68-0.37-3.14-1.17-4.35c-0.84-1.27-2.07-2.31-3.56-3.09c-1.92-1.01-4.24-1.59-6.66-1.69v0.01 l-26.32,0l0.59-3.15c0.57-3.05,0.98-5.96,1.22-8.72c0.23-2.7,0.27-5.21,0.12-7.49c-0.45-6.72-3.89-12.04-7.56-14.83 c-1.17-0.89-2.33-1.5-3.38-1.77C70.04,5.27,69.38,5.26,68.9,5.48L68.9,5.48L68.9,5.48z" />
                </g>
              </svg>
              <svg version="1.1" id="Layer_1" height="40" width="40" size="20" xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 122.88 104.19"
                style="enable-background:new 0 0 122.88 104.19" xml:space="preserve">
                <g>
                  <path fill="#c8c5c5"
                    d="M62.63,97.94c0.56,2.85,2.03,4.68,4.04,5.61c1.64,0.76,3.54,0.83,5.52,0.31c1.72-0.45,3.53-1.37,5.26-2.69 c4.69-3.57,9.08-10.3,9.64-18.71c0.17-2.59,0.13-5.35-0.12-8.29c-0.16-1.94-0.41-3.98-0.75-6.1h19.95l0.09-0.01 c3.24-0.13,6.38-0.92,9.03-2.3c2.29-1.2,4.22-2.84,5.56-4.88c1.38-2.1,2.13-4.6,2.02-7.46c-0.08-2.12-0.65-4.42-1.81-6.88 c0.66-2.76,0.97-5.72,0.54-8.32c-0.36-2.21-1.22-4.17-2.76-5.63c0.08-3.65-0.41-6.71-1.39-9.36c-1.01-2.72-2.52-4.98-4.46-6.98 c-0.17-1.75-0.45-3.42-0.89-4.98c-0.55-1.96-1.36-3.76-2.49-5.35l0,0c-3.4-4.8-6.12-4.69-10.43-4.51c-0.6,0.02-1.24,0.05-2.24,0.05 l-39.02,0c-3.51,0-6.27,0.51-8.79,1.77c-2.5,1.25-4.62,3.17-6.89,6.01l-0.58,1.66v45.52l1.98,0.53c5.03,1.36,8.99,5.66,12.07,10.81 c3.16,5.3,5.38,11.5,6.89,16.51v13.16L62.63,97.94L62.63,97.94L62.63,97.94z M4,61.17h29.08c2.2,0,4-1.8,4-4V4c0-2.2-1.8-4-4-4L4,0 C1.8,0,0,1.8,0,4v53.17C0,59.37,1.8,61.17,4,61.17L4,61.17L4,61.17z M68.9,98.72c-0.43-0.2-0.78-0.7-0.99-1.56V83.89l-0.12-0.76 c-1.61-5.37-4.01-12.17-7.55-18.1c-3.33-5.57-7.65-10.36-13.28-12.57V11.85c1.54-1.83,2.96-3.07,4.52-3.85 c1.72-0.86,3.74-1.2,6.42-1.2h39.02c0.7,0,1.61-0.04,2.45-0.07c2.56-0.1,4.17-0.17,5.9,2.27v0.01c0.75,1.06,1.3,2.31,1.69,3.71 c0.42,1.5,0.67,3.15,0.79,4.92l0.82,1.75c1.72,1.63,3.03,3.46,3.87,5.71c0.86,2.32,1.23,5.11,1.02,8.61l-0.09,1.58l1.34,0.83 c0.92,0.57,1.42,1.65,1.63,2.97c0.34,2.09-0.02,4.67-0.67,7.06l0.21,1.92c1.08,2.07,1.6,3.92,1.67,5.54 c0.06,1.68-0.37,3.14-1.17,4.35c-0.84,1.27-2.07,2.31-3.56,3.09c-1.92,1-4.24,1.59-6.66,1.69v-0.01l-26.32,0l0.59,3.15 c0.57,3.05,0.98,5.96,1.22,8.72c0.23,2.7,0.27,5.21,0.12,7.49c-0.45,6.72-3.89,12.04-7.56,14.83c-1.17,0.89-2.33,1.5-3.38,1.77 C70.04,98.92,69.38,98.94,68.9,98.72L68.9,98.72L68.9,98.72z" />
                </g>
              </svg>
            </div>

            <svg xmlns="http://www.w3.org/2000/svg" shape-rendering="geometricPrecision"
              text-rendering="geometricPrecision" image-rendering="optimizeQuality" fill-rule="evenodd" height="40"
              width="40" size="20" clip-rule="evenodd" viewBox="0 0 511.999 507.107">
              <path fill="#c8c5c5" fill-rule="nonzero"
                d="M25.967 505.131l479.615-241.993c8.555-4.05 8.555-15.093 0-19.147L25.964 2.005C10.301-5.855-5.728 10.881 2.05 26.448l120.852 227.115L2.05 480.679c-7.868 15.689 8.377 32.206 23.917 24.452zm-1.657-22.342l116.464-218.858H458.11L24.31 482.789z" />
            </svg>

          </div>
        </div>

      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: false,
      selectedContainer:'linked assets'
    };
  },
  methods: {
    toggleSidebar(value) {
      console.log('value: ', value);
      this.selectedContainer = value
      this.isVisible = !this.isVisible;
    }
  },
  mounted(){
    this.toggleSidebar('linked assets')
  }
};
</script>


<style scoped >
@import './styles.scss';
.main-container {
  min-height: 100vh;
  height: auto;
  display: flex;
  font-family: var(--zds-typography-base, "Inter", Helvetica, arial, sans-serif);
  color: rgb(45, 46, 46);
}
.selected  {
  border: 3px solid rgb(255, 79, 0) !important;
  border-radius: 15px;
  background-color: rgb(255, 243, 230);
}
.sidebar-container {
  width: 100px;
  background-color: red;
  min-height: 100vh;
  border-right: 1px solid rgb(215, 213, 210);
  background-color: rgb(255, 253, 249);
  padding: 0px 5px;
  display: flex;
  flex-direction: column;
  align-items: center;
  height: auto;
}
textarea:active{
  border: none;

}

.icon-container {
  width: 99%;
  display: flex;
  justify-content: center;
  margin-top: 10px;
  height: 8%;
  align-items: center;
  cursor: pointer;
  min-height: 70px;

}

.icon-path {
  fill: gray;
}

.icon-container {
  svg {
    height: 60%;
    width: 60%;
    max-width: 34px;
    max-height: 34px;
  }
}

.icon-container:hover {
  background-color: rgb(255, 243, 230);
  border-radius: 15px;
}

.icon-container:hover .icon-path {
  fill: black;
}
.sidebar {
  width: 550px;
  min-height: 100vh;
  height: auto;
  background-color: #ffffff;
  border: 1px solid rgb(215, 213, 210);
  box-shadow: rgba(0, 0, 0, 0.1) 0px 20px 30px 0px;
  font-size: 24px;
}

.header {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  background-color: #ffffff;
  height: 11%;
  min-height: 93px;
  padding: 26px;
  border-bottom: 1px solid rgb(215, 213, 210);
}

.header-body {
  display: flex;
  justify-content: space-between;
  align-items: center;
  svg{
    cursor: pointer;
  }
}

span {
  font-size: 34px;
  font-weight: bold;

}

.span1 {
  font-size: 27px;
  font-weight: bold;

}

.badge {
  background-color: black;
  color: white;
  border-radius: 30px;
  margin-left: 10px;
  padding: 3px 8px;
  font-size: 25px;
}

.main-body {
  padding: 24px;
  background-color: rgb(235, 235, 235);
}

.sidebar-body {
  display: flex;
  align-items: center;

}

.para {
  margin-top: 19px;
  font-size: 29px;
}

.svg {
  margin-right: 8px;
}

.time {
  margin-left: 16px;
  font-size: 22px;
  color: gray;
}

.paras {
  margin-top: 40px;
  font-size: 22px;
  line-height: var(--zds-typography-paragraph3-lineheight, 24px);
  font-weight: 400;
  color: rgb(45, 46, 46);
}

li {
  line-height: 2rem;
}

.textarea-div {
  border: 3px solid black;
  border-radius: 6px;
  margin-top: 10px;
  bottom: 10px;
  width: 525px;
  margin-left: 10px;
  position: absolute;
  bottom: 0;
}

textarea {
  border: none;
  width: 99%;
font-size:16px;
  background-color: #fafafa;
  resize: vertical;
  height: 250px !important;
  max-height: 250px !important;
}

.icons {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0px 14px;
  border-top: 1px solid gray;
  height: 60px;

}
.three-icons{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 30%;
}
.selected .icon-path{
  fill: black;
}

.sidebar-icon{
  margin-top: 105px;
}

.tooltiptext {
  visibility: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: black;
  color: #fff;
  min-width: 180px;
  font-size: 20px;
  border-radius: 20px;
  height: 40px;
  left: 130px;
  position: absolute;
}

.icon-container:hover .tooltiptext {
  visibility: visible;
}
textarea:focus{
  outline: none;
}

@media screen and (max-height: 1030px) {
  textarea {
    height: 70px !important;
    max-height: 70px !important;
    resize: none;
  }

  .textarea-div{
    bottom: 0px;
    position: relative;
    margin-top: 30px;
  }
}
</style>
