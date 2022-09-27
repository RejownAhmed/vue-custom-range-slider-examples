<script setup>
import { ref, watch } from 'vue'
import customRangeSlider from './components/customRangeSlider.vue'
const value = ref(0)
const defaultPosition = ref(0.4)
</script>

<template>
<h3>Hover Over the sliders and pull/click/drag to see it working</h3>
<p>NOTE: YOU MUST PASS AN UNIQUE ID PROP. WITHOUT IT YOU CANNOT USE THE SLIDER MULTIPLE TIMES. IT IS MADE REQUIRED </p>
<div>
  <p >Example 1:</p>
  <span>
      <customRangeSlider id="one"></customRangeSlider>
  </span>
</div>
<div>
  <p>Example 2 (Using v-model): We use v-model to get the percent value. Then based on the value you can easily calculate the volume/video/audio progress position</p>
  <span>
        <customRangeSlider id="two" v-model="value"></customRangeSlider>
  </span>
    <div>
      Percent Value Calculation: {{100*value}}%(E.g:100*value)
  </div>
</div>
<div>
  <p>Example 3: Setting a default Position. Just use v-model and pass a default value to the reactive variable</p>
  <span>
        <customRangeSlider v-model="defaultPosition"></customRangeSlider>
  </span>
</div>
<div>
  <p>Example 4: Show the thumb indicator always</p>
  <span>
        <customRangeSlider  
          always-show-thumb 
          thumb-height="500%"><!--Height set to bigger to show properly-->
        </customRangeSlider>
  </span>
</div>
<div>
  <p>Example 5: Expand on hover like youtube. Hover over the slider to see it.</p>
  <span>
        <customRangeSlider 
          expand-on-hover><!--Height set to bigger to show properly-->
        </customRangeSlider>
  </span>
</div>
<div>
  <p>Example 6: No Preview Bar. Hover over the slider to see it.</p>
  <span>
        <customRangeSlider 
          id="six" 
          no-preview-bar
          always-show-thumb 
          expand-on-hover
          thumb-height="500%"><!--Height set to bigger to show properly-->
        </customRangeSlider>
  </span>
</div>
<div>
  <p>Example 7: No thumb Indicator. Hover/Click/Drag the slider to see it.</p>
  <span>
        <customRangeSlider 
          no-thumb 
          expand-on-hover><!--Height set to bigger to show properly-->
        </customRangeSlider>
  </span>
</div>
<div>
  <p>Example 8: No Progress Bar. Drag or click any parts to see it.</p>
  <span style='width: 40%'>
        <customRangeSlider 
          no-progress-bar
          expand-on-hover
          always-show-thumb><!--Height set to bigger to show properly-->
        </customRangeSlider>
  </span>
</div>
<div>
  <p>Example 9: Customizig Colors and other things.</p>
  <span style='width: 40%'>
        <customRangeSlider 
          thumb-height="500%"
          range-height="10px"
          range-container-height="20px"
          thumb-color="skyblue"
          progress-color="yellow"
          range-bg-color="blue"
          preview-color="red" 
          expand-on-hover
          always-show-thumb><!--Height set to bigger to show properly-->
        </customRangeSlider>
  </span>
</div>
</template>
