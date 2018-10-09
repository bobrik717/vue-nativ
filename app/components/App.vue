<template>
    <Page>
        <ActionBar title="Calculator" class="action-bar"/>
        <ScrollView>
            <ActionButtons class="action-buttons"></ActionButtons>
        </ScrollView>
    </Page>
</template>

<script>
    import ActionButtons from './ActionButtons';
    export default {
        components: {ActionButtons},
        data() {
            return {
                msg: 'Peace)))'
            }
        },
        methods: {
            onButtonTap(num) {
                console.log(num);
            },
        },
    }
</script>

<style scoped>
    ActionBar {
        background-color: #53ba82;
        color: #ffffff;
    }
    .action-buttons {
        position: fixed;
        bottom: 0;
        width: 100%;
    }
</style>
