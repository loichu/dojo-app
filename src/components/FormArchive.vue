<template>
  <!-- HTML code -->
  <div>
    <button class="primary" v-go-back=" '/archives' ">Back</button>

    <h1>HELLO</h1>

    <form>
      <q-datetime
        v-model="date"
        class="full-width"
        type="date"
        placeholder="Date"
        format="YYYY - M - d"
        :default-selection="today"
      ></q-datetime>

      <br />

      <q-select
        class="full-width"
        placeholder="Choose a type"
        v-model="type"
        :options="types"
      />

      <div class="floating-label">
        <input v-model="title" required class="full-width">
        <label>Title</label>
      </div>

      <div class="floating-label">
        <textarea  required class="full-width"></textarea>
        <label>Description</label>
      </div>
    </form>

  </div>
</template>

<script>
  import moment from 'moment'
  export default {
    data () {
      return {
        type: '',
        types: [
          {
            label: 'trainee',
            value: 'trainee'
          },
          {
            label: 'advanced',
            value: 'advanced'
          }
        ],
        today: moment().format(),
        date: ""
      }
    },
    computed: {
      placeholder () {
        return 'hello'
      }
    }
  }
</script>

<style>
  /* CSS */
</style>
