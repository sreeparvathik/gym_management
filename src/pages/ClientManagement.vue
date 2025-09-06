<template>
  <div class="content">
    <div class="md-layout ">
       <md-field>
        <label>Search client by phone number</label>
        <md-input v-model="search" type="text" ></md-input>
         <!-- <md-icon @click=toggleSearch>search</md-icon> -->
         
      </md-field>
      <md-button @click=toggleSearch>
           {{ isSearchActive ? "Close Search" : "Search Client" }}
          </md-button>
      
      <div class="md-layout-item md-medium-size-100 md-size-66">
        <edit-profile-form v-if="isSearchActive" data-background-color="green"> </edit-profile-form>
      </div>
      <div class="md-layout-item md-medium-size-100 md-size-66">
        <add-profile-form data-background-color="blue"> </add-profile-form>
      </div>
      <!-- <div class="md-layout-item md-medium-size-100 md-size-33">
        <user-card> </user-card>
      </div> -->
    </div>
  </div>
</template>

<script>
import { EditProfileForm,AddProfileForm ,UserCard } from "@/pages";

export default {
  components: {
    EditProfileForm,
    AddProfileForm,
    // UserCard,
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
