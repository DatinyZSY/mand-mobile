<template>
  <div class="md-example selecotor">
    <section class="md-example-section" v-for="(demo, index) in demos" :key="index">
      <div class="md-example-title" v-html="demo.title"></div>
      <div class="md-example-describe" v-html="demo.describe"></div>
      <div class="md-example-content">
        <component :is="demo"></component>
      </div>
    </section>
	</div>
</template>

<script>import createDemoModule from '../../../examples/create-demo-module'
import Demo0 from './cases/demo0'
import Demo1 from './cases/demo1'
import Demo2 from './cases/demo2'
import Demo3 from './cases/demo3'

export default {...createDemoModule('selecotor', [Demo0, Demo1, Demo2, Demo3])}
</script>

<style lang="stylus">
.md-example-child-selecotor
  .md-field-item-custom-title
    font-weight font-weight-medium
    text-align center
  .md-field-item-custom-brief
    font-size font-minor-normal
    text-align center
</style>