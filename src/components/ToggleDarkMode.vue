<template>
    <!-- Created By Joseph Shenton @TeamiHackify 

Please feel free to use this toggle if you like. But I request that you give credit to me thank you -->

<div class="button-con">
  <label for='cb1'>
    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="dayIcon" :class="{ darkmode : darkMode}" x="0px" y="0px" viewBox="0 0 35 35" style="enable-background:new 0 0 35 35;" xml:space="preserve">
      <g id="Sun">
        <g>
          <path style="fill-rule:evenodd;clip-rule:evenodd;" d="M6,17.5C6,16.672,5.328,16,4.5,16h-3C0.672,16,0,16.672,0,17.5    S0.672,19,1.5,19h3C5.328,19,6,18.328,6,17.5z M7.5,26c-0.414,0-0.789,0.168-1.061,0.439l-2,2C4.168,28.711,4,29.086,4,29.5    C4,30.328,4.671,31,5.5,31c0.414,0,0.789-0.168,1.06-0.44l2-2C8.832,28.289,9,27.914,9,27.5C9,26.672,8.329,26,7.5,26z M17.5,6    C18.329,6,19,5.328,19,4.5v-3C19,0.672,18.329,0,17.5,0S16,0.672,16,1.5v3C16,5.328,16.671,6,17.5,6z M27.5,9    c0.414,0,0.789-0.168,1.06-0.439l2-2C30.832,6.289,31,5.914,31,5.5C31,4.672,30.329,4,29.5,4c-0.414,0-0.789,0.168-1.061,0.44    l-2,2C26.168,6.711,26,7.086,26,7.5C26,8.328,26.671,9,27.5,9z M6.439,8.561C6.711,8.832,7.086,9,7.5,9C8.328,9,9,8.328,9,7.5    c0-0.414-0.168-0.789-0.439-1.061l-2-2C6.289,4.168,5.914,4,5.5,4C4.672,4,4,4.672,4,5.5c0,0.414,0.168,0.789,0.439,1.06    L6.439,8.561z M33.5,16h-3c-0.828,0-1.5,0.672-1.5,1.5s0.672,1.5,1.5,1.5h3c0.828,0,1.5-0.672,1.5-1.5S34.328,16,33.5,16z     M28.561,26.439C28.289,26.168,27.914,26,27.5,26c-0.828,0-1.5,0.672-1.5,1.5c0,0.414,0.168,0.789,0.439,1.06l2,2    C28.711,30.832,29.086,31,29.5,31c0.828,0,1.5-0.672,1.5-1.5c0-0.414-0.168-0.789-0.439-1.061L28.561,26.439z M17.5,29    c-0.829,0-1.5,0.672-1.5,1.5v3c0,0.828,0.671,1.5,1.5,1.5s1.5-0.672,1.5-1.5v-3C19,29.672,18.329,29,17.5,29z M17.5,7    C11.71,7,7,11.71,7,17.5S11.71,28,17.5,28S28,23.29,28,17.5S23.29,7,17.5,7z M17.5,25c-4.136,0-7.5-3.364-7.5-7.5    c0-4.136,3.364-7.5,7.5-7.5c4.136,0,7.5,3.364,7.5,7.5C25,21.636,21.636,25,17.5,25z" />
        </g>
      </g>
    </svg>
  </label>
  <input class='toggle' id='cb1' type='checkbox'>
  <label v-on:click="toggleDarkMode" class='toggle-button' for='cb1'></label>
  <label for='cb1'>
    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="nightIcon" :class="{ darkmode : darkMode}" x="0px" y="0px" viewBox="0 0 100 100" enable-background="new 0 0 100 100" xml:space="preserve">
      <path d="M96.76,66.458c-0.853-0.852-2.15-1.064-3.23-0.534c-6.063,2.991-12.858,4.571-19.655,4.571  C62.022,70.495,50.88,65.88,42.5,57.5C29.043,44.043,25.658,23.536,34.076,6.47c0.532-1.08,0.318-2.379-0.534-3.23  c-0.851-0.852-2.15-1.064-3.23-0.534c-4.918,2.427-9.375,5.619-13.246,9.491c-9.447,9.447-14.65,22.008-14.65,35.369  c0,13.36,5.203,25.921,14.65,35.368s22.008,14.65,35.368,14.65c13.361,0,25.921-5.203,35.369-14.65  c3.872-3.871,7.064-8.328,9.491-13.246C97.826,68.608,97.611,67.309,96.76,66.458z" />
    </svg>
  </label>
</div>
</template>

<script>
export default {
    name: 'ToggleDarkMode',
    emits: ['darkMode-btn'],
    data () {
        return {
            darkMode: false
        }
    },
    methods: {
        toggleDarkMode () {
            this.darkMode = !this.darkMode
            this.$emit('darkMode-btn')
        }
    }
}


</script>


<style scoped>
/* Created By Joseph Shenton @TeamiHackify 

Please feel free to use this toggle if you like. But I request that you give credit to me thank you */

body {
  background: #25272A;
  -webkit-transition: background-color 150ms ease-out !important;
  transition: background-color 150ms ease-out !important;
}

body.day-background {
  background: #FFDB88;
}



#dayIcon {
  position: relative;
  width: 26px;
  height: 26px;
  top: -3px;
  margin: 0 7px;
  fill: #142d4c;
}
#dayIcon.darkmode {
  fill: #9fd3c7;
}

#nightIcon {
  position: relative;
  width: 26px;
  height: 26px;
  top: -3px;
  margin: 0 7px;
  fill: #142d4c;
}
#nightIcon.darkmode {
  fill: #9fd3c7;
}

#dayIcon, #nightIcon {
  cursor: pointer;
}

.toggle {
  display: none;
}

.toggle, .toggle:after, .toggle:before, .toggle *, .toggle *:after, .toggle *:before, .toggle + .toggle-button {
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

.toggle::-moz-selection, .toggle:after::-moz-selection, .toggle:before::-moz-selection, .toggle *::-moz-selection, .toggle *:after::-moz-selection, .toggle *:before::-moz-selection, .toggle + .toggle-button::-moz-selection {
  background: none;
}

.toggle::selection, .toggle:after::selection, .toggle:before::selection, .toggle *::selection, .toggle *:after::selection, .toggle *:before::selection, .toggle + .toggle-button::selection {
  background: none;
}

.toggle + .toggle-button {
  outline: 0;
  display: inline-block;
  width: 4em;
  height: 2em;
  position: relative;
  cursor: pointer;
  border: 2px solid #333;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.toggle + .toggle-button:after, .toggle + .toggle-button:before {
  position: relative;
  display: block;
  content: "";
  width: 50%;
  height: 100%;
}

.toggle + .toggle-button:after {
  left: 0;
}

.toggle + .toggle-button:before {
  display: none;
}

.toggle:checked + .toggle-button:after {
  left: 50%;
}

.toggle + .toggle-button {
  padding: 2px;
  -webkit-transition: all .2s ease;
  transition: all .2s ease;
  border: 2px solid #142d4c;
  border-radius: 2em;
}

.toggle + .toggle-button:after {
  -webkit-transition: all .2s ease;
  transition: all .2s ease;
  background: #385170;
  content: "";
  border-radius: 1em;
}

.toggle:checked + .toggle-button:after {
  left: 50%;
}
@media only screen and (max-width: 380px) and (max-height: 670px){

    .button-con {
        cursor: default;
        position: absolute;
        top: 4.5vh;
        left:45.7vh;
        margin-left: -76px;
        margin-top: -18px;
      }

}
@media only screen and (max-width: 480px) and (min-width: 381px){

    .button-con {
        cursor: default;
        position: absolute;
        top: 4.5vh;
        left:38vh;
        margin-left: -76px;
        margin-top: -18px;
    }

}
@media (max-width: 480px) {
  .button-con {
        cursor: default;
        position: absolute;
        top: 4.5vh;
        left: 82%;
        margin-left: -76px;
        margin-top: -18px;
    }
}
@media (min-width: 481px) and (max-width: 767px){
  .button-con {
        cursor: default;
        position: absolute;
        top: 7.5vh;
        left:90%;
        margin-left: -76px;
        margin-top: -18px;
    }
}
@media (min-width: 768px) and (max-width: 992px){

  .button-con {
        cursor: default;
        position: absolute;
        top: 7.5vh;
        left:90%;
        margin-left: -76px;
        margin-top: -18px;
    }
}
@media (min-width: 992px){

}

</style>