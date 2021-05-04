<template>
<div>
<hero/>
<target/>
<contact/>
</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
 import Hero from '@/components/Hero.vue'; // @ is an alias to /src
import Target from '@/components/Target.vue';
import Contact from '@/components/Contact.vue';

export default defineComponent({
  name: 'Home',
  components: {
     Hero,
     Target,
     Contact
  }
});
</script>

