<template>
  <div id="app">
    <resume></resume>
    <!--<winter></winter>-->
  </div>
</template>

<script>
import Winter from './components/Winter'
import Resume from './components/Resume'

export default {
  name: 'app',
  components: {
    Winter,
    Resume
  }
}
</script>

