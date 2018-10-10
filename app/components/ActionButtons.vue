<template>
    <FlexboxLayout flexWrap="wrap">
        <FlexboxLayout flexWrap="wrap" width="100%" v-for="row in values" v-bind:text="value">
            <Button v-for="value in row" v-bind:text="value" v-bind:width="getWidth(row)" @tap="onTap(value)" />
        </FlexboxLayout>
    </FlexboxLayout>
</template>

<script>
    export default {
        name: "ActionButtons",
        props: ['onButtonTap'],
        data() {
            return {
                values: [
                    ['C', 'DEL', '%', '/'],
                    ['7', '8', '9', 'X'],
                    ['4', '5', '6', '-'],
                    ['1', '2', '3', '+'],
                    ['( )', '0', '.', '='],
                ],
            };
        },
        methods: {
            onTap(num) {
                this.onButtonTap(num);
            },
            getWidth(row) {
                return (100 / row.length) + '%';
            }
        },
    }
</script>

<style scoped>
    Button{
        font-weight: bold;
        color: white;
        background-color: #53ba82;
        border-radius: 1px;
        border-width: 7px;
        border-color: coral;
    }
</style>