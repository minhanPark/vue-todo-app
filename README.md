# vue-todo

> Vue로 만든 투두 앱입니다.

vue로 만든 투두앱의 모습입니다.
![vue-todo](https://user-images.githubusercontent.com/29043491/85940688-d29d3480-b958-11ea-9c19-441a97d04b3c.PNG)

## 프로젝트 시작하기

vue는 점진적으로 프로젝트에 사용될 수 있도록 만들어졌다. 그래서 적용하는 법도 아주 쉽다.

```html
<!-- development version -->
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>

<!-- production version -->
<script src="https://cdn.jsdelivr.net/npm/vue"></script>
```

해당 스크립트 태그를 상황에 맞게 넣으면 뷰를 사용할 수 있다.

```html
<div id="app">
    {{message}}
</div>
```

```js
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
})
```

공식 문서에 나와 있는 내용이다. 위의 태그(id가 app인 div)에 Vue 인스턴스를 연결시키면 된다. data에 정의한 message에 접근한 것을 볼 수 있다.

## Vue 인스턴스에 추가할 수 있는 것

> 1. 라이프 사이클 메소드
> 2. 데이터
> 3. watch
> 4. computed

### 라이프 사이클 알아보기

라이프 사이클 메소드는 생성과정, 갱신과정, 소멸과정이라는 라이프 사이클(생명주기)에서 상황에 따라 실행되는 메소드이다.  
생성과정은 beforeCreate - created - beforeMount - mounted이고, 갱신과정은 beforeUpdate - updated다.  
소멸과정은 beforeDestroy - destroyed이다.  

### watch
데이터값이 변할 때마다 메소드를 실행시킬 수 있는데 해당 메소드가 watch이다. 

```js
watch:{
    dataName: function(){}
}

```
형태로 사용하면 된다.

### computed

html 태그안에 자바스크립트 계산식 등 코드를 넣을 수 있지만 복잡한것은 computed를 활용해서 값을 만들어 내는 것이 좋다. 기존의 참조하고 있던 데이터가 바뀌면 자동으로 바뀌고, 아니면 캐싱을 사용해서 기존에 계산한 값을 가져오기 때문에 속도면에서 아주 좋다.