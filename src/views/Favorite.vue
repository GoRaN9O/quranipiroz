<template>
  <div class="favorite">
    <search />
    <div class="section_content" v-if="!logged">
          <div class="no_login_msg">
            پێویستە سەرەتا خۆت تۆمار بکەیت! 
          </div>
    </div>
    <div class="section_content"  v-if="logged">
          <div class="no_login_msg">
            هیچ شتێک بەردەست نییە
          </div>
    </div>
  </div>
</template>

<script>
  import Search from '@/components/global/Search';
  import {mapState} from 'vuex';
  
  export default {
    name: 'Favorite',
    components: {Search},
    computed: {
      ...mapState(['logged', 'user'])
    }
  }
</script>
