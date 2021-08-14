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
- OOP를 위하 초석
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

#### 6-6. Getter & Setter

#### 6-7. Readonly Properties

#### 6-8. Index Signatures in Class

#### 6-9. Static Properties & Methods

#### 6-10. Singletons

#### 6-11. Inheritance

#### 6-12. Abstract Classes

### Ch 07. Generics
