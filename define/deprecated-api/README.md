# Deprecated API 관리 문서

## 개요

이 문서는 더 이상 사용되지 않는 API 및 이를 적용했던 클라이언트(AOS, Control, Admin, Super Admin)별 사용 여부를 정리한 것입니다. 해당 API들은 새로운 버전으로 대체되었으며, 점진적으로 제거될 예정입니다.

## 개발 및 실서버 Swagger 문서

| 환경            | Backend                                                  | Auth                                                  | File                                                           |
| --------------- | -------------------------------------------------------- | ----------------------------------------------------- | -------------------------------------------------------------- |
| **개발 환경**   | [Backend Swagger](https://api-dev.aswing.net/api/docs#/) | [Auth Swagger](https://api-dev.aswing.net/api/docs#/) | [File Swagger](https://api-dev.aswing.net/file-service/docs#/) |
| **실서버 환경** | [Backend Swagger](https://api.aswing.net/api/docs#/)     | [Auth Swagger](https://api.aswing.net/api/docs#/)     | [File Swagger](https://api.aswing.net/file-service/docs#/)     |

## 변경 매트릭스

| 서비스 이동        | Deprecated API                      | 변경 API                                     | AOS | Control | Admin | Super Admin |
| ------------------ | ----------------------------------- | -------------------------------------------- | --- | ------- | ----- | ----------- |
| **Backend → Auth** | `/api/auth/login`                   | `/auth-service/v1/auth/user/login`           | ✅  |         |       |             |
| **Backend → Auth** | `/api/auth/logout`                  | `/auth-service/v1/auth/user/logout`          | ✅  |         |       |             |
| **Backend → Auth** | `/api/verify`                       | `/auth-service/v1/verify`                    | ✅  |         | ⬜    | ⬜          |
| **Backend → Auth** | `/api/verify/check/{verifyType}`    | `/auth-service/v1/verify/check/{verifyType}` | ✅  |         | ⬜    | ⬜          |
| **Backend → Auth** | `/api/send/email`                   | `/auth-service/v1/send/email`                | ⬜  |         | ⬜    | ⬜          |
| **Backend → Auth** | `/api/send/sms`                     | `/auth-service/v1/send/sms`                  | ⬜  |         | ⬜    | ⬜          |
| **Backend → Auth** | `/api/admin/login`                  | `/auth-service/v1/auth/admin/login`          |     | ⬜      | ⬜    |             |
| **Auth**           | (신규)                              | `/auth-service/v1/auth/admin/logout`         |     | ⬜      | ⬜    |             |
| **Backend → Auth** | `/api/superAdmin/login`             | `/auth-service/v1/auth/superAdmin/login`     |     |         |       | ⬜          |
| **Auth**           | (신규)                              | `/auth-service/v1/auth/admin/logout`         |     |         |       | ⬜          |
| **Backend**        | `/api/user-data/list/{workPlaceId}` | `/api/user-data/{workPlaceId}/{userId}/data` |     |         | ⬜    |             |
| **Backend**        | `/api/roomInvite`                   | `/api/v1/roomInvite`                         | ⬜  | ⬜      | ⬜    |             |
| **Backend**        | `/api/device`                       | `/api/v1/device/register`                    | ✅  |         | ⬜    |             |
| **Backend**        | (신규)                              | `/api/v1/device/checkName`                   | ✅  |         | ⬜    |             |
| **Backend(신규)**  | (신규)                              | `/api/v1/device/checkNamePattern`            | ✅  |         | ⬜    |             |

## 참고 사항

- Deprecated API는 점진적으로 제거될 예정이므로 대체 API로 마이그레이션해야 합니다.
- 변경 API는 서비스별로 나뉘어 있으며, 필요 시 서비스 구성도 변경될 수 있습니다.
- 적용되지 않는 클라이언트는 빈 공간으로 유지되었습니다.
