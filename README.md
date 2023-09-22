# Learn-Python

# 1.Tổng quan
Comment đơn
```
# Đây là một comment
```
Comment nhiều dòng: sử dụng dấu """ hoặc '''
```
"""
   Đây là một comment
   nhiều dòng
"""
```

## 1.1.Print giá trị
```
print ('Hello world')
```

## 1.2. Variables (Biến)
 - Tên biến trong python phân biệt hoa thường
 - Chỉ chứa các ký tự A-z, 0 - 9, và _
 - Bắt đầu chữ hoặc _, không bắt đầu bằng số
 - Tên biến phân biệt hoa thường
```
a = 5
A = 10
print(a,A)
```
- Gán giá trị cho biến. Biến python không quy định khai báo kiểu dữ liệu khi khai báo biến
```
a = 7
print(a)
a = 'hello'
print(a)
a = [1,3,4]
print(a)
a = [1, 'hello', 1.3]
print (a)
```
- Gán 1 giá trị cho nhiều biến
```
x = y = z = "One"
print('Gán một giá trị cho nhiều biến:', 'x:', x, 'y:', y, 'z:', z)
```
- Gán nhiều giá trị cho nhiều biến
```
x = y = z = "One", "Two", "Three"
print('Gán nhiều giá trị cho nhiều biến:', 'x:', x, 'y:', y, 'z:', z)
```
- Gán 1 mảng cho nhiều biến
```
number = ["One", "Two", "Three"]
x = y = z = number
print('Gán 1 mảng cho nhiều biến:', 'x:', x, 'y:', y, 'z:', z)
```
## 1.3. Data Types (Kiểu dữ liệu)
- Text:	`str`
- Numeric:	`int, float, complex`
- Sequence:	`list, tuple, range`
- Mapping:	`dict`
- Set:	`set, frozenset`
- Boolean:	`bool`
- Binary:	`bytes, bytearray, memoryview`
```
x = "Hello world" #str
print(x, type(x))

x = 20 #int
print(x, type(x))

x = 20.5 #float
print(x, type(x))

x = 20j #complex
print(x, type(x))

x = [1,2,3] #list
print(x, type(x))

x = ("One", "Two", "Three") #tuple
print(x, type(x))

x = range(6) #range
print(x, type(x))

x = {"Name": "Duy", "Age":"32"} #dict
print(x, type(x))

x = {"One", "Two", "Three"} #set
print(x, type(x))

x = frozenset({"One", "Two", "Three"}) #frozenset
print(x, type(x))

x = True #boolean
print(x, type(x))


#x = b"Hello"
#print(x, type(x))

#x = bytearray(5)
#print(x, type(x))

#x = memoryview(bytes(5))
#print(x, type(x))
```

## 1.4. Cast (Ép kiểu)

- Chuyển số --> chuỗi
```
i = 2
print(i)
str(i)

x = 1    # int
y = 2.8  # float
z = 1j   # complex
```
```
- convert from int to float:
a = float(x)
- convert from float to int:
b = int(y)
- convert from int to complex:
c = complex(x)

print(a)
print(b)
print(c)

print(type(a))
print(type(b))
print(type(c))
```
## 2.Operators (Toán tử)

### 2.1. Arithmetic Operators (Toán tử số học)
- Phép cộng (+)
- Phép trừ (-)
- Phép nhân (*)
- Phép chia (/)
- Phép chia lấy dư (modulus) (%)
- Luỹ thừa (**)
- Chia lấy nguyên (//)

#### toán tử số học:
```
n = 7
print ("n: ", n)
print ("n + 7: ", n + 7)
print ("n - 20:",n - 20)
print ("n * 3:",n * 3)
print ("n / 2:",n / 2)
print ("n % 2:",n % 2)
print ("n //2:", n//2)
print ("n ** 2:", n**2 )
```
### 2.2. Assignment Operators (Toán tử gán)
- Gán (=)
- (+=), (-=), (\*=), (/=), (%=), (//=), (\**=)
- (&=), (|=), (^=), (>>=), (<<=)
```
n = 3
print (n)

n += 2 # n = n + 2 = 3 + 2 = 5
print(n)

n -= 2 # n = n - 2 = 5 - 2 = 3
print(n)

n *= 2 # n = n * 2 = 3 * 2 = 6
print(n)

n = 7
n /= 2 # n = n / 2 = 7 / 2 = 3.5
print(n)

n = 7
n %= 2 # n = n % 2 = 7 % 2 = 1
print(n)

n = 7
n //= 2 # n = n // 2 = 7 // 2 = 3
print(n)

n **= 2 # n = n ** 2 = 3 ** 2 = 9
print(n)
```
### 2.3. Comparison Operators (Toán tử so sánh)

Dùng để so sánh 2 giá trị
- Equal (So sánh bằng) (==)
- Not Equal (So sánh khác) (!=)
- (>), (<), (>=), (<=)
```
x = 5
y = 7
print (x == y, x != y, x > y, x < y, x >=5, y <= 7)
```
### 2.4. Logical Operators (Toán tử logic)
Dùng để kết nối 2 mệnh đề điều kiện
- And
- Or
- Not
```
x = 5
y = 7
print (x > 3 and x < 7) # (5 > 3 and 5 < 7) --> (true and true) --> true
print (y > 10 or y > x) # (7 > 10 or 7 > 5) --> (false or true) --> true
print ( not(y > 7)) # not( 7 > 7) --> not (false) --> true
```
### 2.5. Identity Operators
Dùng để so sánh 2 đối tượng (object), có thể giá trị bằng nhau nhưng không cùng chung bộ nhớ.
- is
- is not
```
#number
x = 5
y = 5
z = int(5.0)
print (x is y, x is z)

#string
x = "ABC"
y = "ABC"
z = str("ABC")
print (x is y, x is z)

#object
x = ["One", "Two"]
y = ["One", "Two"]
z = x
print (x is y, x == y, z is x)
print (id(x), id(y), id(z)) #xuất danh sách địa chỉ vùng nhớ lưu trữ giá trị của biến,
#x và y cùng giá trị nhưng khác địa chỉ vùng nhớ
#x và z cùng địa chỉ vùng nhớ
```
### 2.6. Membership Operators
Dùng trong trường hợp kiểm tra 1 chuỗi (sequence) có tồn tại trong 1 đối tượng (Object) hay không
 - in
 - not in
```
s = "Hello world"
print ("Hello" in s)

arr = [1,2,3,4,5]
print (1 in arr)

arr = ["One", "Two", "Three"]
print ("one" in arr, "One" in arr)
```
### 2.7. Bitwise Operators (Toán tử trên bit)
 - AND (&): bằng 1 khi cả 2 bit đều bằng 1
 - OR (|): bằng 1 khi 1 trong 2 bit, hoặc cả 2 bit = 1
 - NOT (~)
 - XOR (^): bằng 1 khi chỉ 1 trong 2 bit = 1
 - Shift left (<<): dịch n bit 0 sang trái
 - Shift right (>>): dịch n bit 0 sang phải
```
n = 5 #binary: 0101
print (n & 1) # 0101 & 0001 = 0001 (bin) = 1 (dec)
print (n | 1) # 0101 | 0001 = 0101 (bin) = 5 (dec)
print (n ^ 1) # 0101 ^ 0001 = 0100 (bin) = 4 (dec)
print (n >> 1) # 0101 >> 1 = 0010 (bin) = 2 (dec)
print (n << 1) # 0101 << 1 = 1010 (bin) = 10 (dec)
```
## 3.Collections (Arrays)
- List: là một tập hợp được sắp xếp và có thể thay đổi. Cho phép các thành viên trùng lặp.
- Tuple: là một tập hợp có thứ tự và không thể thay đổi (immutable). Cho phép các thành viên trùng lặp.
- Set: là một tập hợp không có thứ tự và không được lập chỉ mục. Không có thành viên trùng lặp.
- Dictionary: là một tập hợp không có thứ tự và có thể thay đổi. Không có thành viên trùng lặp.

### List
### 3.2. Tuple
### 3.3. Set
Set is an unordered collection of unique items. Set is defined by values separated by comma inside braces { }. Items in a set are not ordered.

Ref: https://www.programiz.com/python-programming/variables-datatypes
```
a = {5,2,3,1,4}

# printing set variable
print("a = ", a)

# data type of variable a
print(type(a))

# set chỉ chứa giá trị duy nhất (unique values), chúng sẽ loại trừ ra các giá trị trùng lập
a = {1,2,2,3,3,3}
print(a)

# set là một tập hợp không có thứ tự nên ko sử dụng index [] cho set
a = {1,2,3}
print(a[1])

# set operator: có thể dùng &, |, ^ và - để thay thế cho các phép union (hợp), intersection (giao), difference (hiệu/ bù)
# và symmetric difference (hiệu đối xứng)
set1 = { 1,2,3 }
set2 = { 'a', 'b', 'c' }

print("Set 1:", set1)
print("Set 2:", set2)
print("intersection:", set1 & set2)
print("union:", set1 | set2)
print("difference:", set1 - set2)
print("symmetric difference:", set1 ^ set2)
```
## 4.If ... Else
Cú pháp
Block code trong python dựa vào thụt đầu dòng (indentation) thay cho {} như các ngôn ngữ khác

```
if condition:
  Block Code
elif condition:
  block code
else:
  block code
```
**Python ko có cú pháp switch case**
```
#Ví dụ If... Elif ... Else
diem = 7
xepLoai = ""
if diem >= 9:
  xepLoai = "Giỏi"
elif diem >= 7:
  xepLoai = "Khá"
elif diem >= 5:
  xepLoai = "Trung bình"
else:
  xepLoai = "Yếu"

print(xepLoai)

#Short Hand If
a = 5
b = 7
#chỉ có if
if a > b: print ("A>B")

#if, else
print ("A > B") if a > b else print ("B >= A")
```
## 5.Loop
- while
- for

### 5.1. While
Cú pháp:
```
while condition:
  block code
```
- while
```
i = 1
while i < 10:
  print(i)
  i += 1
```
- continue: dùng trong trường hợp skip 1 bước lập chuyển qua bước tiếp theo
```
i = 1
while i < 10:
  if i % 2 == 0:
    i += 1
    continue
  print(i)
  i += 1
```
- break: dùng trong trường hợp thoát khỏi vòng lập
```
i = 1
while i < 10:
  if i == 7:
    break
  print(i)
  i += 1
```
### 5.2. For
Khác với các ngôn ngữ khác, for trong python sẽ duyệt các phần tử (tương tự for each)

Cú pháp
```
for x in sequence
  block code
```
**Ngoài ra, for trong python còn có các từ khoá:**
- Else
- pass
```
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)

# Duyệt i từ range(6): [0 - 6)
for i in range(6):
  print(i)

#range (4,6): [4 - 6)
for i in range (4,6):
  print(i)

#range (2,10,3): [2,10), khoảng cách 3 giữa 2 items
for i in range (2, 10, 3):
  print(i)

#else được gọi sau khi vòng for thực hiện xong, lưu ý: trường hợp for có break thì else sẽ không được gọi
# khi break
for x in range(3):
  print(x)
else:
  print("Finally finished!")

#else không được gọi khi break
for x in range(6):
  if x == 3: break
  print(x)
else:
  print("Finally finished!")

# block code xử lý trong for không được để trống, tuy nhiên vì 1 số lý do nào đó
# không có code xử lý trong for --> dùng pass để không bị lỗi.
for x in [0, 1, 2]:
  pass

# cách viết rút gọn của for lồng
A = 'W'
B = '12345678'
print({b for b in B})
```
## 6.Function (Hàm)
Khai báo hàm theo cú pháp:
```
> def functionname(param, param2,..):
>> statements(s)

Hàm nếu không trả dữ liệu thì mặc định sẽ trả về giá trị **None**

Ref: Python cơ bản - Võ Duy Tuấn


def sum(a,b):
 return a+b

def func(a,b):
  a+b

print(sum(4,3))
print(func(3,4))

#Tham số đầu vào có giá trị mặc định nếu như không truyền từ ngoài vào
def plus(a, b = 10):
  return a + b

#Không truyền giá trị b, b sẽ có giá trị mặc định là 10
print(plus(5))

#truyền giá trị b, b sẽ có giá trị được truyền là 5
print(plus(5, 5))

def printNum(a,b):
  print("a: ", a)
  print("b: ", b)


#có thể thay đổi thứ tự tham số bằng cách đặt tên tham số truyền
printNum (1,2)
printNum (b = 5, a = 2)

import itertools
dir(itertools)
```
