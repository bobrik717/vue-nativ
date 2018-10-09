<template>
    <FlexboxLayout flexWrap="wrap">
        <Button text="1" width="25%" @tap="onButtonTap(1)" />
        <Button text="2" width="25%" @tap="onButtonTap(2)" />
        <Button text="3" width="25%" @tap="onButtonTap(3)" />
        <Button text="-" width="25%" @tap="onButtonTap('-')" />
        <Button text="4" width="25%" @tap="onButtonTap(4)" />
        <Button text="5" width="25%" @tap="onButtonTap(5)" />
        <Button text="6" width="25%" @tap="onButtonTap(6)" />
        <Button text="+" width="25%" @tap="onButtonTap('+')" />
        <Button text="7" width="25%" @tap="onButtonTap(7)" />
        <Button text="8" width="25%" @tap="onButtonTap(8)" />
        <Button text="9" width="25%" @tap="onButtonTap(9)" />
        <Button text="*" width="25%" @tap="onButtonTap('*')" />
        <Button text="0" width="75%" @tap="onButtonTap(0)" />
        <Button text="/" width="25%" @tap="onButtonTap('/')" />
    </FlexboxLayout>
</template>

<script>
    export default {
        name: "ActionButtons"
    }
</script>

<style scoped>

</style>