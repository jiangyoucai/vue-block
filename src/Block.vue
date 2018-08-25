<template>
    <article class="bgf b-border p-absolute o-auto" :class="size" v-show="show">
        <slot name="block"></slot>
    </article>
</template>
<script>
export default {
    props: ["show", "size"],
    data() {
        return {}
    }
}
</script>
<style scoped></style>