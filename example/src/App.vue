<script setup>

import HelloWorld from './components/HelloWorld.vue';
import GlobalStyle from './components/GlobalStyle.vue';
import LocalStyle from './components/LocalStyle.vue';
import MyEvent from './components/MyEvent.vue';
import ReactiveCo from './components/ReactiveCo.vue';
import ReactivityConcept from './components/ReactivityConcept.vue';
import ForLoop from './components/ForLoop.vue';
import RefComponent from './components/RefComponent.vue';
import vif_show from './components/vif_show.vue';
import ProPs from './components/ProPs.vue';

// here is define compoent event code 

import CompoentEvent from './components/CompoentEvent.vue';

// import {ref} from 'vue'
// const count = ref(0)

const done = (user, email, password) => {
    console.log('username', user)
    console.log('email', email)
    console.log('password', password)
}

//  here is provide and inject method 

import { provide } from 'vue'
import ProvideInject from './components/ProvideInject.vue';
provide('game', {

    title: 'asdf',
    authoer: 'adff',
    book: 'asfghg',
    id: 55
})


// here Hook lifecycle code
import HookLifecycle from './components/HookLifecycle.vue';

</script>




<template>


    <HelloWorld />
    <GlobalStyle />
    <LocalStyle />
    <ReactiveCo />
    <MyEvent />
    <ReactivityConcept />
    <ForLoop />
    <RefComponent />
    <vif_show />
    <ProPs />

    <!-- // here is define compoent event code in which we use $emit in click class and in parent class access this $emit
    class through @ symbol like @($emit name) -->
    <h1>Count:{{count}}</h1>
<CompoentEvent @incrementCounter="count++"/>

    <!-- $Emit -->

    <CompoentEvent @userinfo="done" />

    <ProvideInject />


    <HookLifecycle />

</template>
