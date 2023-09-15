<script setup lang="ts">
import { FormKitSchema } from "@formkit/vue";

const schema = [
  {
    $el: "section",
    children: [
      {
        $el: "h1",
        children: "Insurance for businesses big, little and bold."
      },
      {
        $el: "ul",
        children: [
          {
            $el: "li",
            children: "Customised to your needs"
          },
          {
            $el: "li",
            children: "Simple process for small businesses"
          },
          {
            $el: "li",
            children: "Broker service for the more complex"
          }
        ]
      },
      {
        $el: "button",
        attrs: {
          class: "btn btn-primary"
        },
        children: "Start your quote"
      },
      {
        $el: "button",
        attrs: {
          class: 'btn btn-secondary'
        },
        children: "Broker service"
      }
    ]
  }
];
</script>

<template>
  <img
    src="https://pro.formkit.com/logo.svg"
    alt="FormKit Logo"
    width="244"
    height="50"
    class="logo"
  />
  <div class="container">
    <FormKitSchema :schema="schema" />
  </div>
</template>

<style>
.container {
  width: calc(100% - 2em);
  max-width: 80rem;
  box-sizing: border-box;
  padding: 2em;
  box-shadow: 0 0 1em rgba(0, 0, 0, 0.1);
  border-radius: 0.5em;
  margin: 4em auto;
}

.btn {
  padding: 0.85rem 0.75rem;
  border-radius: 0.5em;
  margin-right: 2rem;
  border: none;
}

.btn-primary {
  background-color: hotpink;
  color: #fff;
}

.btn-secondary {
  background-color: rgb(22, 1, 12);
  color: #fff;
}

.logo {
  width: 150px;
  height: auto;
  display: block;
  margin: 0 auto 2em auto;
}
</style>
