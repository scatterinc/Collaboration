/* eslint-disable prettier/prettier */
/* eslint-disable prettier/prettier */
<template>
  <div>
    <b-row class="mb-2">
      <b-col class="mb-4 text-center">
        <h5>
          When I click on each button, I want different stuff to show on the
          modal. (i think this is V slot am not sure?) Need your help to walk me
          through this. Or mock it up so I can follow:
        </h5>
      </b-col>
    </b-row>
    <b-row class="mt-2">
      <b-col class="border-left">
        <b-button v-b-modal.modal-center size="lg"> Coding </b-button>
        <p>When I click on this button - I want the following to appear in the modal "I love coding"</p>
      </b-col>
       <b-col class="border-left">
        <b-button v-b-modal.modal-center size="lg"> Photography </b-button>
        <p>When I click on this button - I want the following to appear in the modal "I love Photography"</p>
 
      </b-col>
      <b-col>
        <b-button v-b-modal.modal-center size="lg"> Soccer </b-button>
        <p>When I click on this button - I want the following to appear in the modal "I love soccer"</p>
 
      </b-col>
    </b-row>
    <b-row>
      <b-col class="text-center">
I know i could have done a button group and lets code. but that is not the issue here. How to reuse a modal, and projecting different info in the modal.
      </b-col>
    </b-row>
  </div>
</template>
