# 消息订阅与发布



- 订阅消息
  - 消息名，订阅消息
  - 发布消息

## 消息订阅-发布机制



### PubSub 

`````js
PubSubJs
npm i pubsub-js

import PubSub from 'pubsub-js'

`````

 

```js
// create a function to subscribe to topics
var mySubscriber = function (msg, data) {
    console.log( msg, data );
};

// add the function to the list of subscribers for a particular topic
// we're keeping the returned token, in order to be able to unsubscribe
// from the topic later on
var token = PubSub.subscribe('MY TOPIC', mySubscriber);

// publish a topic asynchronously
PubSub.publish('MY TOPIC', 'hello world!');//发布了消息

// publish a topic synchronously, which is faster in some environments,
// but will get confusing when one topic triggers new topics in the
// same execution chain
// USE WITH CAUTION, HERE BE DRAGONS!!!
PubSub.publishSync('MY TOPIC', 'hello world!');
```