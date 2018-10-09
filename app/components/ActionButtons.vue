<template>
    <FlexboxLayout flexWrap="wrap">
        <Button text="1" width="25%" @tap="onTap(1)" />
        <Button text="2" width="25%" @tap="onTap(2)" />
        <Button text="3" width="25%" @tap="onTap(3)" />
        <Button text="-" width="25%" @tap="onTap('-')" />
        <Button text="4" width="25%" @tap="onTap(4)" />
        <Button text="5" width="25%" @tap="onTap(5)" />
        <Button text="6" width="25%" @tap="onTap(6)" />
        <Button text="+" width="25%" @tap="onTap('+')" />
        <Button text="7" width="25%" @tap="onTap(7)" />
        <Button text="8" width="25%" @tap="onTap(8)" />
        <Button text="9" width="25%" @tap="onTap(9)" />
        <Button text="*" width="25%" @tap="onTap('*')" />
        <Button text="0" width="75%" @tap="onTap(0)" />
        <Button text="/" width="25%" @tap="onTap('/')" />
    </FlexboxLayout>
</template>

<script>
    export default {
        name: "ActionButtons",
        props: ['onButtonTap'],
        methods: {
            onTap(num) {
                this.onButtonTap(num);
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