

## 클래스
```Dart
void main() {
  Idol blackPink = Idol('블랙핑크', 
                        4);
  blackPink.sayName();
  blackPink.secret = 'pinkHi';
  print(blackPink.secret);
  
  Idol bts = Idol.fromMap({
    'name' :'BTS',
    'membersCount' : 7,
  });
  bts.sayName();
  print(bts.secret);
  
  GirlGroup redvelvet = GirlGroup('레드벨벳', 4);
  redvelvet.sayName();
}

class Idol {
  final String name;
  final int membersCount;
  String _secret = '1';

  Idol(this.name, this.membersCount);
  
  Idol.fromMap(Map<String, dynamic> map) 
    : name = map['name'],
  membersCount = map['membersCount'];
  
  String get secret {
    return _secret;
  }
  
  set secret(String secret) {
    _secret = secret;
  }
  
  void sayName() {
    print('저는 $name 입니다. 멤버는 $membersCount명 입니다.');
  }
}

class GirlGroup extends Idol {
  
  GirlGroup(super.name, super.membersCount);
  
  @override
  void sayName() {
    print('저희는 여자 아이돌 $name입니다.');
  }
}
```

## 믹스인
- 클래스의 일부 기능만 상속
```Dart
void main() {
  Idol blackPink = Idol('블랙핑크', 4);
  
  BoyGroup bts = BoyGroup('BTS', 7);
  bts.sing();
}

class Idol {
  final String name;
  final int membersCount;

  Idol(this.name, this.membersCount);

  void sayName() {
    print('저는 $name 입니다.');
  }
  
  void sayMembersCount() {
    print('멤버는 $membersCount명 입니다.');
  }
}

mixin IdolSingMixin on Idol {
  void sing() {
    print('$name이 노래를 부릅니다.');
  }
}

class BoyGroup extends Idol with IdolSingMixin {
  BoyGroup(super.name, super.membersCount);
  
  void sayMale() {
    print('저는 남자 아이돌입니다.');
  }
}
```

## 캐스케이드 연산자
- ..
```Dart
void main() {
  Idol blackPink = Idol('블랙핑크', 4)
	  ..sayName()
	  ..sayMembersCount();
  
}
```

