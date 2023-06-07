---
title: "[swiftUI] Event(이벤트 처리) - Button, onDisappear"
categories: [ios]
comments: true
---

책 [SwiftUI 기반의 Ios 프로그래밍]을 토대로 공부한 내용입니다.<br><br>

---

1. Button(버튼)으로 기본적인 이벤트 처리

```swift
struct ContentView: View{
    var body: some View{
        Button(action:ButtonPressed){
            Text("Click me")
        }
    }

    func buttonPressed(){
        // 동작할 코드
    }
}
```
<br>
위와 같이 액션 함수를 지정하는 대신, 버튼 클릭시 실행될 코드를 클로저로 지정할 수도 있음.
<br>

```swift
struct ContentView: View{
    var body: some View{
        Button(action: {
            //동작할 코드
        }) {
            Text("Click me")
        }
    }
}
```
<br>

다음은 Image 뷰를 버튼으로 만드는 경우.<br>

```swift
struct ContentView: View{
    var body: some View{
        Button(action: {
            print("hello")
        }) {
            Image(systemName: "square.and.arrow.down")
        }
    }
}
```
<br><br><br>

2. onAppear, onDisappear 메서드
```swift
struct ContentView: View{
    var body: some View{
        Text("hello, World!")
        .onAppear(perform: {
            //뷰가 나타날 때 수행되는 코드
        })
        .onDisappear(perform: {
            //뷰가 사라질 때 수행되는 코드
        })
    }
}
```
<br><br><br>

3. 커스텀 컨테이너 뷰 만들기

추후 추가예정
