<template>

  <!-- Swatch 1 -->
  <div>
    <div v-if="variation.color_options.hex_value.length == 1" v-on:mouseover="changeFeature(variation, variationId)" @click="changeFeatureImageOnClick(variation, variationId)"
      class="color-swatch m-auto s-20" :style="{ 'background-color': variation.color_options.hex_value[0] }"
      data-toggle="tooltip" data-placement="top" :title="variation.color_options.option_value"></div>

    <!-- Swatch 2 -->
    <div v-if="variation.color_options.hex_value.length == 2" v-on:mouseover="changeFeature(variation, variationId)" @click="changeFeatureImageOnClick(variation, variationId)"
      class="color-swatch m-auto s-20" :style="{ 'background-color': variation.color_options.hex_value[1] }"
      data-toggle="tooltip" data-placement="top" :title="variation.color_options.option_value">
      <div class="combination-swatch " :style="{ 'background-color': variation.color_options.hex_value[0] }"></div>
    </div>

    <!-- Swatch 3 -->
    <div v-if="variation.color_options.hex_value.length == 3" v-on:mouseover="changeFeature(variation, variationId)" @click="changeFeatureImageOnClick(variation, variationId)"
      class="color-swatch m-auto s-20" :style="{ 'background-color': variation.color_options.hex_value[1] }"
      data-toggle="tooltip" data-placement="top" :title="variation.color_options.option_value">
      <div class="combination-swatch " :style="{ 'background-color': variation.color_options.hex_value[0] }"></div>
      <div class="combination-swatch swatch3" :style="{ 'background-color': variation.color_options.hex_value[2] }">
      </div>
    </div>

    <!-- Swatch 4 -->
    <div v-if="variation.color_options.hex_value.length == 4" v-on:mouseover="changeFeature(variation, variationId)" @click="changeFeatureImageOnClick(variation, variationId)"
      class="color-swatch m-auto s-20" :style="{ 'background-color': variation.color_options.hex_value[1] }"
      data-toggle="tooltip" data-placement="top" :title="variation.color_options.option_value">
      <div class="combination-swatch " :style="{ 'background-color': variation.color_options.hex_value[0] }"></div>
      <div class="combination-swatch swatch3" :style="{ 'background-color': variation.color_options.hex_value[2] }">
      </div>
      <div class="combination-swatch swatch4" :style="{ 'background-color': variation.color_options.hex_value[3] }">>
      </div>
    </div>

    <!-- Swatch 5 -->
    <div v-if="variation.color_options.hex_value.length == 5" v-on:mouseover="changeFeature(variation, variationId)" @click="changeFeatureImageOnClick(variation, variationId)"
      class="color-swatch m-auto s-20" :style="{ 'background-color': variation.color_options.hex_value[1] }"
      data-toggle="tooltip" data-placement="top" :title="variation.color_options.option_value">
      <div class="combination-swatch " :style="{ 'background-color': variation.color_options.hex_value[0] }"></div>
      <div class="combination-swatch swatch3" :style="{ 'background-color': variation.color_options.hex_value[2] }">
      </div>
      <div class="combination-swatch swatch4" :style="{ 'background-color': variation.color_options.hex_value[3] }">>
      </div>
      <div class="combination-swatch swatch5" :style="{ 'background-color': variation.color_options.hex_value[4] }">>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  props: [
    'variation',
    'variationId'
  ],
  methods: {
    changeFeature(variation, variationId) {
      let payload = {
        variation: variation,
        variation_id: variationId
      }
      this.$emit('changeFeatureImage', payload)
    },
    changeFeatureImageOnClick(variation, variationId) {
      let payload = {
        variation: variation,
        variation_id: variationId
      }
      this.$emit('changeFeatureImageOnClick', payload)
    },
  }

}
</script>

<style>
</style>
