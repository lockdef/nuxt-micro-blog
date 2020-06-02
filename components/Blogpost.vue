<template>
  <v-form
    ref="form"
    v-model="valid"
    :lazy-validation="lazy"
  >
    <v-text-field
      v-model="title"
      label="Title"
      required
    />

    <v-text-field
      v-model="text"
      label="Text"
      required
    />

    <v-btn
      color="success"
      class="mr-4"
      @click="sendData"
    >
      Submit
    </v-btn>

    <v-btn
      color="error"
      class="mr-4"
      @click="resetData"
    >
      Reset Form
    </v-btn>
  </v-form>
</template>

<script>
export default {
  name: 'Blogpost',
  data () {
    return {
      title: '',
      text: ''
    }
  },
  methods: {
    sendData () {
      this.$emit('catchData', this.title, this.text)
    },
    resetData () {
      this.title = ''
      this.text = ''
    }
  }

}
</script>
