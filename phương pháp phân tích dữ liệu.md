Phân tích dữ liệu được thực hiện trên Power BI.

**Rút gọn tên tháng**

- Mục đích: khi tạo visualization thì tên tháng không thể hiện đầy đủ mà được rút gọn lại (ví dụ: January -> Jan)
- Tạo cột mới trong bảng DimDate
  ```
  Shorter month =
  FORMAT(DimDate[Datekey], "MMM")
  ```
- Tạo thêm cột để sắp xếp tháng theo trình tự
  ```
  Month Number = 
  MONTH(DimDate[Datekey])
  ```
  Chọn cột Shorter month trong Table View -> *Sort by column -> Month Number*

**Phân tích 80/20 đối với danh mục con**

Kết quả visual Table như sau:

![{334881F3-34EB-4C85-BA51-F5F6DECDAF7C}](https://github.com/user-attachments/assets/4569b43d-1388-4e21-84a1-604e9cf316bf)

- Tính doanh thu đối với từng subcategory:
  ```
  Revenue = 
  SUM(FactOnlineSales[SalesAmount])
  ```

- Xếp hạng các subcategory theo doanh thu:
  ```
  Rank = 
    RANKX(
        ALLSELECTED(DimProductSubcategory[ProductSubcategoryName]),
        [Revenue])
  ```

- Sắp xếp cột Rank theo chiều tăng dần và tính doanh thu lũy tiến:
  ```
  Cumulative Sales = 
  CALCULATE(
    [Revenue],
    TOPN([Rank],
    ALL(DimProductSubcategory[ProductSubcategoryName]),
    [Revenue]))
  ```

- Tính tổng doanh thu của tất cả subcategory:
  ```
  TotalRevenue = 
  CALCULATE(
    [Revenue],
    ALL(DimProductSubcategory[ProductSubcategoryName]))
  ```

- Tính % mức độ đóng góp lũy tiến của các subcategory:
  ```
  %CumulativeSales = 
  DIVIDE(
    [Cumulative Sales],
    [TotalRevenue],
    0)
  ```


