<template>
    <div ref="container">
        <global-events
            :filter="notInContainer"
            v-on="$listeners"
        />
        <slot />
    </div>
</template>

<script>
    import GlobalEvents from 'vue-global-events';

    export default {
        name: 'outside-events',

        components: {
            GlobalEvents,
        },

        methods: {
            /**
             * Check the event wasn't triggered in the container
             *
             * @param {Event} event
             *
             * @returns {Boolean}
             */
            notInContainer({ target }) {
                const { container } = this.$refs;

                return (
                    container !== target
                    && !container.contains(target)
                );
            },
        },
    };
</script>
