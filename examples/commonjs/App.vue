<template>
    <div>
        <star-rating :round-start-rating="false" :decrement="1" v-model="ratingSelected"/>
        <a href="#" @click.prevent="rating = 3.5">Reset</a>
        Rating selected: {{ratingSelected}}
    </div>
</template>
<script type="text/javascript">
import StarRating from '../../src/star-rating.vue';

export default {
    components: {
        StarRating
    },
    created() {
       setTimeout(() => {
            this.rating = 3.5
        }, 1000)

    },
    data() {
        return {
            ratingSelected: null,
            rating: 0
        }
    }
}
</script>
