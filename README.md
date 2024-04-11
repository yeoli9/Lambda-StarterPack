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

인증서 이슈로 바로 적용안될 수 있음

```bash
curl -XGET -H 'MyCustomAuthHeader:allow' https://api.example.com/hello  # change your custom domain
```
