<template>
  <div class="box">
        <div class="title">
          <div v-if="box.name === 'marketplace'" class="svg">
            <svg xmlns="http://www.w3.org/2000/svg" width='30' height='40' viewBox="0 0 24 24">
              <path d="M15.6 1.6H8.4c-.4 0-.7.3-.7.7v2.5h8.5V2.3c.1-.4-.2-.7-.6-.7z" fill="#f8c346" />
              <path d="M19.8 10.2H4.2c-.6 0-1 .4-1 1v10.2c0 .6.4 1 1 1l15.7.1c.6 0 1-.4 1-1V11.3c-.1-.7-.5-1.1-1.1-1.1z" fill="#f8c346" />
              <path d="M9.2 13.6c-1.2 0-2.3-.7-2.9-1.8-.5 1.1-1.6 1.8-2.9 1.8h-.2C1.1 13.5-.1 11.2.8 9.3l3-5.1c.3-.6.8-1 1.5-1h13.5c.6 0 1.2.4 1.5 1l3 5.1c.8 1.9-.4 4.1-2.5 4.2h-.2c-1.2 0-2.3-.7-2.9-1.8-.7 1.6-2.6 2.2-4.2 1.5-.7-.3-1.2-.8-1.5-1.5-.5 1.2-1.6 1.9-2.8 1.9z" fill="#fbd84a" />
              <g>
                <path d="M13.3 22.4v-5.1c0-.3.1-.5.3-.5h4c.1 0 .3.2.3.5v5.1" fill="#fbd84a" />
              </g>
            </svg>
          </div>
          <div v-else class="svg">
            <svg xmlns="http://www.w3.org/2000/svg" width='30' height='40' viewBox="0 0 24 24">
              <path d="M22.5 15.4H1.5c-.7 0-1.4.6-1.4 1.3V18c0 .7.6 1.4 1.4 1.4l21 .1c.7 0 1.4-.6 1.4-1.3v-1.3c0-.8-.6-1.5-1.4-1.5z" fill="#CD302F" />
              <circle cx="4.8" cy="9.6" r="2.4" fill="#CD302F" />
              <path d="M.1 16.5c0-2 2.1-3.6 4.7-3.6s4.7 1.6 4.7 3.6" fill="#CD302F" />
              <circle cx="19.2" cy="9.7" r="2.4" fill="#CD302F" />
              <path d="M14.5 16.5c0-2 2.1-3.6 4.7-3.6s4.7 1.6 4.7 3.6" fill="#CD302F" />
              <circle cx="12" cy="8" r="3.5" fill="#ED9B3D" />
              <path d="M5.2 17.9c0-2.9 3.1-5.3 6.8-5.3 3.7 0 6.8 2.4 6.8 5.3" fill="#ED9B3D" />
              <path d="M5.2 17.9h13.5v1.4H5.2z" fill="#ED9B3D" transform="matrix(1 .00338 -.00338 1 .063 -.04)" />
            </svg>
          </div>
          Quickstart {{box.name}}
        </div>
        <div class="description">
          Launching your {{box.name}}? Use this guide to understand the workflow and basic.
          <div class="link-orange">
            <svg xmlns="http://www.w3.org/2000/svg" width='50' height='25' viewBox="0 0 24 24">
              <path d="M23.6 12.9l-7 7.4c-.5.4-1.4.6-1.9.1s-.5-1.4 0-1.9l4.9-5.2H1.3C.6 13.3 0 12.7 0 12c0-.7.6-1.3 1.3-1.3h18.3l-4.9-5.2c-.4-.4-.5-1.4 0-1.9s1.5-.3 1.9.1l7 7.4c.5.6.4 1.2 0 1.8" fill="#EA7B57" />
            </svg>
           Quickstart {{box.name}}
          </div>
        </div>
      </div>
</template>

<script>
export default {
  name: 'Box',
  props: {
    box: { name:Object, required: true }
  }
}
</script>

<style >
.title {
  padding: 1em 2em;
  letter-spacing: 0.1em;
  border-bottom: 0.2em solid #f0f3f7;
  text-transform: uppercase;
  display: flex;
  align-items: center;
  font-weight: 700;
}

.box {
  margin: 2em;
  background: #ffffff;
  border-radius: 0.2em;
  max-width: 100%;
}

.svg {
  margin-right: 1em;
}

.description {
  padding: 2em;
  font-weight: 300;
  font-size: 20px;
}

.link-orange {
  color: #ea7b57;
  font-weight: 700;
  display: flex;
  align-items: center;
  margin-top: 2em;
  font-size: 20px;
  text-transform: capitalize
}

</style>
