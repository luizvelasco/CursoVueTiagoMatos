<template>
    <div>
        <h1 v-if="$slots.title">
            <slot name="title" />
        </h1>
        <div>
            <slot name="description" />
        </div>
        <div>
            <slot />
        </div>
    </div>
</template>

<script>
export default {
    name: 'SlotComponents',
    mounted(){
        console.log(this.$slots);
    }
}
</script>