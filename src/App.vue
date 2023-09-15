<script setup>
async function submit(data) {
  await new Promise(r => setTimeout(r, 1000))
  alert(`Submitted! 🎉 ${JSON.stringify(data, null, 2)}`)
}
</script>

<template>
  <div class="your-first-form">
    <img
      src="https://pro.formkit.com/logo.svg"
      alt="FormKit Logo"
      width="244"
      height="50"
      class="logo"
    >

    <FormKit type="form" @submit="submit">
      <FormKit type="text" name="Name" label="Your name" help="Your name goes here" validation="required" />
      <FormKit type="email" name="Email" label="Email" help="Your email goes here" validation="required|email"/>
      <FormKit type="textarea" name="Message" label="Message" help="Your message goes here" validation="required" />
    </FormKit>
  </div>
</template>

<style scoped>
.your-first-form {
  width: calc(100% - 2em);
  max-width: 480px;
  box-sizing: border-box;
  padding: 2em;
  box-shadow: 0 0 1em rgba(0, 0, 0, .1);
  border-radius: .5em;
  margin: 4em auto;
}

.logo {
  width: 150px;
  height: auto;
  display: block;
  margin: 0 auto 2em auto;
}
pre {
  background-color: rgba(0, 100, 250, .1);
  padding: 1em;
}
</style>
