<template>
    <div class="welcome mt-10">
        <v-row>
            <v-col cols="12">
                <div>
                    <h2 class="main_title animation_backInLeft">
                        Your 
                    </h2>
                </div>
                <div> 
                   <h2 class="main_title">
                        Front-end 
                    </h2>  
                </div>
                <div>
                    <h2 class="main_title">
                        Developer 
                    </h2>
                </div>
                <div class="mt-8">
                    <p class="main_text mb-0">
                        My name is Nikolay Moroka
                    </p>
                    <p class="main_text mb-0">
                        I will create the best website for your buisness
                    </p>
                </div>
            </v-col>
            <v-col cols="12" class="mt-n7">
                <img width="80%" src="../assets/programmer.png" alt="programer">
            </v-col>
        </v-row>
        
    </div>
</template>

<script>
export default {
    name: 'Welcome',
    data:() => ({

    }),
}
</script>

<style scoped>
.main_title, .main_text {
    color: white;
}

.main_title {
    font-size: 65px;
    line-height: 1.2;
    letter-spacing: 2px;
    font-weight: 400;
    text-transform: uppercase;
    font-family: 'PT Sans', sans-serif !important;
}
.main_text {
    font-size: 22px;
    font-family: 'PT Sans', sans-serif !important;
    line-height: 1.33;
    letter-spacing: 1px;
}

</style>