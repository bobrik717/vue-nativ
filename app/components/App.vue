<template>
    <Page>
        <ActionBar title="Calculator" class="action-bar"/>
        <ScrollView>
            <FlexboxLayout flexWrap="wrap" height="100%">
                <StackLayout height="65%">
                    <TextView editable="false">
                        <FormattedString>
                            <Span v-bind:text="msg" />
                        </FormattedString>
                    </TextView>
                </StackLayout>
                <ActionButtons height="35%" :on-button-tap="onButtonTap"></ActionButtons>
            </FlexboxLayout>
        </ScrollView>
    </Page>
</template>

<script>
    import ActionButtons from './ActionButtons';
    export default {
        components: {ActionButtons},
        data() {
            return {
                msg: '',
            }
        },
        methods: {
            onButtonTap(num) {
                this.msg += '' + num;
            },
        },
    }
</script>

<style scoped>
    ActionBar {
        background-color: #53ba82;
        color: #ffffff;
    }
</style>
