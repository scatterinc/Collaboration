<template>
  <div class="sales">
    <b-container class="Sales Header">
      <b-row>
        <b-col
          ><h1>Sales <i>Grid</i></h1></b-col
        >
        <b-col class="d-flex align-items-center"> {{ timeString }} test </b-col>
        <b-col class="d-flex align-items-center justify-content-end">
          <div>
            <dropdown-bar-item
              v-for="(dd, key) in dropdownBar"
              v-bind="dd"
              :key="key"
            />
          </div>
        </b-col>
      </b-row>
    </b-container>
    <p class="border-top mb-4"></p>
    <b-row variant="transparent">
      <b-col
        class="border center bg-primary"
        style="padding-right: 0px !important"
      >
        <p />
        <div class="mb-2 mt-4 ml-1">
          <b-row
            v-for="(row, n) in list"
            :key="`row${n}`"
            class="text-center center row container-fluid mb-2"
          >
            <b-list-group horizontal="md" class="row px-md-6 flex-fill">
              <b-list-group-item
                v-for="(item, key) in row"
                :key="`item${key}`"
                button
                class="col mr-1 ml-1 rounded border shadow"
                variant="'variant'"
              >
                <template v-if="item.left">
                  <div class="text-left">{{ item.left }}</div>
                  <div class="text-right">{{ item.right }}</div>
                </template>
                <span v-else> {{ item }} </span>
              </b-list-group-item>
            </b-list-group>
                      </b-row>
        </div>

        <b-row class="text-center center row container-fluid"> </b-row>
        <div>
             <h1 style="color: red"><font size="5">I want to add vairant props to v-for function, so i can change color of bottom buttons</font></h1>
            </div>
      </b-col>
      <b-col class="border" cols="6" md="4">
        <p />
        <div>
          <b-list-group horizontal="md" class="mb-2 flex-fill">
            <b-list-group-item button class="mr-4 text-center"
              >Customer</b-list-group-item
            >
            <b-list-group-item button class="mr-4 border-left text-center"
              >Table</b-list-group-item
            >
          </b-list-group>
        </div>
        <div class="table-gridcontainer">
          <b-table
            class="text-center"
            :items="filteredData"
            :fields="fields"
            :small="true"
          >
            <template #cell(extPrice)="{ item }">
              {{ formatCurrency(item.quantity * item.price) }}
            </template>
          </b-table>
        </div>
        <!-----
      <div>
        <b-row>
          <b-col class="border-top">
          </b-col>
          <b-col class="border-top text-right">
            Subtotal
          </b-col>
            <b-col class="border-top text-right">
            $10,000
          </b-col>
        </b-row>
                <b-row>
          <b-col class="border">
          </b-col>
          <b-col class="border text-right">
            Tax
          </b-col>
            <b-col class="border text-right">
            $10
          </b-col>
        </b-row>--->
        <div>
          <b-row>
            <b-col class="border-bottom bg-primary"> </b-col>
            <b-col class="border-bottom text-right bg-primary">
              <b style="color: green"><font size="5">Total</font></b>
            </b-col>
            <b-col class="border-bottom text-right bg-primary">
              <b style="color: green"><font size="5">$ 10,000</font></b>
            </b-col>
          </b-row>
        </div>
        <!----
      <div>
  <b-list-group horizontal>
    <b-list-group-item button class="text-center">1</b-list-group-item>
    <b-list-group-item button class="text-center">2</b-list-group-item>
    <b-list-group-item button class="text-center">3</b-list-group-item>
    <b-list-group-item button class="text-center">Clr</b-list-group-item>
  </b-list-group>
</div>
       <div>
  <b-list-group horizontal='sm'>
    <b-list-group-item button class="text-center">4</b-list-group-item>
    <b-list-group-item button class="text-center">5</b-list-group-item>
    <b-list-group-item button class="text-center"> 6</b-list-group-item>
    <b-list-group-item button class="text-center">OK</b-list-group-item>
  </b-list-group>
</div>
       <div>
  <b-list-group horizontal>
    <b-list-group-item button class="text-center">7</b-list-group-item>
    <b-list-group-item button class="text-center">8</b-list-group-item>
    <b-list-group-item button class="text-center">9</b-list-group-item>
    <b-list-group-item button class="text-center">0</b-list-group-item>
  </b-list-group>
</div> --->
        <p />
        <div>
          <b-list-group horizontal="md" class="mb-4 flex-fill">
            <b-list-group-item
              button
              class="mr-4 mb-4 text-center"
              variant="danger"
              >Delete</b-list-group-item
            >
            <b-list-group-item
              button
              class="mr-4 mb-4 border-left text-center"
              variant="info"
              >Ordgfger</b-list-group-item
            >
            <b-list-group-item
              button
              class="mr-4 mb-4 border-left text-center"
              variant="success"
              >Pay</b-list-group-item
            >
          </b-list-group>
        </div>
      </b-col>
    </b-row>
  </div>
</template>
<script>
export default {
  name: 'SalesGridItem',
  data: () => ({
    list: [
      [
        { left: 'Chicken Foot Soup', right: '$2,000', variant: 'info' },
        'Dapibus ac facilisis in',
        'Morbi leo risus',
        'Cras justo odio',
        'Cras justo odio'
      ], [
        { left: 'Chicken Foot Soup', right: '$2,000' },
        'Dapibus ac facilisis in',
        'Morbi leo risus',
        'Cras justo odio',
        'Cras justo odio'
      ], [
        { left: 'Chicken Foot Soup', right: '$2,000' },
        'Dapibus ac facilisis in',
        'Morbi leo risus',
        'Cras justo odio',
        'Cras justo odio'
      ], [
        { left: 'Chicken Foot Soup', right: '$2,000' },
        'Dapibus ac facilisis in',
        'Morbi leo risus',
        'Cras justo odio',
        'Cras justo odio'
      ], [
        { left: 'Chicken Foot Soup', right: '$2,000' },
        'Dapibus ac facilisis in',
        'Morbi leo risus',
        'Cras justo odio',
        'Cras justo odio'
      ]
    ]
  })
};
</script>
