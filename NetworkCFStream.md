# Network

예제를 통해 JSON - GET,POST 해봄

# Alamofire (https://github.com/Alamofire/Alamofire)

Alamofire는 iOS, macOS를 위한 스위프트 기반 HTTP 네트워킹 라이브러리 (AFNetwork의 스위프트 버전)

비동기로 네트워크 연동

서버로부터 응답을 받을 때까지 기다리지 않고 콜백을 통해 응답을 처리하는 구조

request에 대한 response 는 이를 처리하는 핸들러 안에서 유효하므로, 수신한 response나 data에 의존적인 동작들은 반드시 해당 핸들러 내에서 완료해야함

![image](/uploads/d832e2f07e488911931b9faa86c1a04e/image.png)

# SwiftyJSON (https://github.com/SwiftyJSON/SwiftyJSON)

Alamofire와 호환 가능하고, JSON 파싱 자동화를 도와주는 라이브러리

