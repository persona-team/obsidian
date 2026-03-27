## <변수 선언>
```
// 타입 명시
String name = "승민";
int age = 24;
double height = 152.1;
bool isStudent = true;

// 타입 추론(var)
var name = "승민";  // Dart가 알아서 String으로 인식
// Dart의 var는 JS var와 달리 타입 고정이라 써도 괜찮음
```

## \<final VS. const>
```
final String name = "승민";  // 런타임에 값 결정, 한 번 정하면 변경 불가
const double pi = 3.14;  // 컴파일 타임에 값 결정, 완전 고정
```
- 둘 다 <span class="text-red">변경 불가</span>지만 const가 더 엄격
```
// final ⇒ 실행될 때 값이 정해져도 됨
final DataTime now = DateTime.now();  // 실행할 때마다 다른 값

// const ⇒ 코드 짤 때 이미 값이 확정되어야 함
const DateTime now = DateTime.now();  // 오류
const couble pi = 3.14;  // 코드 짤 때 이미 아는 값
```

## <함수>
```
// 기본 함수
int add(int a, int b) {
	return a + b;
}

// 한 줄 함수(=>)
int add(int a, int b) => a + b;
```

## <null 안정성>
```
String name = "승민";  // null 불가
String? name = null;  // ? 붙이면 null 가능
```
- Dart는 기본적으로 null 허용 안 함
- `?` 붙여야 null 가능

## <리스트/맵>
```
// 리스트(배열)
List<String> fruits = ["사과", "바나나", "딸기"];

// 맵(딕셔너리)
Map<String, int> scores = {
	"승민": 100,
	"영희": 90,
};
```

## <조건문/반복문>
```
// 조건문
if(age >= 20) {
	print("성인");
} else {
	print("미성년자");
}

// 반복문
for(int i = 0; i < 5; i ++) {
	print(i);
}

// for-in
for(String fruit in fruits) {
	print(fruit);
}
```

## <클래스>
```
class Person {
	String name;
	int age;
	
	// 생성자
	Person(this.name, this.age);
	
	void introduce() {
		print("안녕하세요, $name입니다!");
	}
}

// 사용
Person p = Person("승민", 24);
p.introduce();
```

## <문자열 안에 변수 넣기>
```
String name = "승민";
print("안녕하세요, $name!");  // 변수
print("내년엔 ${age + 1}살");  // 계산할 땐 {}
```

## <관습>
### 언더바(`_`) : 프라이빗
- 클래스 밖에서 접근 불가
```
int _counter = 0;  // 이 클래스 안에서만 사용
void _incrementCounter();  // 이 클래스 안에서만 사용
```

### 네이밍 규칙
```
// 클래스 ⇒ PascalCase(대문자 시작)
class MyHomePage {}
class UserProfile {}

// 변수/함수 ⇒ camelCase
int userAge = 24;
void getUserName() {}

// 상수 ⇒ lowerCamelCase(다른 언어랑 다름!)
const double pi = 3.14;  // Java처럼 PI 아님!

// 파일명 ⇒ snake_case
// main.dart
// user_profile.dart
```

### `this` 생략
```
class Person {
	String name;
	int age;
	
	// 다른 언어
	Person(String name, int age) {
		this.name = name;
		this.age = age;
	}
	
	// Dart 관습(this 생략)
	Person(this.name, this.age);
}
```

### `?`/`!`,`??`
```
String? name = null;  // ? = null 가능
print(name!);  // ! = "나는 null 아님을 보장해!"(위험할 수 있음)
String result = name ?? "기본값";  // ?? = null이면 기본값 사용
```

### 한 줄 함수
```
// Dart에서 자주 씀
int add(int a, int b) =>  a + b;
bool isAdult(int age) => age >= 18;
```

### `late` 키워드
```
late String name;  // 나중에 값 넣을게, 근데 null은 아님
// Flutter에서 initState()에서 초기화할 때 자주 씀
```

