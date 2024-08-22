<script>

import axios from 'axios';

export default {



    name: 'FetchParantsMenu',

    data() {
        return {

        };
    },

    mounted() {

    },

    methods: {
        getParantsMenu: function () {
            axios.get('http://localhost:8080/menu')
                .then((result) => {
                    console.log(result.data)
                    var item = result.data.map((menu) => menu);
                    console.log(item)

                })
                .catch((error) => {
                    console.log(error)
                })
        },
    },
};
</script>



<template>
    <div>
        <Button label="get data" @click="getParantsMenu"></Button>
    </div>
</template>
