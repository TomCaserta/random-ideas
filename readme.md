# Random Ideas

This is literally a collection of random ideas I can think of some of them things I want to be available or stuff I want to make. They may not make sense without context, they may already exist in some form or they may not even work past the 'theory stage'. This is simply things I will personally try out over time.

### JS

## Server that sends down only what is required

A lot of the code we write today is asynchronous, it doesn't matter if a function returns immediately or 1s from now, our code will still work. The first idea is to write a JS transformer that can detect code that runs inside a promise and simply does not send it to the client until it needs it. 

When this code is accessed it can send a packet over websockets to request the code its supposed to run, after it has run that code it resolves the promise. This essentially gives us code splitting without a lot of the hassle of figuring out what can be code split. It may be slower but this is just an idea and would be beneficial to see if in every day code there is a performance increase or too much of an overhead.

### Vue

## Compiler that can compile natively to Web Components

Right now Vue can target web components. To be honest it doesn't do it in the best way, it simply clones slot contents and doesn't set attributes if they are not set after the component has been loaded. There are forks that solve this issue such as @gig/vue-web-component-wrapper. 

This works but in my opinion doesn't solve a lot of problems. In an ideal world if you wanted to compile a vue component to a web component you would not need to run Vue at all. The framework is somewhat close to Web Components themselves and in theory you could somewhat easily convert Vue code native JS. What I mean by that is something that is similar to what svelte does. It should be possible to have components that have no runtime requirement of Vue itself.



