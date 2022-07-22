<template>
  <ejs-grid :dataSource="data" height=300 :enableInfiniteScrolling='true' :pageSettings='options' :allowResizing='true' :allowSorting='true'>
    <e-columns>
      <e-column field="No" headerText="No" textAlign="Right" :isPrimaryKey="true" width="30"></e-column>
      <e-column field="Tag for Raw Data(1)" headerText="Tag for Raw Data(1)"  width="70"></e-column>
      <e-column field="Tag for Raw Data(2)" headerText="Tag for Raw Data(2)" width="70"></e-column>
      <e-column field="Tag for input Data" headerText="Tag for input Data" width="70"></e-column>
      <e-column field="Description" headerText="Description" width="80"></e-column>
      <e-column field="Unit" headerText="Unit" width="40"></e-column>
      <e-column field="Raw Data(1)" headerText="Raw Data(1)" width="50"></e-column>
      <e-column field="Raw Data(2)" headerText="Raw Data(2)" width="50"></e-column>
      <e-column field="input Data" headerText="input Data" width="50"></e-column>
      <e-column field="Factor A" headerText="Factor A" width="40"></e-column>
      <e-column field="Factor B" headerText="Factor B" width="40"></e-column>
      <e-column field="Sensor Error" headerText="Sensor Error" width="50"></e-column>
      <e-column field="Reference Input" headerText="Reference Input" width="60"></e-column>
      <e-column field="Remark" headerText="Remark" width="40"></e-column>
    </e-columns>
  </ejs-grid>
</template>
<script>
import { GridComponent, ColumnsDirective, ColumnDirective, InfiniteScroll, Resize, Sort} from "@syncfusion/ej2-vue-grids";
import "../node_modules/@syncfusion/ej2-base/styles/material.css";
import "../node_modules/@syncfusion/ej2-buttons/styles/material.css";
import "../node_modules/@syncfusion/ej2-calendars/styles/material.css";
import "../node_modules/@syncfusion/ej2-dropdowns/styles/material.css";
import "../node_modules/@syncfusion/ej2-inputs/styles/material.css";
import "../node_modules/@syncfusion/ej2-navigations/styles/material.css";
import "../node_modules/@syncfusion/ej2-popups/styles/material.css";
import "../node_modules/@syncfusion/ej2-splitbuttons/styles/material.css";
import "../node_modules/@syncfusion/ej2-vue-grids/styles/material.css";
export default {
  name: "App",
  // Declaring component and its directives
    components: {
      "ejs-grid": GridComponent,
      "e-columns": ColumnsDirective,
      "e-column": ColumnDirective,
    },
  // Bound properties declaration
  data() {
    return {
      options: { pageSize: 50},
      data: [
        {
        "No": 1,
        "Tag for Raw Data(1)": "2811-TM-CV1_POS",
        "Tag for Raw Data(2)": "X_2811-TM-CV1_POS",
        "Tag for input Data": "I_2811-TM-CV1_POS",
        "Description": "HP TURBINE GOVERNING VALUE 1 POSITION",
        "Unit": "%",
        "Raw Data(1)": 100.037240,
        "Raw Data(2)": 100.037240,
        "input Data": 100.037240,
        "Factor A": 1,
        "Factor B": 0,
        "Sensor Error":0.000000,
        "Reference Input": 100.037240,
        "Remark": ""
        },
        {
        "No": 2,
        "Tag for Raw Data(1)": "2811-TM-CV2_POS",
        "Tag for Raw Data(2)": "X_2811-TM-CV2_POS",
        "Tag for input Data": "I_2811-TM-CV2_POS",
        "Description": "HP TURBINE GOVERNING VALUE 2 POSITION",
        "Unit": "%",
        "Raw Data(1)": 99.902058,
        "Raw Data(2)": 99.902058,
        "input Data": 99.902058,
        "Factor A": 1,
        "Factor B": 0,
        "Sensor Error":0.000000,
        "Reference Input": 99.902058,
        "Remark": ""
        }
      ]
    };
  },
  provide: {
    grid: [InfiniteScroll, Resize, Sort]
  }
};
</script>
<style>
  @import "../node_modules/@syncfusion/ej2-vue-grids/styles/material.css";
  .e-grid .e-altrow{
    background-color: #fafafa;
  }
</style>