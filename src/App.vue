<script setup>
import todo from "./components/todo.vue";
import Compositionarr from "./components/compositionarr.vue";
import customdirectivesVue from "./components/customdirectives.vue";
import provide from "./components/provide.vue";
import Inject from "./components/inject.vue";
import slotVue from "./components/slot.vue";
import mountVue from "./components/mount.vue";
import tableVue from "./components/table.vue";
import DataTable from 'primevue/datatable';
import Column from 'primevue/column';
import ColumnGroup from 'primevue/columngroup';     //optional for column grouping
import Row from 'primevue/row';
</script>
<!--<template>
  <div class="container">
    <div class="row">
      <div class="col-sm-6">
      
          <mountVue />
          <customdirectivesVue/>
      </div>

      <div class="col-sm-6">
      <slotVue>
        <template v-slot:default="props">{{props.user}}</template>
        </slotVue>
      </div>
      
    </div>
  </div>
</template>
-->
<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6">
      <tableVue />
      </div>
      <div class="col-md-6">
      </div>
    </div>
    
  </div>
</template>
