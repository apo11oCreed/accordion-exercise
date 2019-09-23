<template>
<div>
    <article class="articleWrapper"><h2>{{ title }} - {{ index }}</h2><a href="#" @click="toggleAccordion" class="arrowUp"></a>
    <p>{{ content }}</p>
    <a href="link">{{ link }}</a>
    </article>
    </div>
</template>

<script>
export default {
  name: 'Accordion',
  props: {
    title:String,
    index:Number,
    content:String,
    link:String
    },
    methods:{
      toggleAccordion: function(){
        console.log('test');
        }
      }
    }
</script>

<style scoped>

</style>