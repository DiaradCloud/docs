# احراز هویت (Auth API)

همه‌ی درخواست‌ها به API نیاز به توکن احراز هویت دارند.

## دریافت توکن
```http
POST /api/auth/login
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "your-password"
}
```
## پاسخ موفق
```json
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}
```
# استفاده از توکن
توکن را در هدر Authorization قرار دهید:
```http
GET /api/abrak/list
Authorization: Bearer <your-token>
```
