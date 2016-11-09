<template>
  <div>
    <div class="tile is-ancestor">
      <div class="tile is-parent">
        <article class="tile is-child box">
          <h1>Data grid</h1>
          <handsontable :data="rawData" :settings="{ }"></handsontable>
        </article>
      </div>
    </div>
  </div>
</template>

<script>
import Handsontable from 'vue-handsontable'

export default {
  components: {
    Handsontable
  },

  data () {
    return {
      rawData: [
        ['', 'Kia', 'Nissan', 'Toyota', 'Honda'],
        ['2008', 11, 11, 12, 13],
        ['2009', 21, 11, 14, 13],
        ['2010', 31, 15, 12, 13]
      ]
    }
  }
}
</script>
