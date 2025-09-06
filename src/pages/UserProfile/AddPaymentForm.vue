<template>
  <form>
    <md-card>
      <md-card-header :data-background-color="dataBackgroundColor">
        <h4 class="title">Add Payment Information</h4>
        <!-- <p class="category">Add a new client</p> -->
      </md-card-header>

      <md-card-content>
        <div class="md-layout">
         <!-- asdf{{ isUserFetched }} -->
          <div class="md-layout-item md-small-size-100 md-size-100">
            <md-field>
              <label>Phone Number</label>
              <md-input v-model="phonenumber" type="text"></md-input>
            </md-field>
          </div>
          <div class="md-layout-item md-small-size-100 md-size-100" >
          <md-button @click="toggleUserFetch">Fetch User</md-button>
          </div>
       <div class="md-layout" v-if="isUserFetched">
          <div class="md-layout-item md-small-size-100 md-size-33">
            <md-field>
              <label>Name</label>
              <md-input disabled v-model="name" type="email"></md-input>
            </md-field>
          </div>
          <div class="md-layout-item md-small-size-100 md-size-30">
            <md-field>
              <label>Date Of Birth</label>
              <md-input disabled v-model="dob" type="text"></md-input>
            </md-field>
          </div>
          
          <div class="md-layout-item md-small-size-100 md-size-30">
            <md-field>
              <label>Address</label>
              <md-input disabled v-model="address" type="text"></md-input>
            </md-field>
          </div>
          <div class="md-layout-item md-small-size-100 md-size-30">
            <md-field>
              <label>Address</label>
              <md-input disabled v-model="address" type="text"></md-input>
            </md-field>
          </div>
         
          <md-card>
            <md-card-header :data-background-color="dataBackgroundColor">
              <h4 class="title">Last Gym memebership Payment Details</h4>
              <!-- <p class="category">Add a new client</p> -->
            </md-card-header>

            <md-card-content>
              <div class="md-layout">
              <!-- asdf{{ isUserFetched }} -->
                <div class="md-layout-item md-small-size-100 md-size-50">
                  <md-field>
                  
                    <label>Start Date</label>
                    <md-input disabled v-model="start_date" type="text"></md-input>
                  </md-field>
                </div>
                <div class="md-layout-item md-small-size-100 md-size-50">
                  <md-field>
                    <label>End Date</label>
                    <md-input disabled v-model="end_date" type="text"></md-input>
                  </md-field>
                  </div>

                <div class="md-layout-item md-size-100 text-right">
                  <md-button class="md-raised md-success">renew Gym memebership </md-button>
                </div>
               
                </div>
             
            </md-card-content>
         </md-card>

          <md-card>
            <md-card-header :data-background-color="dataBackgroundColor">
              <h4 class="title">Last PT membership Payment Details</h4>
              <!-- <p class="category">Add a new client</p> -->
            </md-card-header>

            <md-card-content>
              <div class="md-layout">
              <!-- asdf{{ isUserFetched }} -->
                <div class="md-layout-item md-small-size-100 md-size-50">
                  <md-field>
                  
                    <label>Start Date</label>
                    <md-input disabled v-model="start_date" type="text"></md-input>
                  </md-field>
                </div>
                <div class="md-layout-item md-small-size-100 md-size-50">
                  <md-field>
                    <label>End Date</label>
                    <md-input disabled v-model="end_date" type="text"></md-input>
                  </md-field>
                  </div>

                <div class="md-layout-item md-size-100 text-right">
                  <md-button class="md-raised md-success">renew PT  </md-button>
                </div>
               
                </div>
             
            </md-card-content>
         </md-card>


        </div></div>
        </md-card-content>
    </md-card>
  </form>
</template>
<script>
export default {
  name: "edit-profile-form",
  props: {
    dataBackgroundColor: {
      type: String,
      default: "",
    },
  },
  data() {
    return {
      phonenumber: "00123123123",
      isUserFetched: false,
      name: "Abdul",
      disabled: null,
      dob: "12-12-1212",
      address: "kochi, kerala",
      start_date: "19-09-2024",
      end_date: "19-10-2024",
      // address: null,
      city: null,
      country: null,
      code: null,
      aboutme:
        "Lamborghini Mercy, Your chick she so thirsty, I'm in that two seat Lambo.",
    };
  },
  methods: {
    toggleUserFetch() {
      this.isUserFetched = !this.isUserFetched;
    },
  },
};
</script>
<style></style>
