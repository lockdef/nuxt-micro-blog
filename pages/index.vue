<template>
  <div>
    <Blogpost
      class="mb-4"
      @catchData="getData"
    />
    <hr class="my-4">
    <div v-for="data in blogdata" :key="data">
      <Blogcard
        :title="data.title"
        :text="data.text"
      />
      <hr class="my-4">
    </div>
  </div>
</template>

<script>
import Blogcard from '@/components/Blogcard'
import Blogpost from '@/components/Blogpost'

export default {
  components: {
    Blogcard,
    Blogpost
  },
  data () {
    return {
      blogdata: []
    }
  },
  methods: {
    getData (title, text) {
      this.blogdata.push({ title, text })
    }
  }
}
</script>
