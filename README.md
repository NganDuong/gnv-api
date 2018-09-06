# SHOP OWNER APIs.

1. Đăng ký.
	1. Kiểm tra.
		- API: /users/register/check
		- [Detail](/user/register_check.md).
	1. Đăng ký.
		- Mô tả:
			- Nội dung hiển thị:
				- Tên đăng nhập: `username`
				- Số điện thoại: `phone`
				- Email: `email`
				- Mật khẩu: `password`
		- API: /users/register
		- [Detail](/user/register.md).		
2. Đăng ký push notification token.
	- API: /users/notifications/register
	- [Detail](/user/register_push_token.md).
	- Example notify: [Detail](/order/notification.md).
3. Đăng nhập.
	- API: /users/login
	- [Detail](/user/login.md).
4. Cài đặt chung.
	1. Thông tin tài khoản.
		1. Xem.
			- Mô tả:
				- Nội dung hiển thị:
					- Họ tên: `username`
					- Số điện thoại: `phone`
					- Email: `email`
			- API: /users/{id}
			- [Detail](/user/profile_info_get.md).
		2. Sửa.
			- Mô tả:
				- Nội dung hiển thị:
					- Họ tên: `username`
					- Số điện thoại: `phone`
					- Email: `email`
			- API: /users/{id}
			- [Detail](/user/profile_info_update.md).
	2. Tài khoản ngân hàng.
		1. Xem.
			1. Xem tất cả.
				- Mô tả:
					- Nội dung hiển thị:
						- Chủ tài khoản: `account_holder`
						- Số tài khoản: `bank_account_number`
						- Tên ngân hàng: `bank_name`
						- Chi nhánh: `branch_name`
						- Tài khoản chính: `default_account`
				- API: /users/profile/banks
				- [Detail](/user/profile_bank_get.md).
			2. Xem chi tiết.
				- Mô tả:
					- Nội dung hiển thị:
						- Chủ tài khoản: `account_holder`
						- Số tài khoản: `bank_account_number`
						- Tên ngân hàng: `bank_name`
						- Chi nhánh: `branch_name`
						- Tài khoản chính: `default_account`
				- API: /users/profile/banks/{id}
				- [Detail](/user/profile_bank_get.md).
			2. Xem ngân hàng được hỗ trợ.
				- Mô tả:
					- Nội dung hiển thị:
						- Tên ngân hàng: `name`
				- API: /configs/banks/{id}
				- [Detail](/config/bank/get.md).
		2. Thêm.
			- Mô tả:
				- Nội dung hiển thị:
					- Chủ tài khoản: `account_holder`
					- Số tài khoản: `bank_account_number`
					- Ngân hàng: 
						- Tên ngân hàng: `bank_name`
						- Ngân hàng (chọn từ danh sách có sẵn): `support_bank_id`
					- Chi nhánh: `branch_name`
					- Tài khoản chính: `default_account`
			- API: /users/profile/banks
			- [Detail](/user/profile_bank_create.md).
		3. Sửa.
			- Mô tả:
				- Nội dung hiển thị:
					- Chủ tài khoản: `account_holder`
					- Số tài khoản: `bank_account_number`
					- Ngân hàng: 
						- Tên ngân hàng: `bank_name`
						- Ngân hàng (chọn từ danh sách có sẵn): `support_bank_id`
					- Chi nhánh: `branch_name`
					- Tài khoản chính: `default_account`
			- API: /users/profile/banks/{id}
			- [Detail](/user/profile_bank_update.md).
		4. Xóa.
			- API: /users/profile/banks/{id}
			- [Detail](/user/profile_bank_delete.md).
	3. Chi nhánh cửa hàng.
		1. Xem.
			1. Xem tất cả.
				- Mô tả:
					- Nội dung hiển thị:
						- Tên cửa hàng: `name`
						- Số điện thoại: `phone`
						- Địa chỉ:
							- Đường: `address`
							- Quận: `location` -> `district` -> `name`
							- Tỉnh/Thành phố: `location` -> `province` -> `name`
						- Cửa hàng chính: `default_store`
				- API: /users/profile/stores
				- [Detail](/user/profile_store_get.md).
			2. Xem chi tiết.
				- Mô tả:
					- Nội dung hiển thị:
						- Tên cửa hàng: `name`
						- Số điện thoại: `phone`
						- Địa chỉ:
							- Đường: `address`
							- Quận: `location` -> `district` -> `name`
							- Tỉnh/Thành phố: `location` -> `province` -> `name`
						- Cửa hàng chính: `default_store`
				- API: /users/profile/stores/{id}
				- [Detail](/user/profile_store_get.md).
		2. Thêm.
			- Mô tả:
				- Nội dung hiển thị:
					- Tên người liên hệ: `name`
					- Số điện thoại: `phone`
					- Địa chỉ:
						- Đường: `address`
						- Khu vực: `location_id`
						- Kinh độ: `longitude`
						- Vĩ độ: `latitude`
					- Cửa hàng chính: `default_store`
			- API: /users/profile/stores
			- [Detail](/user/profile_store_create.md).
		2. Lấy danh sách địa chỉ lấy hàng.
			- API: /configs/locations?support_type_id[in]=1,3
			- [Detail](/config/location/get.md).
		3. Sửa.
			- Mô tả:
				- Nội dung hiển thị:
					- Tên người liên hệ: `name`
					- Số điện thoại: `phone`
					- Địa chỉ:
						- Đường: `address`
						- Khu vực: `location_id`
						- Kinh độ: `longitude`
						- Vĩ độ: `latitude`
					- Cửa hàng chính: `default_store`
			- API: /users/profile/stores/{id}
			- [Detail](/user/profile_store_update.md).
		4. Xóa.
			- API: /users/profile/stores/{id}
			- [Detail](/user/profile_store_delete.md).
	4. Lịch đối soát.
		1. Lấy thông tin để tạo (lấy lựa chọn).
			- API: /configs/schedules/crossCheck
			- [Detail](/config/schedule/cross_check_get_schedule.md).
		2. Xem.
			- API: /users/profile/schedules/crossCheck/{id}
			- [Detail](/user/profile_cross_check_schedule_get.md).
		3. Tạo/Cập nhật.
			- API: /users/profile/schedules/crossCheck/{id}
			- [Detail](/user/profile_cross_check_schedule_update.md).
5. Quản lý đơn hàng.
	1. Xem các đơn hàng.
		- API: /orders
		- [Detail](/order/get.md).
	2. Xem chi tiết đơn hàng.
		1. Xem thông tin đơn hàng.
			- API: /orders/{id}
			- [Detail](/order/get.md).
		2. Xem lịch sử đơn hàng.
			- API: /orders/notes?order_id={id}
			- [Detail](/order/get_notes.md).
	3. Gửi yêu cầu cho 1 đơn hàng.
		1. Chọn loại yêu cầu.
			- API: /configs/orders/requests/
			- [Detail](/config/order/request_type_get.md).
		2. Gửi yêu cầu.
			- API: /orders/requests
			- [Detail](/order/request_create.md).
		3. Xem yêu cầu.
			- Mô tả:
			- Lấy danh sách yêu cầu đã gửi. Kết quả trả về được gom nhóm theo mã đơn hàng, mỗi nhóm sẽ gồm danh sách các yêu cầu đối với đơn hàng này.
			- Params:
				- Mã đơn hàng: `order_code`
				- Tiêu đề yêu cầu: `order_request_type` -> `name`
				- Nội dung yêu cầu: `description`
				- Ngày tạo yêu cầu: `created`
				- Trạng thái: `status`
				- Người xử lý: `solver` -> `username`
				- Thời gian đã xử lý: `solved`
			- API lấy tất cả yêu cầu: /orders/requests
			- API lấy yêu cầu của 1 đơn hàng: /orders/requests?order_id={id}
			- API lấy 1 yêu cầu của 1 đơn hàng: /orders/requests?order_id={order id}&id={request id}
			- [Detail](/order/request_get_new.md).
	4. Lấy danh sách trạng thái đơn hàng.
		- Mô tả: 
			- Hiển thị danh sách trạng thái đơn hàng.
			- Nội dung hiển thị:
				- Trạng thái: `name`.
		- API: /configs/orders/status/{id}
		- [Detail](/order/status_get.md).
	4. Tìm kiếm đơn hàng.
		- API: /orders
		- [Detail](/order/search.md).
		- Tìm kiếm theo:
			1. Mã đơn hàng:
				> + Field to search: ```order_code```
				> + Value's type: string
				> + Example URL: /orders?order_code=O1527428478
			2. Số điện thoại người gửi / nhận:
				> + Field to search: ```sender_phone``` / ```receiver_phone```
				> + Value's type: string / string
				> + Example URL: /orders?sender_phone=0123456789
			3. Tên người gửi / nhận:
				> + Field to search: ```sender_name``` / ```receiver_name```
				> + Value's type: string / string
				> + Example URL: /orders?sender_name=ngan
			4. Địa chỉ người gửi / nhận:
				> + Field to search: ```sender_address``` / ```receiver_address``` / ```sender_location_id``` / ```receiver_location_id```
				> + Value's type: string / string / integer / integer
				> + Example URL: /orders?sender_address[like]=104
			5. Trạng thái đơn hàng:
				> + Field to search: ```order_status_id```
				> + Value's type: integer : range = [1-16]
				> + Example URL: /orders?order_status_id=1
			6. Ngày tạo đơn hàng:
				- Từ:
					> + Field to search: ```created```
					> + Value's type: string / datetime
					> + Example URL: /orders?created[ge]=27/05/2018
				- Đến:
					> + Field to search: ```created```
					> + Value's type: string / datetime
					> + Example URL: /orders?created[le]=27/05/2018T23:59:59
			7. Người thanh toán phí:
				> + Field to search: ```fee_payer```
				> + Value's type: integer : range = [0 (shop owner / sender), 1 (receiver)] 
				> + Example URL: /orders?fee_payer=0
	5. Tạo đơn hàng.
		1. Tạo.
			- API: /orders
			- [Detail](/order/create.md).
			- Fields:
				1. Thông tin giao nhận.
					1. Thông tin người gửi.
						1. Chọn từ danh sách chi nhánh cửa hàng.
						2. Nhập mới.
							- Tên: `sender_name`
							- Số điện thoại: `sender_phone`
							- Địa chỉ: `sender_address`
							- Khu Vực: `sender_location_id`
					2. Thông tin người nhận.
						- Tên: `receiver_name`
						- Số điện thoại: `receiver_phone`
						- Địa chỉ: `receiver_address`
						- Khu Vực: `receiver_location_id`
					3. Ngày giờ muốn lấy hàng.
						- Ngày Lấy Hàng: `expected_pickup_date`
						- Ca Lấy Hàng: `expected_pickup_session`
					4. Ngày giờ muốn nhận hàng.
						- Ngày Giao Hàng: `expected_delivery_date`
						- Ca Giao Hàng: `expected_delivery_session`
				2. Chi tiết đơn hàng (gói hàng).
					- Mã đơn của shop: `customer_order_code`
					- Loại hàng: `type`
					- Kích thước:
						- Dài: `size_lenght`
						- Rộng: `size_width`
						- Cao: `size_height`
					- Cân nặng: `weight`
					- Gói cước (dịch vụ): `service_id`
					- Ghi chú đơn hàng: `handle_instruction`
				3. Thông tin thanh toán.
					- Khai giá hàng hóa: `value`
					- Thu hộ: `cod`
					- Phí vận chuyển (chọn người trả): `fee_payer`
					- Mã Khuyến Mãi: `coupon_code`
		2. Lấy danh sách địa chỉ lấy hàng.
			- API: /configs/locations?support_type_id[in]=1,3
			- [Detail](/config/location/get.md).
		2. Lấy danh sách địa chỉ giao hàng.
			- API: /configs/locations?support_type_id[in]=2,3
			- [Detail](/config/location/get.md).
		2. Lấy thông tin giới hạn kích thước.
			1. Chiều dài.
				- API: /configs/variables?name=PARCEL_LENGTH_LIMIT
				- [Detail](/config/variable/get.md).
			1. Chiều rộng.
				- API: /configs/variables?name=PARCEL_WIDTH_LIMIT
				- [Detail](/config/variable/get.md).
			1. Chiều cao.
				- API: /configs/variables?name=PARCEL_HEIGHT_LIMIT
				- [Detail](/config/variable/get.md).
		2. Lấy thông tin giới hạn cân nặng.
			- API: /configs/variables?name=PARCEL_WEIGHT_LIMIT
			- [Detail](/config/variable/get.md).
		2. Kiểm tra coupon.
			- API: /configs/orders/coupons/check?code={coupon code}&user_id={current user id}
			- [Detail](/config/coupon/check.md).
		2. Lấy danh sách gói dịch vụ.
			- API: /configs/orders/deliveries/services?sender_location_id={id}&receiver_location_id={id}
			- Example: /configs/orders/deliveries/services?sender_location_id=1&receiver_location_id=1
			- [Detail](/config/service/get_specific.md).
		4. Tính phí, tiền.
			- API: /orders/fees/
			- Example: /orders/fees?&sender_location_id=1&receiver_location_id=1&weight=1&length=1&width=1&height=1&service_id=1&cod=0
			- [Detail](/order/calculate_fee.md).
6. Quản lý đối soát.
	1. Đối soát sắp tới.
		- Xem thông tin.
			- API: /orders/moneys
			- [Detail](/order/money.md).
	2. Lịch sử đối soát.
		- Xem thông tin.
			- API: /orders/transferedMoneys
			- [Detail](/order/transfered_money.md).
7. Thông báo.
	- Xem danh sách thông báo.
		- Mô tả: 
			- Hiển thị danh sách thông báo.
			- Nội dung hiển thị:
				- Mã đơn hàng: `order_notification` -> `order_code`.
				- Thời gian: `created`.
				- Tiêu đề: `order_notification` -> `header`.
				- Nội dung: `order_notification` -> `content`.
				- Trạng thái: `status`.
		- API: /users/notifications
		- [Detail](/user/notification_get.md).
	- Đánh dấu đã xem thông báo.
		- Mô tả: 
			- Đánh dấu đã xem 01 thông báo.
		- API: /users/notifications/read/{id}
		- [Detail](/user/notification_read.md).