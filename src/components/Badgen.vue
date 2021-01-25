<template>
    <div>
        <img :src="url" :alt="subject" :loading="loading" />
    </div>
</template>

<script>
export default {
    name: 'Badgen',
    props: {
        type: {
            type: String,
            default: 'classic'
        },
        subject: {
            type: String,
            default: 'vue-badgen'
        },
        status:  {
            type: String,
            default: '1.0.0'
        },
        color:  {
            type: String,
            default: 'green'
        },
        loading: {
            type: String,
            default: 'lazy'
        }
    },
    data() {
        return {
            url: ''
        }
    },
    methods: {
        generateBadge() {
            const typeUrl = this.type === 'flat' ? 'https://flat.badgen.net' : 'https://badgen.net';
            this.url = typeUrl + '/badge/' + this.subject + '/' + this.status + '/' + this.color;
        }
    },
    mounted: function () {
        this.generateBadge();
    }
};
</script>