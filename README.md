# MyPertamina
Un-Official MY PERTAMINA API Wrapper

## REGISTER
 [POST] https://api.my-pertamina.id/customer/v2/register

    :method: POST
    :scheme: https
    :path: /customer/v2/register
    :authority: api.my-pertamina.id
    accept: */*
    content-type: application/json
    authorization: Basic dGVsa29tOmRhMWMyNWQ4LTM3YzgtNDFiMS1hZmUyLTQyZGQ0ODI1YmZlYQ==
    accept-encoding: br;q=1.0, gzip;q=0.9, deflate;q=0.8
    user-agent: MyPertamina/2.16.1 (com.pertamina.mypertamina; build:117; iOS 14.4.0) Alamofire/5.4.3
    content-length: 105
    accept-language: id-ID;q=1.0
    
    {"name":"NAMA LENGKAP","dob":"1945-08-17","pin":"pRjV7LSvzBGrX9MWeSJ+Ew==","mobileNumber":"081234567890"}
	

## SEND OTP REGISTER
[POST] https://api.my-pertamina.id/notification/v1/otp/customer/sms/send

    :method: POST
    :scheme: https
    :path: /notification/v1/otp/customer/sms/send
    :authority: api.my-pertamina.id
    content-type: application/json
    accept: */*
    authorization: Basic dGVsa29tOmRhMWMyNWQ4LTM3YzgtNDFiMS1hZmUyLTQyZGQ0ODI1YmZlYQ==
    namespace: OTP Register
    usecase: OTP-REGISTER
    accept-language: id-ID;q=1.0
    accept-encoding: br;q=1.0, gzip;q=0.9, deflate;q=0.8
    origin: Mypertamina 2.16.1 - customer iOS
    content-length: 31
    user-agent: MyPertamina/2.16.1 (com.pertamina.mypertamina; build:117; iOS 14.4.0) Alamofire/5.4.3
    
    {"mobileNumber":"081234567890"}

## VERIFY OTP REGISTER
[POST] https://api.my-pertamina.id/customer/v2/auth/registration/otp/verification

    :method: POST
    :scheme: https
    :path: /customer/v2/auth/registration/otp/verification
    :authority: api.my-pertamina.id
    accept: */*
    content-type: application/json
    authorization: Basic dGVsa29tOmRhMWMyNWQ4LTM3YzgtNDFiMS1hZmUyLTQyZGQ0ODI1YmZlYQ==
    accept-encoding: br;q=1.0, gzip;q=0.9, deflate;q=0.8
    user-agent: MyPertamina/2.16.1 (com.pertamina.mypertamina; build:117; iOS 14.4.0) Alamofire/5.4.3
    content-length: 46
    accept-language: id-ID;q=1.0
    
    {"mobileNumber":"081234567890","otp":"6275XX"}
	
## LOGIN
[POST] https://api.my-pertamina.id/customer/v2/auth/login

    :method: POST
    :scheme: https
    :path: /customer/v2/auth/login
    :authority: api.my-pertamina.id
    x-geolocation: -7.412059783935547,94.95267681448584
    content-type: application/json
    accept: */*
    authorization: Basic dGVsa29tOmRhMWMyNWQ4LTM3YzgtNDFiMS1hZmUyLTQyZGQ0ODI1YmZlYQ==
    accept-encoding: br;q=1.0, gzip;q=0.9, deflate;q=0.8
    x-device-id: 9183F0ED-4C17-4E98-A32B-14BAAAE8776A
    user-agent: Mypertamina 2.16.1;iOS 14.4;iPhone 8
    content-length: 241
    accept-language: id-ID;q=1.0
    
    {"pin":"pRjV7LSvzBGrX9MWeSJ+Ew==","mobileNumber":"081234567890","fcmToken":"fP46F6f1001ophkFVeZzmv:APA91bH9-wXcnvH0LZwD9-VKlcrOZob7KyxQgNyEVji9s6tjSGpSUKbTiHoXpx63thCxmOB4deF7Ns0UIObn71fBN2w-TxkVu168JCl2zmgU92vZsMgiZlMRrG0hSm7-MyOnIo3FWN9z"}
	

Response 
```json
 {
    	"success": true,
    	"data": {
    		"name": "Vladimir Putin",
    		"token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.XXXXX"
    	},
    	"message": "Customer credentials",
    	"code": 200
    }
```
## PROFILE INFO
[GET]  https://api.my-pertamina.id/user/v1/customers/profile/me
```
:method: GET
:scheme: https
:path: /user/v1/customers/profile/me
:authority: api.my-pertamina.id
accept: */*
content-type: application/json
accept-encoding: br;q=1.0, gzip;q=0.9, deflate;q=0.8
user-agent: MyPertamina/2.16.1 (com.pertamina.mypertamina; build:117; iOS 14.4.0) Alamofire/5.4.3
accept-language: id-ID;q=1.0
authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.XXXXX
```
