## MVVM概念
#### MVVM分为三个部分
  > 分别是M（Model，模型层 ），V（View，视图层），VM（ViewModel，V与M连接的桥梁，也可以看作为控制器）
  > 1. M：模型层，主要负责业务数据相关；
  > 2. V：视图层，顾名思义，负责视图相关，细分下来就是html+css层；
  > 3. VM：V与M沟通的桥梁，负责监听M或者V的修改，是实现MVVM双向绑定的要点；
  > MVVM支持双向绑定，意思就是当M层数据进行修改时，VM层会监测到变化，并且通知V层进行相应的修改，反之修改V层则会通知M层数据进行修改，以此也实现了视图与模型层的相互解耦；

## v 视图层
```
    <form class="form">
      <p>name:<input type="text" class="name" name="name"></p>
      <p>age:<input type="text" class="age" name="age"></p>
    </form>
```
## m 模型层
```
      let person = {
        _data: {
          name: '',
          age: '',
        },
      }
```
## vm 控制器
```
    function binding(obj, key) {
      let dom = document.querySelector(`.${key}`);
      Object.defineProperty(obj, key, {
        get() {
          // 获取模型层数据
          return obj._data[key];
        },
        set(v) {
          // 设置显示层内容
          dom.value = v;
          // 设置模型层数据
          obj._data[key] = v;
          console.log(`person.${key}: `, v);
        },
      });
    }

    Object.keys(person._data).forEach(function(k) {
      binding(person, k);
    });

    document.querySelector('.form').addEventListener('input', (e) => {
      let value = e.target.value;
      let name = e.target.getAttribute('name');
      person[name] = value;
    });
```
