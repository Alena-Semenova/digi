<template>
    <span role="img" aria-hidden="true" :style="config">
        <slot></slot>
    </span>
</template>

<script>

export default {
    name: 'IconWrapper',
    props: {
        color: String,
        width: {
            type: String,
            required: false,
        },
        height: {
            type: String,
            required: false,
        },
    },

    computed: {
        config() {
            return {
                color: this.color,
                width: this.width,
                height: this.height,
                display: 'inline-flex',
                fontSize: 'inherit',
            }
        }
    }

}




</script>