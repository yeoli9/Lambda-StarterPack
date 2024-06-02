# Lambda Starter pack Demo

## SAM 소개

## 프로젝트 만드는 법

## SAM 명령어 간단 소개

## SAM 선행조건

- AWS CLI
- AWS IAM AdministratorAccess
- SAM cli installation
- SAM init
- hostzone, custom domain 설정
- API Gateway Authorizer 설정
- template.yaml 업데이트
- 배포

### 배포

```bash
sam build && sam deploy --profile $YOUR_PROFILE --no-confirm-changeset # 적절한 Profile로 변경해주세요.
```

```bash
curl -XGET -H 'MyCustomAuthHeader:allow' https://api.example.com/hello  # change your custom domain
```

## Issue

- 인증서 배포에 시간이 걸려 실제 호출에 시간이 걸릴 수 있음
  - 늦어도 10분 내에 배포 완료
- 배포 중 종료하게되면 관련된 리소스를 모두 삭제 후 다시 배포할 것
- 배포하는 자격증명에 권한이 부족할 수 있음
  - Route53
  - API Gateway
  - ACM
  - Lambda
  - IAM
  - 등 적절한 권한이 있는지 확인할 것
