<template>
  <div id="body-navbar" >
        <div class="flex justify-center">
            <div  class="flex justify-between w-11/12 m-1 ">
                <div class="w-24 leading-tight">
                    <p class="text-white text-center text-sm"> Your Todo Apps</p>
                </div>
                <div class="text-white text-center text-sm flex p-4" >
                    <NuxtLink to="/Card"> Home</NuxtLink>
                    <NuxtLink to="/Register" class="ml-4"> Register</NuxtLink>
                    <NuxtLink to="/" class="ml-4"> Login</NuxtLink>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
    #body-navbar{
        background-color: #1F1D36;
    }
</style>