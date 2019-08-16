<template>
    <div class="row">
     <div class="col-lg-12 col-md-12">
         <div class="progress">
                 <div class="progress-bar" role="progressbar" :style="{width:(quoteCount / maxQuotes * 100 + '%')}">
                     {{ quoteCount }}/{{ maxQuotes }}
                     </div>
         </div>

         </div>
     </div>
</template>

<script>

export default {
    props: ['quoteCount', 'maxQuotes']
}
</script>

<style scoped>

</style>