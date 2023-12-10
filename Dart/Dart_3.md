
## 비동기
```Dart
void main() async {
  final result = await addNumbers(1, 1);
  print('결과값 = $result');
  
  final result2 = await addNumbers(2, 2);
  print('결과값 = $result2');
}

Future<int> addNumbers(int number1, int number2) async {
  print('$number1 + $number2 계산 시작!');

  await Future.delayed(Duration(seconds: 3), () {
    print('$number1 + $number2 = ${number1 + number2}');
  });
  
  print('$number1 + $number2 코드 실행 끝');
  
  return number1 + number2;
}
```


![Future vs Stream](../images/img_20231210143458.png)

