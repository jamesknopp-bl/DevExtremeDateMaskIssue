<script setup>
import {ref} from 'vue'
import DxDateBox from 'devextreme-vue/date-box'

const value = ref(new Date());

</script>
<template>
  <div>
    <h2 class="content-block">Home</h2>
    <div class="content-block">
      <div class="dx-card responsive-paddings">
        <DxDateBox label="Date with mask" v-model="value" display-format="dd/MM/yyyy HH:mm" type="datetime" :use-mask-behavior="true" />
        <br />
        <div class="instructions">
          <p>Steps to replicate issue:</p>
          <ol>
            <li>Set the time to 00:00 using the keyboard</li>
            <li>Set the minutes to 01 using the keyboard</li>
            <li>Left mouse click into the hours and type in 1</li>            
          </ol>        
          <p>Expected result: 01:01<br />
            Actual result: 11:01</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss"></style>
