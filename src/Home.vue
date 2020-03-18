<template>
        <p class="homeText">
            ACCOUNT OWNER VUE.JS APP
        </p>
</template>

<script>
import OwnerService from '@/api-services/owner.service';
 
export default {
  name: 'Home',
  created() {
    OwnerService.getAll().then((response) => {
      console.log(response.data);
    }).catch((error) => {
      console.log(error.response.data);
    });
  }
};
</script>
<style scoped>
.homeText {
    font-size: 35px;
    color: blue;
    text-align: center;
    position: relative;
    top: 30px;
    text-shadow: 2px 2px 2px gray;
}
</style>