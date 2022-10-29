<template>
    <div>
        <Navbar />
        <div id="body" class="flex justify-center items-center w-screen h-screen">
                <div class="w-[300px] h-auto p-3 bg-white rounded">
                    <div class="text-center mt-3  ">
                        <h1 class="font-semibold text-2xl subpixel-antialiased">Come Join Us!</h1>
                        <h3 class="font-normal text-base">Welcome, Please Fill Register Form !</h3>
            
                        <div class="mt-[50px]">
                            <form>
                                <p>
                                    <input class="w-[250px] border p-1 rounded" type="text" placeholder="Email" />
                                </p>
                                <p>
                                    <input class="w-[250px] border mt-3 p-1 rounded" type="password" placeholder="Password" />
                                </p>
                                <div>
                                    <button class="text-white bg-blue-700 hover:bg-blue-800 font-medium rounded text-sm px-5 py-2.5 mt-4 mr-2 mb-2 "> Register </button>
                                </div>
                                <div>
                                    <p class="font-base text-sm"> Already have account? <span class="text-[#2D4263]"> <button> Sign In </button> </span></p>
                                </div>
                            </form>
                        </div>
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
    #body{
        background-color: #E9A6A6;
    }
</style>