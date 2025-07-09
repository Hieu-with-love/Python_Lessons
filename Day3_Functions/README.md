# 📘 Day 3: Functions (Hàm) - Python Tutorial

## 📋 Table of Contents
- [Định nghĩa Hàm](#-định-nghĩa-hàm)
- [Khai báo và gọi hàm](#-khai-báo-và-gọi-hàm)
- [Quy tắc đặt tên](#-quy-tắc-đặt-tên)
- [Thực hành với hàm](#-thực-hành-với-hàm)
- [Function có tham số](#-function-có-tham-số)
- [Bài tập thực hành](#-bài-tập-thực-hành)

---

## 🎯 Định nghĩa Hàm (Function)

Một **hàm** là một khối mã (code block) hoặc tập hợp các câu lệnh lập trình có thể **tái sử dụng**, được thiết kế để thực hiện một nhiệm vụ cụ thể. 

- Python cung cấp từ khóa `def` để định nghĩa hoặc khai báo một hàm
- Khối mã bên trong hàm chỉ được thực thi khi hàm được gọi (invoke)

## 🔧 Khai báo và gọi hàm

**Khai báo hàm (declaring a function)**: Hành động tạo ra một hàm  
**Gọi hàm (calling/invoking a function)**: Hành động sử dụng hàm đã được khai báo

### ✨ Cú pháp cơ bản:
```python
# Định nghĩa hàm
def function_name():
    print("This is a function.")

# Gọi hàm
function_name()
```

## 📝 Quy tắc đặt tên

> **💡 Lưu ý**: Đặt tên hàm cho có ý nghĩa và dễ hiểu

### 🐍 Các quy ước đặt tên trong Python:

| Quy ước | Sử dụng cho | Ví dụ |
|---------|-------------|--------|
| **snake_case** | Tên hàm, biến | `calculate_area`, `user_name` |
| **PascalCase** | Tên lớp (Class) | `StudentInfo`, `LoginForm` |
| **UPPER_CASE** | Hằng số (constant) | `MAX_SIZE`, `PI` |

## 🚀 Thực hành với hàm

### 1️⃣ Function không tham số, không có giá trị trả về

```python
def generate_full_name():
    first_name = "Tran"
    last_name = "Trung Hieu"
    space = ' '
    full_name = first_name + space + last_name
    print(full_name)

# Gọi hàm
generate_full_name()  # Output: Tran Trung Hieu
```

### 2️⃣ Function không tham số, có giá trị trả về

```python
def generate_full_name_with_return():
    first_name = "Tran"
    last_name = "Trung Hieu"
    space = ' '
    full_name = first_name + space + last_name
    return full_name

# Chúng ta cần tạo một biến để lưu giá trị trả về từ hàm
full_name = generate_full_name_with_return()
print(full_name)  # Output: Tran Trung Hieu
```

---
## 📥 Function có tham số

Trong một hàm, chúng ta có thể truyền nhiều kiểu dữ liệu khác nhau làm tham số:
- **Số** (int, float)
- **Chuỗi** (string) 
- **Boolean** (True/False)
- **Danh sách** (list)
- **Bộ** (tuple)
- **Từ điển** (dictionary) 
- **Tập hợp** (set)

### 1️⃣ Tham số đơn (Single Parameter)

Khi khai báo hàm có yêu cầu tham số, thì khi gọi hàm chúng ta cần truyền vào một đối số tương ứng.

#### ✨ Cú pháp:
```python
# Khai báo hàm
def function_name(parameter):
    # code implementation
    return result

# Gọi hàm
print(function_name(argument))
```

#### 📋 Ví dụ:
```python
def greet_person(name):
    return f"Hello, {name}!"

# Gọi hàm
print(greet_person("Alice"))  # Output: Hello, Alice!
```

### 2️⃣ Số lượng đối số tùy ý (Arbitrary Number of Arguments)

Nếu chúng ta không biết trước số lượng đối số sẽ truyền vào hàm, chúng ta có thể tạo một hàm nhận số lượng đối số tùy ý bằng cách thêm dấu `*` trước tên tham số.

#### ✨ Cú pháp:
```python
def function_name(*args):
    # args sẽ là một tuple chứa tất cả các đối số được truyền vào
    pass
```

#### 📋 Ví dụ:
```python
def show_students(*names):
    for name in names:
        print("Student:", name)

# Gọi hàm
show_students("Alice", "Bob", "Charlie")
# Output:
# Student: Alice
# Student: Bob  
# Student: Charlie
```

> **💡 Giải thích**: Khi gọi `show_students("Alice", "Bob", "Charlie")`, Python sẽ gộp tất cả các đối số vào một tuple `names`. Hàm sẽ in lần lượt tên của từng sinh viên.

---

## 🧩 Bài tập thực hành

### 🔰 Mức 1 - Cơ bản

#### 1. ➕ **Tính tổng hai số**
Khai báo một hàm `add_two_numbers`. Hàm nhận hai tham số và trả về tổng của chúng.

#### 2. 🔵 **Tính diện tích hình tròn**
Diện tích hình tròn được tính theo công thức: `area = π × r × r`  
Viết một hàm tính `area_of_circle`.

#### 3. 🔢 **Tính tổng nhiều số**
Viết một hàm có tên là `add_all_nums`, hàm nhận số lượng đối số tùy ý và tính tổng tất cả các đối số. Kiểm tra nếu tất cả phần tử trong danh sách đều là kiểu số. Nếu không, hãy đưa ra thông báo hợp lý.

#### 4. 🌡️ **Chuyển đổi nhiệt độ**
Nhiệt độ °C có thể chuyển sang °F bằng công thức: `°F = (°C × 9/5) + 32`  
Viết một hàm chuyển đổi từ °C sang °F, đặt tên hàm là `convert_celsius_to_fahrenheit`.

#### 5. 🌿 **Kiểm tra mùa**
Viết một hàm có tên `check_season`, nhận một tham số là tháng và trả về mùa: Thu, Đông, Xuân hoặc Hè.

#### 6. 📈 **Tính hệ số góc**
Viết một hàm có tên `calculate_slope` để trả về hệ số góc của một phương trình đường thẳng.

#### 7. 📐 **Giải phương trình bậc hai**
Phương trình bậc hai được tính theo công thức: `ax² + bx + c = 0`  
Viết một hàm tính nghiệm của phương trình bậc hai, đặt tên là `solve_quadratic_eqn`.

#### 8. 📋 **In danh sách**
Khai báo một hàm có tên `print_list`. Hàm nhận một danh sách làm tham số và in ra từng phần tử trong danh sách.

#### 9. 🔄 **Đảo ngược danh sách**
Khai báo một hàm có tên `reverse_list`. Hàm nhận một mảng làm tham số và trả về mảng đảo ngược (sử dụng vòng lặp).

```python
print(reverse_list([1, 2, 3, 4, 5]))
# Expected Output: [5, 4, 3, 2, 1]

print(reverse_list(["A", "B", "C"]))
# Expected Output: ["C", "B", "A"]
```

#### 10. 🔠 **Viết hoa danh sách**
Khai báo một hàm có tên `capitalize_list_items`. Hàm nhận một danh sách làm tham số và trả về danh sách các phần tử đã được viết hoa.

#### 11. ➕ **Thêm phần tử vào danh sách**
Khai báo một hàm có tên `add_item`. Hàm nhận hai tham số: một danh sách và một phần tử. Hàm trả về danh sách với phần tử đã được thêm vào cuối.

```python
food_staff = ['Potato', 'Tomato', 'Mango', 'Milk']
print(add_item(food_staff, 'Meat'))  
# Expected Output: ['Potato', 'Tomato', 'Mango', 'Milk', 'Meat']

numbers = [2, 3, 7, 9]
print(add_item(numbers, 5))  
# Expected Output: [2, 3, 7, 9, 5]
```

#### 12. ➖ **Xóa phần tử khỏi danh sách**
Khai báo một hàm có tên `remove_item`. Hàm nhận hai tham số: một danh sách và một phần tử. Hàm trả về danh sách sau khi đã loại bỏ phần tử đó.

```python
food_staff = ['Potato', 'Tomato', 'Mango', 'Milk']
print(remove_item(food_staff, 'Mango'))  
# Expected Output: ['Potato', 'Tomato', 'Milk']

numbers = [2, 3, 7, 9]
print(remove_item(numbers, 3))  
# Expected Output: [2, 7, 9]
```

#### 13. 🔢 **Tính tổng từ 1 đến n**
Khai báo một hàm có tên `sum_of_numbers`. Hàm nhận một tham số là số và tính tổng tất cả các số từ 1 đến số đó.

```python
print(sum_of_numbers(5))   # Expected Output: 15
print(sum_of_numbers(10))  # Expected Output: 55
print(sum_of_numbers(100)) # Expected Output: 5050
```

#### 14. 🔢 **Tính tổng số lẻ**
Khai báo một hàm có tên `sum_of_odds`. Hàm nhận một tham số là số và tính tổng tất cả các số lẻ trong khoảng từ 1 đến số đó.

#### 15. 🔢 **Tính tổng số chẵn**
Khai báo một hàm có tên `sum_of_even`. Hàm nhận một tham số là số và tính tổng tất cả các số chẵn trong khoảng từ 1 đến số đó.

---

### 🚀 Mức 2 - Trung bình

#### 1. 🔄 **Đếm số chẵn và lẻ**
Khai báo một hàm có tên `evens_and_odds`. Hàm nhận một số nguyên dương làm tham số và đếm số lượng số chẵn và số lẻ trong khoảng từ 0 đến số đó.

```python
print(evens_and_odds(100))
# Expected Output:
# The number of odds are 50.
# The number of evens are 51.
```

#### 2. 📊 **Tính giai thừa**
Gọi hàm `factorial`, hàm nhận một số nguyên dương và trả về giai thừa của số đó.

#### 3. 🔍 **Kiểm tra rỗng**
Gọi hàm `is_empty`, hàm nhận một tham số và kiểm tra xem nó có rỗng hay không.

#### 4. 📈 **Các hàm thống kê**
Viết các hàm khác nhau nhận danh sách làm đầu vào. Các hàm nên thực hiện:

- `calculate_mean` – Tính trung bình
- `calculate_median` – Tính trung vị
- `calculate_mode` – Tìm mode
- `calculate_range` – Tính khoảng cách (max - min)
- `calculate_variance` – Tính phương sai
- `calculate_std` – Tính độ lệch chuẩn

---

### ⭐ Mức 3 - Nâng cao

#### 1. 🔢 **Kiểm tra số nguyên tố**
Viết một hàm có tên `is_prime`, kiểm tra xem một số có phải là số nguyên tố hay không.

#### 2. 🔄 **Kiểm tra tính duy nhất**
Viết một hàm kiểm tra xem tất cả các phần tử trong danh sách có duy nhất (không trùng lặp) hay không.

#### 3. 🔍 **Kiểm tra cùng kiểu dữ liệu**
Viết một hàm kiểm tra xem tất cả các phần tử trong danh sách có cùng kiểu dữ liệu hay không.

#### 4. ✅ **Kiểm tra tên biến hợp lệ**
Viết một hàm kiểm tra xem biến được cung cấp có phải là tên biến hợp lệ trong Python hay không.

#### 5. 🗂️ **Xử lý dữ liệu quốc gia**
Truy cập thư mục dữ liệu (data folder) và mở file `countries-data.py`.

- Tạo một hàm có tên `most_spoken_languages`, trả về 10 hoặc 20 ngôn ngữ được nói nhiều nhất trên thế giới theo thứ tự giảm dần.
- Tạo một hàm có tên `most_populated_countries`, trả về 10 hoặc 20 quốc gia đông dân nhất thế giới theo thứ tự giảm dần.

---

## 🎉 Kết luận

Bạn đã hoàn thành Day 3 về Functions trong Python! 🐍

**Những kiến thức đã học:**
- ✅ Định nghĩa và cách sử dụng hàm
- ✅ Các loại tham số khác nhau
- ✅ Quy tắc đặt tên hàm
- ✅ Thực hành với nhiều bài tập từ cơ bản đến nâng cao

**Tiếp theo:** Hãy thực hành các bài tập để củng cố kiến thức và chuẩn bị cho Day 4! 💪

---

> 📚 **Ghi chú**: README này là một phần của Python Tutorial series. Để hiểu rõ hơn, hãy thực hành code trong file `functions.py`!

