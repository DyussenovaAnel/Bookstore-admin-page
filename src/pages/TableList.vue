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
            <simple-table></simple-table>
          </md-card-content>
        </md-card>
      </div>
    </div>
  </div>
</template>

<script>
import { SimpleTable } from "@/components";
import { OrderedTable } from "@/components";

export default {
  components: {
    // OrderedTable,
    'simple-table': OrderedTable,
  },
};
</script>
