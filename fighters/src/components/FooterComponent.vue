<template>
    <footer id="footer-component">
        <p>
            {{copyright}}
            <br>
            {{fightersComponentTitle}}
        </p>
        <button v-on:click="changeRootSubTitle">
            Change fightersComponentTitle
        </button>
    </footer>    
</template>


<script>
    export default ({
        name: 'footer-component',

        props: {
            fightersComponentTitle : {
                type : String
            }
        },

        data() {
            return {
                copyright: 'Copyright 2022 - Vue Fighters'
            }
        },

        methods : {
            changeRootSubTitle() {
                this.$emit('footerTitleChange', 'The subTitle was changed on the Root by sending up an event from FooterComponent.vue')
            }
        }

    })
</script>

<style scoped>

    #footer-component {
        background-color: rgb(80, 35, 35);
        color: whitesmoke;
        padding: 1.25rem;
        margin:0;
    }

</style>