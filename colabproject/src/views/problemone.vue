
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
        <b-button @click="onClickOpenDialog('Coding')" size="lg">
          Coding
        </b-button>
        <p>
          When I click on this button - I want the following to appear in the
          modal "I love coding"
        </p>
      </b-col>
      <b-col class="border-left">
        <b-button @click="onClickOpenDialog('Photography')" size="lg">
          Photography
        </b-button>
        <p>
          When I click on this button - I want the following to appear in the
          modal "I love Photography"
        </p>
      </b-col>
      <b-col>
        <b-button @click="onClickOpenDialog('Soccer')" size="lg">
          Soccer
        </b-button>
        <p>
          When I click on this button - I want the following to appear in the
          modal "I love soccer"
        </p>
      </b-col>
    </b-row>
    <b-row>
      <b-col class="text-center">
        I know i could have done a button group and lets code. but that is not
        the issue here. How to reuse a modal, and projecting different info in
        the modal.
      </b-col>
    </b-row>
    <b-modal
      v-model="statusDialog"
      id="modal-center"
      centered
      title="BootstrapVue"
    >
      <p class="my-4">{{ dataDialog }}</p>
    </b-modal>
  </div>
</template>
<script>
export default {
  name: "problemone",
  data() {
    return {
      statusDialog: false,
      dataDialog: "",
    };
  },
  methods: {
    // function base when you click button , optionDialog is option of button click ư
    // createdBy : HTHIEU (2021-05-29)
    onClickOpenDialog(optionDialog) {
      if (optionDialog == "Coding") {
        // onclick button Coding
        this.dataDialog = "Here Dialog Coding when you click button coding!"; // update value dataDialog
        this.statusDialog = !this.statusDialog;
      } else if (optionDialog == "Photography") {
        // onclick button Photography
        this.dataDialog =
          "Here Dialog Photography when you click button Photography!"; // update value dataDialog
        this.statusDialog = !this.statusDialog;
      } else if (optionDialog == "Soccer") {
        // onclick button Soccer
        this.dataDialog = "Here Dialog Soccer when you click button Soccer!"; // update value dataDialog
        this.statusDialog = !this.statusDialog;
      }
    },
  },
};
</script>
