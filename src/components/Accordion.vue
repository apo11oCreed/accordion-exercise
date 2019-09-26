<template>
<div>
    <article :class="open ? 'articleWrapper open' : 'articleWrapper'">
      <h2 @click="$emit('toggleAccordion', index)">{{ title }} - {{ index }}</h2>
      <div class="content">
      <div>
        <img src="https://via.placeholder.com/32x32/fc8776/000000/?text=img" :alt="title" />
        </div>
        <div>
          <p>{{ content }}</p>
          <a class="link" href="link">{{ link }}</a>
          </div>
          </div>
          </article>
          </div>
</template>

<script>
export default {
  name: 'Accordion',
  props: ['title',
    'index',
    'content',
    'link',
    'open'
    ]
  }
</script>

<style scoped>
</style>