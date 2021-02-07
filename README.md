# API status

- 200 Ok: Trả về thành công cho những phương thức GET, PUT, PATHCH, DELETE
- 201 Created: Trả về khi một Resource vừa được tạo thành công.
- 204 No Content: Trả về khi một Resource xóa thành công.

- 304 Not Modified: Client có thể sử dụng dữ liệu cache.

- 400 Bad Request: Request không hợp lệ.
- 401 Unauthorized: Cần auth.
- 403 Forbidden: Bị từ chối không cho phép.
- 404 Not Found: Không tìm thấy resource từ URI.
- 405 Method Not Allowed: Phương thức không cho phép với user hiện tại.
- 410 Gone - Resource không tồn tại, Version đã cũ không còn hỗ trợ.
- 415 Unsupport Media Type - Không hỗ trợ kiểu Resource này.
- 422 Unprocessable Entity - Dữ liệu không xác thực.
- 429 Too Many Request - Resource bị từ chối do bị giới hạn. 
