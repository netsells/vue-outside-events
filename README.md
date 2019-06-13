[![npm version](https://badge.fury.io/js/%40netsells%2Fvue-outside-events.svg)](https://badge.fury.io/js/%40netsells%2Fvue-outside-events)
[![Build Status](https://travis-ci.com/netsells/vue-outside-events.svg?branch=master)](https://travis-ci.com/netsells/vue-outside-events)
[![codecov](https://codecov.io/gh/netsells/vue-outside-events/branch/master/graph/badge.svg)](https://codecov.io/gh/netsells/vue-outside-events)

# Vue Outside Events

Listen to events outside of the component

## Installation
```
yarn add @netsells/vue-outside-events
```

```javascript
import Vue from 'vue';
import OutsideEvents from '@netsells/vue-outside-events';

// register globally
Vue.component('OutsideEvents', OutsideEvents)

// or locally
export default {
  components: { OutsideEvents },
  // rest of your component
}
```

## Usage

```html
<outside-events @click="handleOutsideClick">
    Click somewhere else!
</outside-events>
```
