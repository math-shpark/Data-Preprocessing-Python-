# 1. Number, Text, Bit

# Chapter 1. 수, 텍스트, 비트

## 1.1 변수

### 1.1.1 변수

- 변수
    - 데이터를 담는 메모리 공간
- 변수 예시
    
    ```python
    >>> a = 2020
    >>> a
    2020
    >>> b = a + 3030
    >>> b
    5050
    >>> a = a - 20
    >>> a
    2000
    ```
    

## 1.2 수 다루기

### 1.2.1 정수

- 정수
    - 음의 정수, 0, 양의 정수를 모두 통틀어 일컫는 말
    - python에서는 메모리가 허용한 무한대의 정수를 다룰 수 있음
- 정수 입력 예시
    
    ```python
    >>> a = 3
    >>> b = 123456789
    >>> c = 1234567890123456789012345678901234567890
    >>> a
    3
    >>> b
    123456789
    >>> c
    1234567890123456789012345678901234567890
    ```
    
- 음수 입력 예시
    
    ```python
    >>> d = -1234567890123456789012345678901234567890
    >>> e= -123456789
    >>> f = -3
    >>> d
    -1234567890123456789012345678901234567890
    >>> e
    -123456789
    >>> f
    -3
    ```
    
- 변수의 형식
    - python은 코드가 실행될 때 변수의 형식 결정
    - 예시
        
        ```python
        >>> f = -3
        >>> type(f)
        <class 'int'>
        ```
        
- 정수의 사칙 연산
    - 더하기 : `+`
    - 빼기 : `-`
    - 곱하기 : `*`
    - 나눗셈의 몫 구하기 : `//`
    - 나눗셈의 나머지 구하기 : `%`
    - 나누기 : `/`
- 정수의 사칙 연산 예시
    1. 덧셈
        
        ```python
        >>> a = 3 + 4
        >> a
        7
        ```
        
    2. 뺄셈
        
        ```python
        >>> b = 7 - 10
        >>> b
        -3
        ```
        
    3. 곱셈
        
        ```python
        >>> c = 7 * -3
        >>> c
        -21
        ```
        
    4. 나눗셈
        
        ```python
        >>> d = 30 // 7
        >>> d
        4
        >>> e = 30 % 7
        >>> e
        2
        >>> f = 22 / 7
        >>> f
        3.142857142857143
        >>> type(f)
        <class 'float'>
        ```
        

### 1.2.2 실수

- 부동 소수형
    - 컴퓨터로 소수의 소수점을 표현하는 방식 중 하나
    - 소수점을 움직여서 소수를 표현하는 자료형
    - 부동 소수형은 8byte만을 이용해서 수를 표현
        
        ⇒ 한정된 범위의 수만 표현 가능
        
    - 디지털 방식으로 소수를 표현해야 하므로 정밀도에 한계가 있음
- 부동 소수형 예시
    
    ```python
    >>> a = 3.14
    >>> a
    3.14
    >>> type(a)
    <class 'float'>
    >>> b = 22 / 7
    >>> b
    3.142857142857143 #정수를 정수로 나누어도 만들어짐
    >>> type(b)
    <class 'float'>
    ```
    

### 1.2.3 복소수

- 복소수
    - $a\pm bi$의 꼴로 나타낼 수 있는 수
    - $a$와 $b$는 실수
    - $i$는 허수 단위로 $i^2=-1$을 만족
    - 켤레 복소수는 복소수 중 허수 부분의 부호가 반대인 복소수
- 복소수 예시
    
    ```python
    >>> a = 2 + 3j    #python에서는 허수 단위 부호로 j를 사용
    >>> a
    (2+3j)
    >>> type(a)
    <class 'complex'>
    >>> a.real    #복소수 a의 실수부
    2.0
    >>> a.imag    #복소수 a의 허수부
    3.0
    >>> a.conjugate()   #복소수 a의 켤레 복소수
    (2-3j)
    ```
    

### 1.2.4 math 모듈을 이용한 계산

- 모듈
    - python 코드를 담고 있는 `.py` 확장자를 가진 파일
    - python은 인터프리터와 함께 매우 다양한 모듈 제공
    - 모듈을 사용하려면 `import` 구문 이용
- math 모듈
    - python은 사칙 연산자 말고도 다양한 계산 수단을 제공
    - 제곱 연산, 로그 연산, 삼각 함수 계산을 수행하는 연산자와 함수를 제공
    - 많은 수학 함수가 math 모듈에 정리되어 있음
    - 구현 코드
        
        ```python
        >>> import math
        ```
        
- $\pi$와 $e$
    
    ```python
    >>> math.pi   #원주율
    3.141592653589793
    >>> math.e   #자연상수
    2.718281828459045
    ```
    
- 절댓값, 버림, 반올림
    1. 절댓값
        - 함수 : `abs()`
        - 내장 함수
        - 예시
            
            ```python
            >>> abs(10)
            10
            >>> abs(-10)
            10
            ```
            
    2. 반올림
        - 함수 : `round()`
        - 내장 함수
        - 예시
            
            ```python
            >>> round(1.4)
            1
            >>>round(1.5)
            2
            ```
            
    3. 버림
        - 함수 : `trunc()`
        - math 모듈
        - 예시
            
            ```python
            >>> import math
            >>> math.trunc(1.4)
            1
            >>> math.trunc(1.5)
            1
            >>> math.trunc(1.9)
            1
            ```
            
- 팩토리얼
    - 1부터 어떤 양의 정수 $n$까지의 정수를 모두 곱한 것
    - 함수 : `factorial()`
    - 예시
        
        ```python
        >>> import math
        >>> math.factorial(1)
        1
        >>> math.factorial(5)
        120
        >>> math.factorial(10)
        3628800
        ```
        
- 도와 라디안
    1. 도
        - 원을 360도로 표현한 것
        - 함수 : `degrees()`
        - 예시
            
            ```python
            >>> import math
            >>> math.degrees(math.pi)
            180.0
            >>> math.degrees(math.pi/2)
            90.0
            ```
            
    2. 라디안
        - 반지름이 1인 원에서 호의 길이가 1인 부채꼴의 각을 기본단위로 삼는 것
        - 함수 : `radians()`
        - 예시
            
            ```python
            >>> import math
            >>> math.radians(180)
            3.141592653589793
            <<< math.radians(90)
            1.5707963267948966
            ```
            
- 삼각함수
    1. 코사인 : `cos()`
    2. 사인 : `sin()`
    3. 탄젠트 : `tan()`
    4. 코사인 역함수 : `acos()`
    5. 사인 역함수 : `asin()`
    6. 탄젠트의 역함수 : `atan()`
- 삼각함수 예시
    
    ```python
    >>> import math
    >>> math.sin(math.radians(90))
    1.0
    >>> math.cos(math.radians(180))
    -1.0
    >>> math.tan(math.radians(45))
    0.9999999999999999
    >>> math.acos(-1)
    3.141592653489793
    >>> math.asin(1.0)
    1.570963267948966
    >>> math.atan(10000)
    1.5706963267952299
    ```
    
- 제곱과 제곱근
    1. 제곱
        - 함수 : `**`, `pow()`
        - 예시
            
            ```python
            >>> 3 ** 3
            27
            >>> import math
            >>> math.pow(3,3)
            27.0
            ```
            
    2. 제곱근
        - 함수 : `sqrt()`
        - 예시
            
            ```python
            >>> import math
            >>> math.sqrt(4)
            2.0
            ```
            
            - 세제곱근, 네제곱근 등은 $x^{\frac{1}{n}}=\sqrt[n]{x}$ 성질 이용
- 로그
    - `log()` : 첫 번재 매개변수의 로그를 구하고, 두 번째 매개변수는 밑(생략 시 $e$로 간주)
    - `log10()` : 밑이 10인 로그 계산
    - 예시
        
        ```python
        >>> import math
        >>> math.log(4,2)
        2.0
        >>> math.log(math.e)
        1.0
        >>> math.log10(1000)
        3.0
        ```
        

## 1.3 텍스트 다루기

### 1.3.1 문자열 데이터

- 문자열 데이터
    - 작은따옴표(') 또는 큰따옴표(")의 쌍으로 텍스트를 감싸서 표현
    - 여러 줄로 이루어진 문자열은 작은따옴표 3개(''') 또는 큰따옴표 3개(""")의 쌍으로 텍스트를 감싸서 표현
    - 예시
        
        ```python
        >>> a = 'Hello, World.'
        >>> a
        'Hello, World'
        >>> b = "안녕하세요"
        >>> b
        '안녕하세요.'
        >>> c = '''어서와
        파이썬은
        처음이지?'''
        >>> c
        '어서와\n파이썬은\n처음이지?'
        >>> d = """Welcome to
        Python."""
        >>>
        'Welcome to\nPython.'
        >>> type(d)
        <class 'str'>   #str은 Python의 문자열 형식 이름
        ```
        
- 문자열 연결
    - `+` 연산자 사용
        
        ```python
        >>> hello = 'Hello'
        >>> world = 'World'
        >>> hello_word = hello + ', ' + world
        >>> hello_word
        'Hello, World'
        ```
        
- 문자열 분리(Slicing)
    - 대괄호 연산자 사용
        
        ```python
        >>> s = 'Good Morning'
        >>> s[0:4]   #문자열 s의 0번째 문자부터 4번째 문자 앞까지를 분리
        'Good'
        ```
        
    - 문자열 뿐만 아니라 다른 순서열 자료형에서도 이용 가능
    - 슬라이싱을 수행해도 원본은 유지
        
        ```python
        >>> a = 'Good Morning'
        >>> b = a[0:4]
        >>> c = a[5:12]
        >>> a
        'Good Morning'
        >>> b
        'Good'
        >>> c
        'Morning'
        ```
        
    - 문자열의 처음부터 슬라이싱을 하면 첫 번째 매개변수는 생략 가능
    - 문자열의 마지막까지 슬라이싱을 하면 두 번째 매개변수는 생략 가능
    - 특정 위치에 있는 문자 참조 가능
        
        ```python
        >>> a = 'Good Morning'
        >>> a[0]
        'G'
        >>> a[8]
        'n'
        ```
        
- 문자열 확인
    - `in` 연산자는 프로그래머가 원하는 부분이 문자열 안에 존재하는지 확인
    - 존재하면 `True`, 그렇지 않으면 `False`
    - 예시
        
        ```python
        >>> a = 'Good Morning'
        >>> 'Good' in a
        True
        >>> 'X' in a
        False
        ```
        
- 문자열 길이
    - 함수 : `len()`
    - 예시
        
        ```python
        >>> a = 'Good Morning'
        >>> len(a)
        12
        ```
        

### 1.3.2 문자열 메소드

- 문자열 메소드
    1. `startswith()`
        - 원본 문자열이 매개변수로 입력한 문자열로 시작되는지 판단
        - 결과는 `True` 또는 `False`
        - 예시
            
            ```python
            >>> a = 'Hello'
            >>> a.startswith('He')
            True
            >>> a.startswith('lo')
            False
            ```
            
    2. `endswith()`
        - 원본 문자열이 매개변수로 입력한 문자열로 끝나는지를 판단
        - 결과는 `True` 또는 `False`
        - 예시
            
            ```python
            >>> a = 'Hello'
            >>> a.endswith('He')
            False
            >>> a.endswith('lo')
            True
            ```
            
    3. `find()`
        - 원본 문자열 안에 매개변수로 입력한 문자열이 존재하는 위치를 앞에서부터 찾음
        - 존재하지 않으면 -1을 결과로 출력
        - 예시
            
            ```python
            >>> a = 'Hello'
            >>> a.find('ll')
            2
            >>> a,find('H')
            0
            >>> a.find('K')
            -1
            ```
            
    4. `rfind()`
        - 원본 문자열 안에 매개변수로 입력한 문자열이 존재하는 위치를 뒤에서부터 찾음
        - 존재하지 않으면 -1을 결과로 출력
        - 예시
            
            ```python
            >>> a = 'Hello'
            >>> a.rfind('H')
            0
            >>> a.rfind('lo')
            3
            >>> a.rfind('M')
            -1
            ```
            
    5. `count()`
        - 원본 문자열 안에 매개변수로 입력한 문자열이 몇 번 등장하는지 출력
        - 예시
            
            ```python
            >>> a = 'Hello'
            >>> a.count('l')
            2
            ```
            
    6. `lstrip()`
        - 원본 문자열 왼쪽에 있는 공백 제거
        - 예시
            
            ```python
            >>> '         Left Strip'.lstrip()
            'Left Strip'
            ```
            
    7. `rstrip()`
        - 원본 문자열 오른쪽에 있는 공백 제거
        - 예시
            
            ```python
            >>> 'Right Strip        '.rstrip()
            'Right Strip'
            ```
            
    8. `strip()`
        - 원본 문자열 양쪽에 있는 공백 제거
        - 예시
            
            ```python
            >>> '              Strip                 '.strip()
            'Strip'
            ```
            
    9. `isalpha()`
        - 원본 문자열이 숫자와 기호를 제외한 알파벳(영문, 한글 등)으로만 이루어져 있는지 출력
        - 예시
            
            ```python
            >>> 'ABCDefgh'.isalpha()
            True
            >>> '123ABC'.isalpha()
            False
            ```
            
    10. `isnumeric()`
        - 원본 문자열이 숫자로만 이루어져 있는지 출력
        - 예시
            
            ```python
            >>> '1234'.isnumeric()
            True
            >>> '123ABC'.isnumeric()
            False
            ```
            
    11. `isalnum()`
        - 원본 문자열이 알파벳과 수로만 이루어져 있는지 출력
        - 예시
            
            ```python
            >>> '1234ABC'.isalnum()
            True
            >>> '1234'.isalnum()
            True
            >>> 'ABC'.isalnum()
            True
            >>> '1234 ABC'.isalnum()
            False
            ```
            
    12. `replace()`
        - 원본 문자열에서 찾고자 하는 문자열을 바꾸고자 하는 문자열로 변경
        - 예시
            
            ```python
            >>> a = 'Hello, World'
            >>> b = a.replace('World', 'Korea')
            >>> a
            'Hello, World'
            >>> b
            'Hello, Korea'
            ```
            
    13. `split()`
        - 매개변수로 입력한 문자열을 기준으로 원본 문자열을 나눠 리스트를 만듦
        - 예시
            
            ```python
            >>> a = 'Apple, Orange, Kiwi'
            >>> b = a.split(',')
            >>> b
            ['Apple', 'Orange', 'Kiwi']
            >>> type(b)
            <class 'list'>
            ```
            
    14. `upper()`
        - 원본 문자열을 모두 대문자로 바꾼 문자열 출력
        - 예시
            
            ```python
            >>> a = 'lower case'
            >>> b = a.upper()
            >>> a
            'lower case'
            >>> b
            'LOWER CASE'
            ```
            
    15. `lower()`
        - 원본 문자열을 모두 소문자로 바꾼 문자열 출력
        - 예시
            
            ```python
            >>> a = 'UPPER CASE'
            >>> b = a.lower()
            >>> a
            'UPPER CASE'
            >>> b
            'upper case'
            ```
            
    16. `format()`
        - 형식을 갖춘 문자열을 만들 때 사용
        - 문자열 안에 중괄호 `{ }`로 다른 데이터가 들어갈 자리를 만들어 두고 `format()` 함수를 호출할 때 이 자리에 들어갈 데이터를 순서대로 넣어주면 원하는 형식의 문자열을 만들어 낼 수 있음
        - 예시
            
            ```python
            >>> a = 'My name is {0}. I am {1} years old.'.format('Mario',40)
            >>> a
            'My name is Mario. I am 40 years old.'
            >>> b = 'My name is {name}. I am {age} years old.'.format(name='Luigi', age=35)
            >>> b
            'My name is Luigi. I am 35 years old.'
            ```
            

## 1.4 수에서 텍스트로, 텍스트에서 수로

### 1.4.1 input 함수

- 내장 함수 input
    - 사용자로부터 입력을 받아들여 프로그램에게 전달
    - 전달하는 데이터의 형식이 문자열
    - 예시 1
        
        ```python
        a = input()
        b = input()
        result = a * b     #a와 b는 문자열이기 때문에 수행할 수 없음
        ```
        
    - Python은 숫자 형식의 생성자 안에 문자열을 해당 형식으로 변환하는 기능을 탑재했음
        
        ⇒ `int('12345')`의 꼴로 문자열을 정수로 변환할 수 있음
        
    - 예시 2
        
        ```python
        >>> int('1234567890')
        1234567890
        >>> float('123.4567')
        123.4567
        >>> complex('1+2j')
        (1+2j)
        ```
        

### 1.4.2 형식 변환 실습

- 실습
    
    <input_multiply.py>
    
    ```python
    print("첫 번째 수를 입력하세요. : ")
    a = input()
    print("두 번째 수를 입력하세요. : ")
    b = input()
    
    result = int(a) * int(b)
    
    print("{0} * {1} = {2}".format(a, b, result))
    ```
    
- 실습 결과
    
    ```python
    첫 번째 수를 입력하세요. : 
    5
    두 번째 수를 입력하세요. : 
    4
    5 * 4 = 20
    ```
    

## 1.5 비트 다루기

### 1.5.1 시프트 연산자

- 시프트 연산자
    1. `<<` : 왼쪽 시프트 연산자
        - 첫 번째 피연산자의 비트를 두 번째 피연산자의 수만큼 왼쪽으로 이동
    2. `>>` : 오른쪽 시프트 연산자
        - 첫 번째 피연산자의 비트를 두 번째 피연산자의 수만큼 오른쪽으로 이동
- 예시 1
    
    ```python
    >>> a = 240     #00000000 11110000
    >>> a
    240
    >>> a << 2     #00000011 11000000  2는 옮길 비트의 수
    960
    >>> a >> 2     #00000000 00111100
    60
    ```
    
- 예시 2
    
    ```python
    >>> a = 1
    >>> hex(a)
    '0x1'
    >>> hex(a<<1)
    '0x2'
    >>> hex(a<<2)
    '0x4'
    >>> hex(a<<5)
    '0x20'
    >>> b = 255
    >>> hex(b)
    '0xff'
    >>> hex(b>>1)
    '0x7f'
    >>> hex(b>>2)
    >>> '0x3f'
    >>>hex(b>>5)
    '0x7'
    >>> c = -255
    >>> hex(c)
    '-0xff'
    >>> hex(c>>1)
    '-0x80'
    >>> hex(c>>2)
    '-0x40'
    >>> hex(c>>5)
    '-0x8'
    ```
    

### 1.5.2 비트 논리 연산자

- 비트 논리 연산자
    1. `&` : 논리곱 연산자
        - 두 피연산자 비트에 대해 논리곱을 수행
    2. `|` : 논리합 연산자
        - 두 피연산자의 비트에 대해 논리합을 수행
    3. `^` : 배타적 논리합 연산자
        - 두 피연산자의 비트에 대해 배타적 논리합을 수행
    4. `~` : 보수 연산자
        - 피연산자의 비트에 대해 0은 1로, 1은 0으로 반전
- 예시
    1. `&`
        
        ```python
        >>> 9 & 10     #9(1001)와 10(1010)의 논리곱은
        8              #1000인 8
        ```
        
    2. `|`
        
        ```python
        >>> 9 | 10     #9(1001)와 10(1010)의 논리합은
        11             #1011인 11
        ```
        
    3. `^`
        
        ```python
        >>> 9 ^ 10     #9(1001)와 10(1010)의 배타적 논리합은
        3              #0011인 3
        ```
        
    4. `~`
        
        ```python
        >>> a = 255
        >>> -a
        -256
        ```
        

---