# SHIPPER APIs.

1. Đăng nhập.
	- API: /users/login
	- [Detail](user/login.md)
	- Example notify: [Detail](order/notification.md).
2. Đăng ký push notification token.
	- API: /users/notifications/register
	- [Detail](/user/register_push_token.md).
3. Cập nhật vị trí.
	- API: /users/profile/locations
	- [Detail](/shipper/profile/update_location.md).
4. Danh sách cần lấy.
	1. Danh sách cần lấy: 
		- Mô tả:
			- Lấy ra các đơn hàng được group theo địa chỉ lấy hàng trong ca hiện tại.
			- Nội dung hiển thị:
				- Tên liên hệ lấy hàng: sender_name
				- Số điện thoại liên hệ lấy hàng: sender_phone
				- Địa chỉ lấy hàng: sender_address, sender_location_id, sender_longitude, sender_latitude, sender_address_detail
				- Tổng số đơn hàng ở địa chỉ này: total
				- Số đơn hàng đã lấy tại địa chỉ này: total_picked_up
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
		- API: /orders/{id}
		- [Detail](/order/get.md)
	8. Xem lịch sử đơn hàng:
		- Mô tả:
			- Hiển thị thông tin lịch sử đơn hàng.
		- API: /orders/notes?order_id={id}
		- [Detail](/order/get_notes.md)
	9. Xác nhận đã thanh toán phí:
		- Mô tả:
			- Xác nhận đã thu tiền phí.
		- API: /orders/pickup/collectFees/{id}
		- [Detail](/shipper/pickup/collect_fee.md)
	10. Thêm (Upload hình ảnh).
		- Mô tả:
			- Upload hình ảnh lấy hàng/ chữ ký xác nhận của người gửi.
		- API: /orders/pickup/upload/{id}
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
	11. Xác nhận lấy giao thất bại.
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
		- [Detail](../order/request_get.md).
	2. Xem chi tiết yêu cầu.
		- API lấy yêu cầu của 1 đơn hàng: /orders/requests?order_id={id}
		- API lấy 1 yêu cầu của 1 đơn hàng: /orders/requests?order_id={order id}&id={request id}
		- [Detail](../order/request_get.md).
8. Call log.
	- Ghi call log.
		- Mô tả: 
			- Ghi call log cho đơn hàng hiện tại.
			- Params:
				- ID đơn hàng: `order_id`.
				- Nội dung: `description`.
		- API: /orders/notes
		- [Detail](/order/note_create_shipper.md).