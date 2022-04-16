<template>
    <footer id="footer-component">
        <p>
            {{copyright}}
        </p>
    </footer>    
</template>


<script>
    export default ({
        name: 'footer-component',

        data() {
            return {
                copyright: 'Copyright 2022 - Vue Fighters'
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