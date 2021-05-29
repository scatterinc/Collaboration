<template>
  <div>
    <h4 class="text-center">Making sidebar reusable</h4>
    <p class="text-center">
      This one is harder for me. The issue I have, is that I am unable to use
      the sidebar through components, similar to what I did for modal.- I want
      to reuse and pass different data through it.

      <b-row>
        <b-col class="text-center">
          <b-button @click="onClickOpenSideBar('buttonOne')" size="lg">
            This Works
          </b-button>
          <p class="text-center">
            When I embed the sidebar it works perfectly as you can see when you
            click this button.
          </p>
        </b-col>
        <b-col class="text-center">
          <b-button @click="onClickOpenSideBar('buttonTwo')" size="lg">
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
      <h1 style="color: red">
        HAHA - I GOT IT TO WORK. the only issue is the same as modal, how can i
        have one side bar, but two seperate information is displayed
      </h1>
    </div>
    <b-sidebar
      v-model="statusSideBarg"
      id="sidebar-right"
      title="Sidebar"
      right
      shadow
    >
      <div class="px-3 py-2">
        <p>
          {{ dataSideBar }}
        </p>
        <b-img
          src="https://picsum.photos/500/500/?image=54"
          fluid
          thumbnail
        ></b-img>
      </div>
    </b-sidebar>
  </div>
</template>
<script>
export default {
  name: "problemtwo",
  data() {
    return {
      statusSideBarg: false,
      dataSideBar: "",
    };
  },
  methods: {
    // function base when you click button , optionSideBar is option of button click
    // createdBy : HTHIEU (2021-05-29)
    onClickOpenSideBar(optionSideBar) {
      if (optionSideBar == "buttonOne") {
        // onclick button buttonOne
        this.dataSideBar = "Here SideBar One when you click button buttonOne!"; // update value dataSideBar
        this.statusSideBarg = !this.statusSideBarg;
      } else if (optionSideBar == "buttonTwo") {
        // onclick button buttonTwo
        this.dataSideBar = "Here SideBar Two when you click button buttonTwo!"; // update value dataSideBar
        this.statusSideBarg = !this.statusSideBarg;
      }
    },
  },
};
</script>
