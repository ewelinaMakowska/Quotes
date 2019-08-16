<template>
    <div class="row">
        <div class="col-lg-12 col-md-8">
            <form>
             
                 <label>Quote</label><br>
              
                 <textarea rows="3" v-model="quote"></textarea><br>

               
                 <button @click.prevent="createNewQuote">Add Quote</button>
                
            </form>
           

        </div>

        <div class="col-lg-8 col-m-8">
            
        </div>
    </div>
</template>

<script>
export default {
    data: function() {
        return {
               quote: ''
        };
    },
        methods: {
            createNewQuote() {
               // console.log(this.quote);
                this.$emit('quoteEmitted', this.quote);
                this.quote = '';
               // console.log('New Quote!');
            }
        }    
    }

</script>

<style scoped>
.form-wrapper {
    text-align: center
}

form {
    width: 90%;
    margin-left: 5%;
    text-align: center
}

label {
    text-align: center
}

textarea {
    resize: none;
    height: 30vh;
    width: 100%;
}



button {

}
</style>