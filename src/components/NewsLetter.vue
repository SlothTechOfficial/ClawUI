<template>
    <section class="newsletter">
        <img :src="source">
        <div class="newsletter__subscription">
            <div class="newsletter__title">Stay Updated</div>
            <div class="newsletter__subtitle"> Give a brief reason for people to subscribe to newsletter</div>
            <div class="newsletter__subscribe">
                <span class="newsletter__container">
                    <input class="newsletter__text" type="email" v-model="email">
                </span>
                <button class="button--primary secondary" @click="submit()">  Subscribe
                </button> 
            </div>   
        </div>
    </section>
</template>

<script>
export default {
    name: 'NewsLetter',
    data () {
        return {
            email:'',
            source:'https://images.pexels.com/photos/1109543/pexels-photo-1109543.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
        }
    },
    methods: {
        submit () {
            this.email =''
        }
    }
}
</script>
