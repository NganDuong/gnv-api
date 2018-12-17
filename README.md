# SHIPPER APIs.

1. Đăng nhập.
	- Mô tả:
		- Đăng nhập.
		- Nội dung:
			- Tên đăng nhập (varchar(50)): `username`
			- Mật khẩu (varchar(255)): `password`
	- API: /users/login
	- [Detail](user/login.md)
2. Đăng ký push notification token.
	- Mô tả:
		- Đăng ký token để nhận thông báo từ Firebase.
		- Nội dung:
			- Firebase token (varchar(255)): `device_token`
			- Loại thiết bị (int): `device_type`
	- API: /users/notifications/register
	- [Detail](/user/register_push_token.md).
3. Cập nhật vị trí.
	- Mô tả:
		- Cập nhật vị trí shipper.
		- Nội dung:
			- Longitude (decimal(11, 8)): `longitude`
			- Latitude (decimal(10, 8)): `latitude`
	- API: /users/profile/locations
	- [Detail](/shipper/profile/update_location.md).
4. Danh sách cần lấy.
	1. Danh sách cần lấy: 
		- Mô tả:
			- Lấy ra các đơn hàng được group theo địa chỉ lấy hàng trong ca hiện tại.
			- Nội dung:
				- Tên liên hệ lấy hàng (varchar(50)): `sender_name`
				- Số điện thoại liên hệ lấy hàng (varchar(50)): `sender_phone`
				- Địa chỉ lấy hàng: `sender_address`, `sender_location_id`, `sender_longitude`, `sender_latitude`, `sender_address_detail`
				- Tổng số đơn hàng ở địa chỉ này (int): `total`
				- Số đơn hàng đã lấy tại địa chỉ này (int):` total_picked_up`
				- Số đơn hàng đã lấy thất bại tại địa chỉ này (int):` total_failed`
				- Mã trạng thái nhóm (int): `group_status_id`
				- Trạng thái nhóm  (varchar(50)): `group_status`
				- Tổng quan đơn hàng: `order`
					- Mã đơn (varchar(50)): `order_code`
					- Mã shop (varchar(50)): `user_code`
					- Đã trả phí (0 - chưa | 1 - đã trả) (int): `fee_paid`
					- Mã trạng thái đơn (int): `order_status_id`
					- Giảm giá (float): `discount`
					- Hình ảnh đơn hàng (array): `pickup_photos`, `pickup_signature_photo`
						- URL: `path`
					- Tiền phải thu (float): `cash`
					- Tên trạng thái (varchar(50)): `status`
					- Tên ca lấy hàng (string): `session`
		- API: /orders/pickup/
		- [Detail](/shipper/pickup/prs.md)
	2. Thống kê:
		- Mô tả:
			- Thống kê dựa trên các đơn hàng có trong ca hiện tại.
			- Nội dung hiển thị:
				- Số đơn hàng đã lấy: picked
				- Số đơn hàng chưa lấy: picking
				- Số đơn hàng lấy thất bại: failed
				- Tiền thu shop: total_cash
		- API: /orders/pickup/statistics
		- [Detail](/shipper/pickup/statistic.md)
	3. Xem đơn hàng đã lấy:
		- Mô tả:
			- Thống kê dựa trên các đơn hàng đã lấy được group theo địa chỉ lấy hàng có trong ca hiện tại.
			- Nội dung hiển thị:
				- Tên liên hệ lấy hàng: sender_name
				- Số điện thoại liên hệ lấy hàng: sender_phone
				- Địa chỉ lấy hàng: sender_address, sender_location_id, sender_longitude, sender_latitude, sender_address_detail
				- Tổng số đơn hàng: total
		- API: /orders/pickup/statistics/picked
		- [Detail](/shipper/pickup/picked_orders.md)
	4. Xem đơn hàng chưa lấy:
		- Mô tả:
			- Thống kê dựa trên các đơn hàng chưa lấy được group theo địa chỉ lấy hàng có trong ca hiện tại.
			- Nội dung hiển thị:
				- Tên liên hệ lấy hàng: sender_name
				- Số điện thoại liên hệ lấy hàng: sender_phone
				- Địa chỉ lấy hàng: sender_address, sender_location_id, sender_longitude, sender_latitude, sender_address_detail
				- Tổng số đơn hàng: total
		- API: /orders/pickup/statistics/picking
		- [Detail](/shipper/pickup/picking_orders.md)
	5. Xem đơn hàng lấy thất bại:
		- Mô tả:
			- Thống kê dựa trên các đơn hàng lấy thất bại được group theo địa chỉ lấy hàng có trong ca hiện tại.
			- Nội dung hiển thị:
				- Tên liên hệ lấy hàng: sender_name
				- Số điện thoại liên hệ lấy hàng: sender_phone
				- Địa chỉ lấy hàng: sender_address, sender_location_id, sender_longitude, sender_latitude, sender_address_detail
				- Tổng số đơn hàng: total
		- API: /orders/pickup/statistics/failed
		- [Detail](/shipper/pickup/failed_orders.md)
	6. Xem các đơn hàng cùng địa chỉ lấy hàng:
		- Mô tả: 
			- Thống kê các đơn hàng thuộc địa chỉ lấy hàng có trong ca hiện tại.
			- Nội dung hiển thị:
				- Tên liên hệ lấy hàng: sender_name
				- Số điện thoại liên hệ lấy hàng: sender_phone
				- Địa chỉ lấy hàng: sender_address, sender_location_id, sender_longitude, sender_latitude, sender_address_detail
				- Tổng số đơn hàng: total
				- Danh sách các đơn hàng.
		- API: /orders/pickup?sender_address={address number/street}&sender_location_id={id}&sender_phone={phone number}
		- [Detail](/shipper/pickup/pickup_location_detail.md)
	7. Xem thông tin đơn hàng:
		- Mô tả:
			- Hiển thị thông tin chung của đơn hàng.
			- Nội dung hiển thị:
				- Mã đơn hàng: `order_code`
				- Tuyến đơn hàng: `route_text`
				- Thông tin người gửi:
					- Người gửi: `sender_name`
					- Số điện thoại: `sender_phone`
					- Địa chỉ lấy hàng:
						- Đường: `sender_address`
						- Kinh độ: `sender_longitude`
						- Vĩ độ: `sender_latitude`
					- Thời gian lấy: `pickup_session`
					- Ngày lấy hàng: `pickup_date`
				- Thông tin người nhận:
					- Người nhận: `receiver_name`
					- Số điện thoại: `receiver_phone`
					- Địa chỉ giao hàng:
						- Đường: `receiver_address`
						- Kinh độ: `receiver_longitude`
						- Vĩ độ: `receiver_latitude`
					- Thời gian giao: `delivery_session`
					- Ngày giao hàng: `delivery_date`
				- Thông tin đơn hàng:
					- Mã đơn hàng (của shop/khách hàng): `customer_order_code`
					- Kích thước:
						- Dài: `size_lenght`
						- Rộng: `size_width`
						- Cao: `size_height`
					- Gói cước: `service` -> `name`
					- Ghi chú đơn hàng: `handle_instruction`
					- Trạng thái: `order_status`
					- Loại hàng: `type`
					- Trọng lượng: `weight`
				- Thông tin thanh toán:
					- Khai giá hàng hóa: `value`
					- Thu hộ(COD): `cod`
					- Thanh toán phí: `fee_payer`
					- Phí giao hàng: `delivery_fee`
					- Tổng tiền thu: `cash`
				- Hình ảnh đơn hàng (array): `pickup_photos`, `delivery_signature_photo`, `delivery_photos`, `pickup_signature_photo`
						- URL: `path`
		- API: /orders/{id}
		- [Detail](/order/get.md)
	8. Xem lịch sử đơn hàng:
		- Mô tả:
			- Hiển thị thông tin lịch sử đơn hàng.
				- Ngày: `created`
				- Header: `field`
				- Content: `description` & `note_date` & `note`
		- API: /orders/notes?order_id={id}
		- [Detail](/order/get_notes.md)
	9. Xác nhận đã thanh toán phí:
		- Mô tả:
			- Xác nhận đã thu tiền phí.
		- API: /orders/pickup/collectFees/{id}
		- [Detail](/shipper/pickup/collect_fee.md)
	10. Upload hình ảnh lấy hàng.
		- Mô tả:
			- Upload hình ảnh lấy hàng.
		- API: /orders/pickup/upload/{id}
		- [Detail](/shipper/pickup/upload_photo.md)
	10. Upload hình ảnh chữ ký xác nhận của người gửi.
		- Mô tả:
			- Upload hình ảnh chữ ký xác nhận của người gửi.
		- API: /orders/pickup/upload/sign/{id}
		- [Detail](/shipper/pickup/upload_photo.md)
	11. Xác nhận lấy hàng thành công.
		- Mô tả:
		- API: /orders/pickup/confirm/{id}
		- [Detail](/shipper/pickup/confirm_pickup.md)
	13. Xác nhận lấy hàng thất bại.
		- Mô tả:
		- API: /orders/pickup/failed/{id}
		- [Detail](/shipper/pickup/failed_pickup.md)
	14. Chọn nguyên nhân thất bại.
		- Mô tả:
		- API: /configs/orders/notes/
		- [Detail](/config/order/order_note_reason_get.md)
5. Danh sách cần giao.
	1. Danh sách cần giao.
		- Mô tả:
			- Lấy ra các đơn hàng được group theo địa chỉ giao hàng trong ca hiện tại.
			- Nội dung:
				- Tên liên hệ giao hàng (varchar(50)): `receiver_name`
				- Số điện thoại liên hệ giao hàng (varchar(50)): `receiver_phone`
				- Địa chỉ giao hàng: `receiver_address`, `receiver_location_id`, `receiver_longitude`, `receiver_latitude`, `receiver_address_detail`
				- Tổng số đơn hàng ở địa chỉ này (int): `total`
				- Số đơn hàng đã giao tại địa chỉ này (int):` total_delivered`
				- Số đơn hàng đã giao thất bại tại địa chỉ này (int):` total_failed`
				- Mã trạng thái nhóm (int): `group_status_id`
				- Trạng thái nhóm  (varchar(50)): `group_status`
				- Tổng quan đơn hàng: `order`
					- Mã đơn (varchar(50)): `order_code`
					- Mã shop (varchar(50)): `user_code`
					- Đã trả phí (0 - chưa | 1 - đã trả) (int): `fee_paid`
					- Mã trạng thái đơn (int): `order_status_id`
					- Giảm giá (float): `discount`
					- Hình ảnh đơn hàng (array): `delivery_photos`, `delivery_signature_photo`
						- URL: `path`
					- Tiền phải thu (float): `cash`
					- Tên trạng thái (varchar(50)): `status`
					- Tên ca lấy hàng (string): `session`
		- API: /orders/delivery
		- [Detail](/shipper/delivery/drs.md)
	2. Thống kê:
		- Mô tả:
			- Thống kê dựa trên các đơn hàng có trong ca hiện tại.
			- Nội dung hiển thị:
				- Số đơn hàng đã lấy: picked
				- Số đơn hàng chưa lấy: picking
				- Số đơn hàng lấy thất bại: failed
				- Tiền thu shop: total_cash
		- API: /orders/delivery/statistics
		- [Detail](/shipper/delivery/statistics.md)
	3. Xem đơn hàng đã giao:
		- Mô tả:
			- Thống kê dựa trên các đơn hàng đã giao được group theo địa chỉ giao hàng có trong ca hiện tại.
			- Nội dung hiển thị:
				- Tên liên hệ giao hàng: receiver_name
				- Số điện thoại liên hệ giao hàng: receiver_phone
				- Địa chỉ giao hàng: receiver_address
				- Tổng số đơn hàng: total
		- API: /orders/delivery/statistics/delivered
		- [Detail](/shipper/delivery/delivered_orders.md)
	4. Xem đơn hàng chưa giao:
		- Mô tả:
			- Thống kê dựa trên các đơn hàng chưa giao được group theo địa chỉ giao hàng có trong ca hiện tại.
			- Nội dung hiển thị:
				- Tên liên hệ giao hàng: receiver_name
				- Số điện thoại liên hệ giao hàng: receiver_phone
				- Địa chỉ giao hàng: receiver_address
				- Tổng số đơn hàng: total
		- API: /orders/delivery/statistics/delivering
		- [Detail](/shipper/delivery/delivering_orders.md)
	5. Xem đơn hàng giao thất bại:
		- Mô tả:
			- Thống kê dựa trên các đơn hàng giao thất bại được group theo địa chỉ giao hàng có trong ca hiện tại.
			- Nội dung hiển thị:
				- Tên liên hệ giao hàng: receiver_name
				- Số điện thoại liên hệ giao hàng: receiver_phone
				- Địa chỉ giao hàng: receiver_address
				- Tổng số đơn hàng: total
		- API: /orders/delivery/statistics/failed
		- [Detail](/shipper/delivery/failed_orders.md)
	6. Xem các đơn hàng cùng địa chỉ giao hàng:
		- Mô tả: 
			- Thống kê các đơn hàng thuộc địa chỉ giao hàng có trong ca hiện tại.
			- Nội dung hiển thị:
				- Tên liên hệ giao hàng: receiver_name
				- Số điện thoại liên hệ giao hàng: receiver_phone
				- Địa chỉ giao hàng: receiver_address
				- Tổng số đơn hàng: total
				- Danh sách các đơn hàng.
		- API: /orders/delivery?receiver_address={address number/street}&receiver_location_id={id}&receiver_phone={phone number}
		- [Detail](/shipper/delivery/delivery_location_detail.md)
	7. Quét barcode.
		- Mô tả: 
		- API: /orders/delivery/check
		- [Detail](/shipper/delivery/check.md)
	8. Xem thông tin đơn hàng:
		- Mô tả:
			- Hiển thị thông tin chung của đơn hàng.
		- API: /orders/{id}
		- [Detail](/order/get.md)
	9. Xem lịch sử đơn hàng:
		- Mô tả:
			- Hiển thị thông tin lịch sử đơn hàng.
		- API: /orders/notes?order_id={id}
		- [Detail](/order/get_notes.md)
	10. Xác nhận lấy giao thành công.
		- Mô tả:
		- API: /orders/delivery/confirm/{id}
		- [Detail](/shipper/delivery/confirm_delivery.md)
	11. Xác nhận giao thất bại.
		- Mô tả:
		- API: /orders/delivery/failed/{id}
		- [Detail](/shipper/delivery/failed_delivery.md)
	12. Thêm (Upload hình ảnh).
		- Mô tả:
			- Upload hình ảnh giao hàng/ chữ ký xác nhận.
		- API: /orders/pickup/upload/{id}
		- [Detail](/shipper/pickup/upload_photo.md)
	13. Chọn nguyên nhân thất bại.
		- Mô tả:
		- API: /configs/orders/notes/
		- [Detail](/config/order/order_note_reason_get.md)
6. Xem yêu cầu.
	1. Xem các yêu cầu.
		- Mô tả: 
			- Hiển thị danh sách yêu cầu.
			- Nội dung hiển thị:
				- Mã đơn hàng: `order_code`.
				- Thời gian: `requests` -> `created`.
				- Tiêu đề: `requests` -> `order_request_type` -> `name`.
				- Nội dung: `requests` -> `description`.
				- Trạng thái xử lý: `status`.
				- Trạng thái đã xem: `requests` -> `read_status`.
		- API: /orders/requests
		- [Detail](/order/request_get.md).
	2. Xem chi tiết yêu cầu.
		- API lấy yêu cầu của 1 đơn hàng: /orders/requests?order_id={id}
		- API lấy 1 yêu cầu của 1 đơn hàng: /orders/requests?order_id={order id}&id={request id}
		- [Detail](/order/request_get.md).
8. Call log.
	- Ghi call log.
		- Mô tả: 
			- Ghi call log cho đơn hàng hiện tại.
			- Params:
				- ID đơn hàng: `order_id`.
				- Nội dung: `description`.
		- API: /orders/notes
		- [Detail](/order/note_create_shipper.md).
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
			- Đánh dấu đã xem thông báo.
			- Nội dung:
				- Mã thông báo: `ids`.
		- API: /users/notifications/read/{id}
		- [Detail](/user/notification_read.md).