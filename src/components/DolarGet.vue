<template name="bitcoin">
    <div  v-if="dolar" id="teste">
        <h1>Dollar Quotation to Real</h1>


        <div class="currency">Low: <span class="lighten">{{dolar.low | currencydecimalDolar}}</span></div>
        <div class="currency">High: <span class="lighten">{{dolar.high | currencydecimalDolar}}</span></div>
        <div class="currency">Date: <span class="lighten">{{dolar.create_date | dataSimplify}}</span></div>


    </div>
</template>


<script>
    import axios from 'axios'

    export default {
        name: 'DolarGet',
        data() {
            return {
                dolar: null,
            }
        },
        mounted() {
            axios
                .get('https://economia.awesomeapi.com.br/all/USD-BRL')
                .then(response => (this.dolar = response.data.USD))
                .catch(err =>(console.log(err)))

        },
        filters: {
            currencydecimalDolar(value) {
                return "$" + parseFloat(value).toFixed(2);
            },
            dataSimplify(value){
                return value.split(' ')[0].split('-').reverse().join('/')
                
            }
        },

    }
</script>

