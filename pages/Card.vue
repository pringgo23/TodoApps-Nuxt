<template>
    <div>
        <Navbar/>
        <div class="bg-[#E9A6A6] h-screen">
          <div class=" flex justify-center p-4">
                  <div id="body-task" class="w-4/5 rounded-full flex justify-between ">
                      <p class="text-white text-sm p-1 ml-2"> What is your plan? </p>
                      <div class="flex items-center">
                          <button @click="showModal = true" id="btn-add" class="text-xs text-white ml-1 mr-1 rounded-full"
                              type="button"> Add </button>
                      </div>
                  </div>
                  <Modal v-show="showModal" @close-modal="showModal = false" @filterData = "btnFilter(activeFilter)" />
              </div>
              <div class="">
                  <div class="w-3 ml-11 flex">
                      <div>
                          <button @click="Ascending" id="btn-add" class="text-xs text-white ml-1 mr-1 rounded-full" type="button">
                              Asc </button>
                      </div>
                      <div>
                          <button @click="Descending" id="btn-add" class="text-xs text-white ml-1 mr-1 rounded-full ml-3"
                              type="button"> Desc </button>
                      </div>
                  </div>
                  <div class="mt-5 ml-11">
                      <form>
                          <label class="bg-[#864879] rounded-md p-1 text-white" for="card">Filter the Title:</label>
                          <select class="w-[50px] rounded" v-model="activeFilter">
                              <option  v-for="value in filters" :key="value" :value="value" :selected="value == 'a'">{{value}}</option>
                          </select>
                      </form>
                      <button @click="btnFilter(activeFilter)"  class="ml-11 mt-2 text-xs p-1 rounded bg-[#3F3351] text-white">Submit</button>
                  </div>
              </div>
      
              <div id="card-view" class="w-3/4">
              <div class="grid sm:grid-cols-12 md:grid-cols-3 md:gap-4">
                  <div id="wrap-card">
                      <div id="title" class="rounded-t-md h-10 mt-3 ">
                          <div class="flex justify-between p-2">
                              <h1 id="content-title" class="text-center text-white pl-9"
                                  >Ini judul</h1>
                              <div class="flex mr-2">
                                  <button class="text-green-500 mr-2" > V </button>
                                  <button  class="mr-2 text-white"> <img class="w-4 bg-white"
                                          src="../assets/edit.png" alt="edit" /> </button>
                                  <button class="text-red-500" > X </button>
                              </div>
                          </div>
                      </div>
                      <div id="description" class="rounded-b-md h-36 p-2">
                          <p id="para-desc" class="text-justify text-sm text-white ">Ini deskripsi</p>
                      </div>
                      
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
/* :style="{ 'text-decoration': (tugas.status ? 'line-through' : '') }" */
    #body-task {
    background-color: #864879;
}

#btn-add {
    background-color: #3F3351;
    width: 71px;
    height: 21px;
}

#card-view {
    margin: auto;
}

#title {
    background-color: #1F1D36;
}

#content-title {
    margin: auto;
}

#description {
    background-color: #864879;
}

#para-desc {
    display: -webkit-box;
    -webkit-line-clamp: 6;
    -webkit-box-orient: vertical;
    overflow: hidden;
}
</style>