# TypeScript_study
TypeScript study in Lemonade DevTeam


### Compilation Context

### tsconfig
#### 최상위 프로퍼티
- compileOnSave
- extends
- compileOptions
- files
- include
- exclude
- references
- ~~typeAcquisition~~ 
- ~~tsNode~~

compileOnSave


extends
 온라인에서 증명된 tsconfig 가져와서 사용가능

files 가 제일 강력 include or exclude 보다!
[Uploading Screen Shot 2021-07-21 at 7.07.41 PM.png…]()

### Ch 06. Classes

#### 6-1.
- object를 만드는 blueprint(청사진, 설계도)
- 클래스 이전에 object를 만드는 기본적인 방법은 function
- javascript에도 class는 es6부터 사용 가능
- OOP를 위한 초석
- TypeScript에서 클래스도 사용자가 만드는 타입의 하나

#### 6-2.
- class 키워드를 이용하여 클래스를 만들 수 있다.
- class 이름으 보토 대문자를 이용한다.
- new 를 이용항 class를 통해 object르 만드 수 있다.
- constructor를 이용하여 object를 생성하면 값으 전달하 수 있다.
- this를 이용해 만들어진 object를 가리킬 수 있다.
- js로 컴파일되면 es5으 경우 function을 변경 된다.

#### 6-3. Constructor & Initialize
- 생성자 함수가 없으면, 디폴트 생성자가 불린다.
- 프로그래머가 만드 생성자가 하나라도 있으면, 디폴트 생성자는 사라진다.
- strict 모드에서는 프로퍼티를 선언하는 곳 또는 생성자에서 값을 할당해야 한다.
- 프로퍼티르 선언하는 곳 또는 생성자에 값을 할당하지 않는 경우에느 !를 붙혀서 위험을 표현한다.
- 클래스의 프로퍼티가 정의되어 있지만, 값을 대입하지 않으면 undefined이다.
- 생성자에는 async르 설정할 수 없다.

#### 6-4. Access Modifiers
- 접근 제어자에는 public, private, protected가 있다.
- 설정하지 않으면 public 
- 클래스 내부으 모든 곳에 (생성자, 프로퍼티, 메서드)설정 가능하다.
- private로 설정하면 클래스 외부엣 접근할 수 없다.
- js에서 private를 지원하지 않아 오랫동안 프로퍼티나 메서드 이름앞에 _를 붙혀 사용

#### 6-5. Initialization in Constructor Parameters
- contstructor의 parameter에 public 등을 사용해서 초기화 가능

#### 6-6. Getter & Setter
- get 함수를 사용해서 private property를 부를 수 있음
- set 함수로 property 변경 가능

#### 6-7. Readonly Properties
- public이여도 readonly면 변경 불가능, 조회만 가능
- 초기화 하는 영역에서만 값을 세팅 가능

#### 6-8. Index Signatures in Class
- 프로퍼티가 고정이 아닌 동적일 경우 사용 
```typescript
class Students {
 [index: string]: "male" | "female" 
}
```

#### 6-9. Static Properties & Methods
- 

#### 6-10. Singletons
- application 사용하는 동안 class에서 object를 1개만 생성해서 사용하는 패턴
- static을 매개체 역활을 하는 함수를 선언

#### 6-11. Inheritance
- 부모클래스를 extends로 상속 받을 수 있음
- 접근제어자도 덮어씌우기 가능
- constructor를 overriding 할 때에는 super()로 부모 constructor를 불러야 함

#### 6-12. Abstract Classes
- 기능이 완전하지 않은 클래스
- new 로 생성불가
- class에 extends해서 abstract 함수를 완전히 구현해서 사용 가능 

### Ch 07. Generics

#### 7-1. Difference of Generics and Any
- Generic은 타입 추론으로 알아서 타입이 정해짐

#### 7-2. Generics Basic
- 직접 <>안에 타입 지정하거나 지정 안해도 됨(타입추론)
- 복수로 설정 가능

#### 7-3. Generics Array and Tuple
- 배열 안에 한가지 타입이 아니여도 추론 가능
- 정해진 길이라면 Tuple로 하는게 정확함

#### 7-4. Generics Function
- 매개변수 앞에 선언해서 사용

#### 7-5. Generics Class
- 클래스네임 바로 뒤에 선언

#### 7-6. Generics with extends
- extends 사용 권장
 ```typescript
<T extends string | number> 같은 형식으로 generic의 타입을 제한 가능
```

#### 7-7. keyof & type lookup system
```typescript
getProp<T, K extends keyof T>(obj: T, key: K): T[K] {
 return onj[key];
};
extends와 generic을 사용하여 심화된 typesciprt 사용 가능
```
