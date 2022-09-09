<template>
  <div class="content">
    <div class="md-layout">
      <div
        class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-100"
      >
        <md-card>
          <!-- <md-card-header>
            <h4><b>Все товары</b></h4>
          </md-card-header> -->
          <md-card-content>
            <lists-table></lists-table>
          </md-card-content>
        </md-card>
      </div>
    </div>
  </div>
</template>

<script>
import { ListsTables } from "@/components";

export default {
  components: {
    // OrderedTable,
    'lists-table': ListsTables,
  },
};
</script>
