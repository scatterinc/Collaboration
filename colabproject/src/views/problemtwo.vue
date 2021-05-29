<template>
  <div>
    <h4 class="text-center">Making sidebar reusable</h4>
    <p class="text-center">
      This one is harder for me. The issue I have, is that I am unable to use
      the sidebar through components, similar to what I did for modal.- I want
      to reuse and pass different data through it.

      <b-row>
        <b-col class="text-center">
          <b-button v-b-toggle.sidebar-right size="lg"> This Works </b-button>
          <p class="text-center">
            When I embed the sidebar it works perfectly as you can see when you
            click this button.
          </p>
        </b-col>
        <b-col class="text-center">
          <b-button v-b-toggle.sidebar-right size="lg">
            I need this to work
          </b-button>
          <p class="text-center mr-4">
            However I want to use the same sidebar for multiple issues how i go
            about, rendering it accross multiple views?
          </p>
        </b-col>
      </b-row>
          </p>
          <div>
              <h1 style="color:red">
              HAHA - I GOT IT TO WORK. the only issue is the same as modal, 
          how can i have one side bar, but two seperate information is displayed</h1>
          </div>
  </div>
</template>
