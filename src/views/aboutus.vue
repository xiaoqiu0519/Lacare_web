<template>
    <div class="aboutus">
        <div class="top_title"><img @click="gotoindex" class="lecrae_logo" src="../assets/h5_logo.png" alt srcset /></div>
        <div class="content">
            <img v-if="languagetype == 1" src="../assets/about_us_detail_ch.png" alt="" srcset="">
            <img v-else-if="languagetype == 2" src="../assets/about_us_detail_en.png" alt="" srcset="">
            <img v-else-if="languagetype == 3" src="../assets/about_us_detail_jp.png" alt="" srcset="">
        </div>
        <Footer></Footer>
    </div>
</template>
<script>
import Footer from '../views/Footer'
import {mapGetters} from 'vuex';
export default {
    components:{
        Footer
    },
    computed:{
        ...mapGetters(['languagetype'])
    },
    mounted(){
        
    },
    methods:{
        gotoindex(){
            this.$router.push('/home')
        }
    }
}
</script>
<style lang="stylus" scoped>
.content
    width 100%;
    img 
        width 100%;
        position relative;
        top -2px;
</style>