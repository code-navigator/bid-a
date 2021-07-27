<template lang="pug" >
  splitpanes
    pane(
      size="15"
    )
      splitpanes(
        horizontal
      )
        pane
          v-card(
            height="100%"
            width="100%"
            color="secondary"
          )
            v-toolbar(
              dense
            )

        pane
          v-card(
            height="100%"
            width="100%"
            color="secondary"
          )
            v-toolbar(
              dense
            )

    pane 3

</template>

<script>
import { Splitpanes, Pane } from 'splitpanes'
import 'splitpanes/dist/splitpanes.css'

export default {
  components: {
    Splitpanes,
    Pane
  }
}
</script>

<style>
  .splitpanes__pane {
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: Helvetica, Arial, sans-serif;
    color: rgba(255, 255, 255, 0.6);
    font-size: 5rem;
  }

  .splitpanes--horizontal>.splitpanes__splitter {
    height: 5px;
    background-color: white;
  }

  .splitpanes--vertical>.splitpanes__splitter {
    width: 5px;
    background-color: white;
  }

</style>


