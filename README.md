# touch-module
Mouse ve touch modülü devamlılık gerektiren olayları daha basit ve düzenli uygulamanıza imkan verir.

## Kullanımı

```html

touch("#eventItem",{
    start:function (event,helper) {
        //Başlarken yapmak istediğiniz komutlar
    },
    cancel:function (event,helper) {
        //İptal durumunda yapmak istediğiniz komutlar
    },
    move:function (event,helper) {
        //Sürükleme durumunda yapmak istediğiniz komutlar
    },
    end:function (event,helper) {
        //Sürükleme işlemi sonunda yapmak istediğiniz komutlar
    },
    leave:function (event,helper) {
        //Ayrılma durumunda yapmak istediğiniz komutlar
    },
});

```
### Helper parametresi
Helper parametresi ile x ve y koordinatında mouse yönünü, başlangıç, değişim ve son noktayı alabilirsiniz.Ayrıca `#eventItem`elemanına ulaşmak için `helper.trigger` ve `helper.clicked` ile event durumunu öğrenmek için kullanabilirsiniz...
```js
//başlarken...
helper.start.x // x 
helper.start.y // y 

//değişim...
helper.change.x // x 
helper.change.y // y 

//son...
helper.finish.x // x 
helper.finish.y // y 
```
