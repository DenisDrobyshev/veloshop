<template>
    <footer class="footer">
        <div class="footer__copyright">{{ copyrightText }}</div>
    </footer>
</template>

<script>
export default {
    computed: {
        copyrightText() {
            const currentYear = new Date().getFullYear();
            return `2023-${currentYear}, VeloShop`;
        }
    }
}
</script>

<style lang="scss">
.footer {
    background: linear-gradient(#cee356, #52a5cc);
    padding: 10px;
    text-align: center;
    position: relative;
    bottom: 0;
    width: 100%;
    margin-top: auto;
}
</style>