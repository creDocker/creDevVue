<template>  
  <div class="elemFirst">
    {{ msg }}-{{ counter }}
    <button @click="addOne">
      Add
    </button>
    -{{ c4uUid }}
    <slot />
  </div>
</template>
 
<style scoped>
  .elemFirst {
    background: red;
  }
</style>

<script>
//  import C4uGlue from "./C4uGlue2.js";
  import C4uGlue from "c4u-glue";
 
  export default {
    mixins: [C4uGlue], 
    props: {msg: {type: String, default: '1st'}},
    data: function() {
           return {
            c4uParentTag: "c4u-also-to-be-defined",
            counter: 0,
            }
        },
    methods: { 
       // eslint-disable-next-line
       addOne: function(ignoreEvent) {
          this.counter += 1;
       },
    },
//    created() {
//         console.log("***** Elem-1st-created #" + this.c4uUid);
//    },
//    mounted() {
//         console.log("***** Elem-1st-mounted #" + this.c4uUid);
//    },
//    updated() {
//         console.log("***** Elem-1st-updated #" + this.c4uUid);
//    },
//    beforeDestroy() {
//         console.log("***** Elem-1st-destroyed #" + this.c4uUid);
//    },

  }
</script>
