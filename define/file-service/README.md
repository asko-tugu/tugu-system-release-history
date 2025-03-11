# 📂 Storage S3 저장 구조

## **📌 Profile Photo 저장 경로**

| 타입           | 경로                                                |
| -------------- | --------------------------------------------------- |
| **User**       | `<bucket> / tugu / profile / user / <object>`       |
| **Admin**      | `<bucket> / tugu / profile / admin / <object>`      |
| **SuperAdmin** | `<bucket> / tugu / profile / superadmin / <object>` |
| **Company**    | `<bucket> / tugu / profile / company / <object>`    |
| **WorkPlace**  | `<bucket> / tugu / profile / workplace / <object>`  |
| **Room**       | `<bucket> / tugu / profile / room / <object>`       |

---

## **📌 Room File 저장 경로**

| 타입      | 경로                                                    |
| --------- | ------------------------------------------------------- |
| **Voice** | `<bucket> / tugu / room / <room id> / voice / <object>` |
| **Photo** | `<bucket> / tugu / room / <room id> / photo / <object>` |
| **File**  | `<bucket> / tugu / room / <room id> / file / <object>`  |

---

## **📌 파일(object) 저장 형식**

- **파일명 형식:** `<day(utc)>-<uuid>`
  - 📌 **예시:** `20250306-c8d9f7a2-3c4b-4d5e-9f8a-b1c2d3e4f567`
- **파일 메타정보 (Size / Duration / Type)**
  - 📌 **클라이언트에서 제공됨**

---

## **🛠 개발 환경**

- **S3 개발 환경 저장 경로:**
  - 📌 `<bucket> / tugu-dev / ….(하위)`

### **📌 API Documentation**

- [📄 Swagger API Docs](https://api-dev.aswing.net/file-service/docs#/)

### **📌 프로필 사진 Test Code**

- **User Profile Photo:** [🔗 테스트 코드](https://github.com/asko-tugu/tugu-backend-tester/blob/main/test/file-service/profile-photo/file-service.user.profile-photo.test.ts)
- **Company Profile Photo:** [🔗 테스트 코드](https://github.com/asko-tugu/tugu-backend-tester/blob/main/test/file-service/profile-photo/file-service.company.profile-photo.test.ts)
- **WorkPlace Profile Photo:** [🔗 테스트 코드](https://github.com/asko-tugu/tugu-backend-tester/blob/main/test/file-service/profile-photo/file-service.work-place.profile-photo.test.ts)
- **Room Profile Photo:** [🔗 테스트 코드](https://github.com/asko-tugu/tugu-backend-tester/blob/main/test/file-service/profile-photo/file-service.room.profile-photo.test.ts)

### **📌 Room File Test Code**

- **Room 일반 File:** [🔗 테스트 코드](https://github.com/asko-tugu/tugu-backend-tester/blob/main/test/file-service/room-file/file-service.room-file.test.ts)
- **Room Voice File:** [🔗 테스트 코드](https://github.com/asko-tugu/tugu-backend-tester/blob/main/test/file-service/room-file/file-service.room-voice-file.test.ts)
- **Room Image File:** [🔗 테스트 코드](https://github.com/asko-tugu/tugu-backend-tester/blob/main/test/file-service/room-file/file-service.room-image-file.test.ts)
