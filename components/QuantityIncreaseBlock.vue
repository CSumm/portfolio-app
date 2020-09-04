<template>
<div>
<span>Qty: </span>
    <Select :options="options"/>
        </div>
</template>

<script>
export default {
    props: {
        options: Array
    },
    data: {
        options: [lorem,lorem,lorem,lorem,lorem]
    }
}
</script>