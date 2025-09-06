<template>
  <div class="content">
    <div class="md-layout ">
      
      
      <div class="md-layout-item md-medium-size-100 md-size-66">
        <add-payment-form  data-background-color="green"> </add-payment-form>
      </div>
     
      <!-- <div class="md-layout-item md-medium-size-100 md-size-33">
        <user-card> </user-card>
      </div> -->
    </div>
  </div>
</template>

<script>
import {  AddPaymentForm } from "@/pages";

export default {
  components: {
    
AddPaymentForm
  },
  data() {
    return {
      search:"0001234123",
      isSearchActive: false,
    };
  },
  methods: {
    toggleSearch() {
      this.isSearchActive = !this.isSearchActive;
    },
  },
};
</script>
