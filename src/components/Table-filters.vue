<template>
  <div>
  <h2 class="subtitle">Table Filters Demo</h2>
  <p><strong>vue-good-table</strong> allows two modes of filtering</p>
  <vue-good-table
      title="Global Filter"
      :columns="columns"
      :paginate="true"
      :globalSearch="true"
      :rows="rows"
      styleClass="table table-bordered"/>
<pre v-highlightjs><code class="html">&lt;vue-good-table
  title=&quot;Global Filter&quot;
  :columns=&quot;columns&quot;
  :rows=&quot;rows&quot;
  :paginate=&quot;true&quot;
  :globalSearch=&quot;true&quot;
  styleClass=&quot;table table-bordered&quot;/&gt;
</code></pre>
  <vue-good-table
      title="Column Filters"
      :columns="columns2"
      :paginate="true"
      :rows="rows"
      styleClass="table table-bordered"/>
<div class="notification is-warning">
  Make sure you don't have globalSearch set to true
</div>
<pre v-highlightjs><code class="javascript">
// here we set property filterable on the columns
columns: [
  {
    label: 'Name',
    field: 'name',
    filterable: true,
  },
  {
    label: 'Age',
    field: 'age',
    type: 'number',
    filterable: true,
  },
  {
    label: 'Joined On',
    field: 'joined',
    type: 'date',
    inputFormat: 'YYYYMMDD',
    outputFormat: 'MMM Do YYYY',
  },
]
</code></pre>
  </div>
</template>

<script>
export default {

  name: 'Table-filters',

  data () {
    return {
      columns: [
          {
            label: 'Name',
            field: 'name',
          },
          {
            label: 'Age',
            field: 'age',
            type: 'number',
          },
          {
            label: 'Joined On',
            field: 'joined',
            type: 'date',
            inputFormat: 'YYYYMMDD',
            outputFormat: 'MMM Do YYYY',
          },
        ],
      columns2: [
          {
            label: 'Name',
            field: 'name',
            filterable: true,
          },
          {
            label: 'Age',
            field: 'age',
            type: 'number',
            filterable: true,
          },
          {
            label: 'Joined On',
            field: 'joined',
            type: 'date',
            inputFormat: 'YYYYMMDD',
            outputFormat: 'MMM Do YYYY',
          },
        ],
      rows: [
        {name:"John", age:20, joined: '20120201'},
        {name:"Jane", age:24, joined: '20120305'},
        {name:"Susan", age:16, joined: '20140823'},
        {name:"Chris", age:55, joined: '20161109'},
        {name:"Dan", age:40, joined: '20170612'},

        {name:"Jay", age:20, joined: '20120201'},
        {name:"Seah", age:24, joined: '20120305'},
        {name:"Sarah", age:16, joined: '20140823'},
        {name:"Mohit", age:55, joined: '20161109'},
        {name:"Don", age:40, joined: '20170612'},

        {name:"Ernesto", age:20, joined: '20120201'},
        {name:"Clark", age:24, joined: '20120305'},
        {name:"Monty", age:16, joined: '20140823'},
        {name:"Priya", age:55, joined: '20161109'},
        {name:"Sans", age:40, joined: '20170612'},
      ],
    };
  }
};
</script>

<style lang="css" scoped>
</style>