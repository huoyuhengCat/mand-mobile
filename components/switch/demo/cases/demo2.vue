<template>
  <div class="md-example-child md-example-child-switch md-example-child-switch-2">
    <md-switch
      v-model="isActive"
      disabled
      @change="handler('switch2', isActive, $event)"
    ></md-switch>
  </div>
</template>

<script>import {Switch} from 'mand-mobile'

export default {
  name: 'switch-demo',
  /* DELETE */
  title: '开启不可用状态',
  titleEnUS: 'Open and disabled',
  /* DELETE */
  components: {
    [Switch.name]: Switch,
  },
  data() {
    return {
      isActive: true,
    }
  },
  methods: {
    handler(name, active) {
      console.log(`Status of switch ${name} is ${active ? 'active' : 'inactive'}`)
    },
  },
}
</script>