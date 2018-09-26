#### Rxjava2
subcribe()
onNext()
onError()
onComplete()
onTermital()
doOnSubscribe()
delaySubscription()
finalyDo()

基本认知：
subcribe()方法建立订阅关系，只有该方法执行后，才会开始发送事件
doOnSubscribe()建立订阅后，在发送之前执行，可以指定线程
onerror和onComplete中只有一个方法会被且仅被调一次，之后便会取消订阅关系。
delaySubscription().延迟订阅
subcribeOn():只有第一个有效，其他不执行
observerOn():都执行，最后一个有效决定下游执行的线程
onTermital():订阅被终止时，在onerror()和onComplete()方法之前执行
finalyDo():订阅完成后执行，在onerror()和oncomplete()之后执行