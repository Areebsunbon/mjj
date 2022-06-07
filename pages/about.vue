<template>
  <div class="about-page">
      <h1>About Hello MJJ</h1>
      <p>This is an app</p>
  </div>

</template>
 <script>
export default {
    head(){
        return {
            title: "About Us",
            meta: [
                {
                    hid: 'description',
                    name: 'Description',
                    content: 'This is an app'
                }           
            ]
        }
    }

}; 
</script>
