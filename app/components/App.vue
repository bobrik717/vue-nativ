<template>
    <Page>
        <ActionBar title="Calculator" class="action-bar"/>
        <ScrollView>
            <FlexboxLayout flexWrap="wrap" height="100%">
                <StackLayout height="50%">
                    <TextView editable="false">
                        <FormattedString>
                            <Span v-bind:text="viewStack()" />
                        </FormattedString>
                    </TextView>
                </StackLayout>
                <ActionButtons height="50%" :on-button-tap="onButtonTap"></ActionButtons>
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
                stack: [],
            }
        },
        methods: {
            onButtonTap(num) {
                this.stack.push(num);
            },
            viewStack() {
                let str = '';
                for(let i in this.stack) {
                    str += this.stack[i];
                }
                return str;
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
