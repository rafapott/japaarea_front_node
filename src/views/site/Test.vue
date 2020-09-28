<template>
  <div>

    teste: {{listData}}

  </div>
</template>

<script>

const axios = require('axios');

export default {
  name: 'Test',
  data () {
    return {
      backend_dir:"http://localhost:3000/",
      listData:[]
    }
  },
  async mounted(){
    let data = await this.teste();

    console.log('really data',data);
    this.$set(this,'listData',data);
  },
  methods: {
    async teste(){

      let data = await axios.get(this.backend_dir+'users/getAll');

      if(data.data){
        if(data.data.ok){
          return data.data.data;
        }
      }
    }
  }
}

</script>
