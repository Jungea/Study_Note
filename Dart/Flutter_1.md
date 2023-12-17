
- children : 위젯 여러개 / child 위젯 한 개

## Text 위젯
- 글자를 적고 스타일링
```Dart
Text(
	'Hello Flutter~!',
	style: TextStyle(
		fontSize: 16.0,
		fontWeight: FontWeight.w700,
		color: Colors.blue,
	),
),
```

---
## 제스처 관련 위젯
- 사용자가 키보드로 글자를 입력하는 행위 외의 모든 입력

### Button 위젯
- TextButton : 텍스트만 있는 버튼
- OutlinedButton : 테두리가 있는 버튼
- ElevatedButton : 입체적으로 튀어나온 느낌의 배경이 들어간 버튼

### IconButton 위젯
- [Icons 클래스](https://api.flutter.dev/flutter/material/Icons-class.html)

### GestureDetector 위젯
- 손가락 입력을 인지하는 위젯
- [제스처 매개변수](https://api.flutter.dev/flutter/widgets/GestureDetector-class.html)

### FloatingActionButton 위젯
- 플로팅 버튼

---
## 디자인 관련 위젯
- 디자인적 요소 적용
- 배경, 간격, 패딩...

### Container 위젯
- 너비, 높이, 배경, 테두리

### SizedBox 위젯
- 일정 크기의 공간을 공백으로 둘 때
- const 생성자 사용 시

### Padding 위젯
- 내부 간격 추가
- margin : Container위젯에 추가

### SafeArea 위젯
- 노치 디자인을 가리지 않는 화면에만 위젯을 그림

---
## 배치 관련 위젯

### Row 위젯
- 가로로

### Column 위젯
- 세로로

### Flexible 위젯


### Expanded 위젯
- Flexible 위젯을 상속
- FlexFit.tight 기본 제공


