<template>
    <tr>
        <td>{{coin.Cur_Abbreviation}}</td>
        <td>{{coin.Cur_Name}}</td>
        <td>{{coin.Cur_OfficialRate}}</td>
    </tr>
</template>
<script>
export default {
    props: {
        coin: {
            type: Object,
            required: true
        }
    },
    name: "CurrenciesItem"
}
</script>
