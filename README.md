# Phân Tích Hiệu Suất Bán Hàng Online của Contoso (2007 - 2009)

## Mục lục

- [Tổng quan dự án](#tổng-quan-dự-án)
- [Mục tiêu](#mục-tiêu)
- [Dữ liệu](#dữ-liệu)
- [Phân tích dữ liệu](#phân-tích-dữ-liệu)
- [Insights](#insights)
- [Đề xuất](#đề-xuất)
- [Tài liệu tham khảo](#tài-liệu-tham-khảo)

### Tổng quan dự án

Contoso là một tập đoàn bán lẻ đa quốc gia có trụ sở tại Paris (Pháp) với danh mục sản phẩm hơn 100 nghìn loại khác nhau. Việc phân tích dữ liệu sẽ tập trung vào các chỉ số về bán hàng online như lợi nhuận, doanh thu, tăng trưởng doanh thu hàng năm và chỉ số liên quan đến khách hàng như CLV. Từ đó, dự án đề xuất giải pháp cho sales manager để cải thiện chiến lược bán hàng và tối ưu hóa doanh thu cho Contoso.

### Mục tiêu

- Xác định những mặt hàng bán chạy và cơ hội để triển khai hoạt động upselling và cross-selling
- Phân tích doanh thu, doanh số bán hàng online theo thời gian (2007-2009)

### Dữ liệu

Dự án sử dụng database được cung cấp bởi Microsoft, tham khảo tại [đây](https://www.microsoft.com/en-us/download/details.aspx?id=18279). Vì bộ dữ liệu này bao gồm thông tin từ nhiều phòng ban trong doanh nghiệp như C-level, Sales/Marketing, IT, Finance... nên dự án sẽ chỉ tập trung vào các bảng sau:

- **FactOnlineSales**: lưu dữ liệu bán hàng về doanh thu, doanh số, chi phí, lượng hàng trả về và giá trị mặt hàng giảm giá cho mỗi giao dịch online
- **DimDate**: mô tả thời gian diễn ra giao dịch theo năm, quý, tháng, tuần và ngày
- **DimProduct**: thông tin về sản phẩm như nhà sản xuất, thương hiệu, đặc điểm bên ngoài và chi phí, giá bán cho mỗi sản phẩm
- **DimProductCategory**: mô tả tên và key cho từng danh mục sản phẩm bao gồm: Audio, Computers, Cellphones...)
- **DimProductSubCategory**: Phân loại sản phẩm con (được chia nhỏ hơn so với danh mục sản phẩm) bao gồm: Televisions, VCD&DVD, Accessories...
- **DimCustomer**: thông tin nhân khẩu học của khách hàng (giới tính, thu nhập cả năm, học vấn, nghề nghiệp...) 
- **DimPromotion**: chi tiết về từng loại giảm giá và mức giảm giá
- **DimGeography**: thông tin địa lý theo từng quốc gia, từng vùng gắn với nơi khách hàng sinh sống

Database diagram được mô tả như hình dưới đây:
![](https://github.com/Toridotoji/Project-1/blob/main/database%20diagram.png?raw=true)

### Phân tích dữ liệu
Xem thêm tại file [Phương pháp phân tích dữ liệu](https://github.com/Toridotoji/Project-1/blob/bb46d5e1fc9250ce68c0dcb509ce43bd0805d4a6/ph%C6%B0%C6%A1ng%20ph%C3%A1p%20ph%C3%A2n%20t%C3%ADch%20d%E1%BB%AF%20li%E1%BB%87u.md)

### Insights

## Tình hình kinh doanh
Năm 2009, doanh thu và lợi nhuận ròng Contoso đạt được lần lượt là 857,73 triệu đô và 437,91 triệu đô.

![{8098E5FE-E2F8-472D-8700-CD092D98418B}](https://github.com/user-attachments/assets/1dc7d28d-0c14-4766-9afd-63d21da5dfdb)

![{9D3C5F3B-6F94-4A1D-BD14-114E0F87363A}](https://github.com/user-attachments/assets/2a857f71-399e-4c0d-be4e-4495ffed1351)

![{15166663-527F-4593-9D7F-1E6E8F82FCC0}](https://github.com/user-attachments/assets/f26e5d61-f256-4e22-bf93-a9aa9de149af)

## Sản phẩm

Sản phẩm bán chạy nhất năm 2009 là Tủ lạnh LitWare 24.7CuFt X980 (màu nâu) với doanh thu là 3,12 triệu đô, trước đó vào năm 2008 sản phẩm này cũng đứng đầu sản phẩm bán chạy nhất (màu trắng) với doanh thu là 4 triệu đô.

![{E6C6E53A-FC6F-4713-9816-0B26AAB19858}](https://github.com/user-attachments/assets/677fe477-1d6a-48ba-87ae-5894e3452cb1)

**Phân tích theo nguyên tắc 80/20**
Danh mục con này chủ yếu đến từ danh mục sản phẩm "Home Appliances"

![{A1074CB3-0468-4BFF-8B89-485D6EA2AF3D}](https://github.com/user-attachments/assets/83ba22d2-8ee8-483d-9d62-0ff3f42c7122)


### Đề xuất

### Tài liệu tham khảo
