<template>
  <div>
    Hello GIS, Hello Map
  </div>
</template>

<script>
export default {
  name: 'HelloGIS',
  mounted () {
    this.loadData()
  },
  methods: {
    loadData () {
      fetch('/api/city').then(response => {
        return response.json()
      }).then(data => {
        console.log(data)
      })
    }
  }
}
</script>
