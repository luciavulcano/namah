<template>
  <div>
    <div class="separador">
      <div class="linha"></div>
      <h2>Blog</h2>
      <div class="linha"></div>
    </div>
    <div class="wrapper">
      <div class="content">
        <p>Here is my content.</p>
        <p>Here is my content.</p>
      </div>
    </div>
    <q-card class="my-card">
      <q-img src="~/assets/blog-card1.png">
        <div class="absolute-bottom">
          <div class="">Our Changing Planet</div>
          <div class="">by John Doe</div>
        </div>
      </q-img>
    </q-card>
    <Newsletter/>
  </div>
</template>
<script>
import Newsletter from 'components/Newsletter.vue'

export default {
  components: { Newsletter }
}
</script>
