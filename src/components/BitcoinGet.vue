<template name="bitcoin">

    <div v-if="info" id="teste">
        <h1>Bitcoin Quotation</h1>

        <div  v-for="currency in info" class="currency" :key="currency.id">
                 {{ currency.description }}:

            <span class="lighten">
                <span v-html="currency.symbol"></span>{{ currency.rate_float | currencydecimal }}
            </span>

        </div>

    </div>
</template>


<script>
    import axios from 'axios'

    export default {
        name: 'BitcoinGet',

        data() {
            return {
                info: null,
            }
        },
        mounted() {
            axios
                .get('https://api.coindesk.com/v1/bpi/currentprice.json')
                .then(response => (this.info = response.data.bpi))
                .catch(err => (console.log(err)))

        },
        filters: {
            currencydecimal(value) {
                return value.toFixed(2);
            }
        },

    }
</script>