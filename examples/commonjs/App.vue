<template>
    <div>
        <star-rating :round-start-rating="false" :decrement="1" @rating-decrement="getDecrement" v-model="rating"/>
        <a href="#">Reset</a>
        Rating selected: {{ratingSelected}}
    </div>
</template>
<script type="text/javascript">
import StarRating from '../../src/star-rating.vue';

export default {
    components: {
        StarRating
    },
    methods: {
        getDecrement(rat) {
            this.ratingSelected = rat
        }
    },
    created() {

    },
    data() {
        return {
            ratingSelected: null,
            rating: 0
        }
    }
}
</script>
