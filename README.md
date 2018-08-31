# Vue-countdown-timer Component

<p>
  <a href="https://circleci.com/gh/TriDiamond/vuejs-countdown-timer/tree/master">
    <img src="https://img.shields.io/circleci/project/github/TriDiamond/vuejs-countdown-timer.svg" alt="Build Status">
  </a>
  <a href="https://github.com/TriDiamond/vuejs-countdown-timer/stargazers">
    <img src="https://img.shields.io/github/stars/TriDiamond/vuejs-countdown-timer.svg" alt="Github starts">
  </a>
  <a>
    <img src="https://img.shields.io/github/license/TriDiamond/vuejs-countdown-timer.svg" alt="License">
  </a>
  <a href="https://www.npmjs.com/package/vue-photoswipes">
    <img src="https://img.shields.io/npm/dt/vuejs-countdown-timer.svg" alt="Npm downloads">
  </a>
</p>

> 一 Vue 2 countdown and timer component

[📙中文文档](https://github.com/TriDiamond/vuejs-countdown-timer/blob/master/README_CN.md)

## Installation

``` bash
npm i vuejs-countdown-timer -S
```

## Usage

### Support

| Supported Package | Version |
|-------------------|---------|
| Vue               | 2.5+    |


### Install component

Javascript

``` javascript
// global register
import VueCountdownTimer from 'vuejs-countdown-timer'
Vue.use(VueCountdownTimer)

methods: {
  startCallBack: function (x) {
    console.log(x)
  },
  endCallBack: function (x) {
    console.log(x)
  }
}
```

Vue template

```vue
<vue-countdown-timer
  @start_callback="startCallBack('event started')"
  @end_callback="endCallBack('event ended')"
  :current-time="1481450106"
  :start-time="1481450110"
  :end-time="1481450115"
  :start-label="'Until start:'"
  :end-label="'Until end:'"
  label-position="begin"
  :end-text="'Event ended!'"
  :day-txt="'days'"
  :hour-txt="'hours'"
  :minutes-txt="'minutes'"
  :seconds-txt="'seconds'">
</vue-countdown-timer>
```

### Props

**current-time**
- `type`: Number
- `required` : false
- `default`: `new Date().getTime()`

**start-time**
- `type`: Number
- `required` : true

**end-time**
- `type`: Number
- `required` : true

**start-label**
- `type`: String
- `required` : false
- `default` : ''

**end-label**
- `type`: String
- `required` : false
- `default` : ''

**label-position** - begin (before countdown) / end (after countdown)
- `type`: String
- `required` : false
- `default` : 'begin'
    
**end-text**
- `type`: String
- `required` : false
- `default` : 'Event ended!'

**day-txt**
- `type`: String
- `required` : false
- `default` : ':'
    
**hour-txt**
- `type`: String
- `required` : false
- `default` : ':'

**seconds-txt**
- `type`: String
- `required` : false
- `default` : ':'

**seconds-fixed**
- `type`: String
- `required` : false
- `default` : ':'
    
### Events
**start_callback** - Event started callback
- `type`: Function
- `required` : false

**end_callback** - Event ended callback
- `type`: Function
- `required` : false
    
# Liscense
MIT License

Copyright (c) 2018 TriDiamond
