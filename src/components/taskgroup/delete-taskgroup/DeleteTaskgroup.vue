<template>
  
</template>

<script>
import { deleteTaskgroupApi } from "./../../../services/api";
export default {
  props: ["id"],
  mounted: function() {
    deleteTaskgroupApi(this.id).then(response => {
     
      this.$router.push({name: "listTaskgroup"});
      
    });
  }
};
</script>