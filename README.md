# 🐱 Catfe
<p align="center">
  <img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/ab34784a-1236-4dd2-918c-49277a460457" />
<p/>

<br/>

## 📖 프로젝트 개요
**Catfé**는 온라인 공간에서 실시간으로 소통하며 함께 공부하는 스터디 카페 플랫폼으로,  
실시간 스터디룸, 일정 관리, 커뮤니티, 파일 공유 기능을 통합 제공하는 협업 중심 서비스입니다.

<br/>

## 📎 팀 레포지토리 링크

- **Frontend Repository**: [GitHub - Catfe Frontend Repository](https://github.com/prgrms-web-devcourse-final-project/WEB5_6_Catfe_FE)  
- **Backend Repository**: [GitHub - Catfe Backend Repository](https://github.com/prgrms-web-devcourse-final-project/WEB6_8_Catfe_BE)

<br/><br/>

## 👥 팀원 소개

| 이름 | 프로필 | 역할 |
|------|--------|------|
| 김주은 | [@jueunk617](https://github.com/jueunk617) | 백엔드 팀장, 스터디룸 상호작용(캠·화면 공유·마이크·채팅), 알림 |
| 김선호 | [@KSH0326](https://github.com/KSH0326) | 스터디 플래너 |
| **남기은** | [@namgigun](https://github.com/namgigun) | **PO, 인프라 관리, CI/CD 파이프라인 구축, S3 파일 관리 API 제공** |
| 조예원 | [@joyewon0705](https://github.com/joyewon0705) | 사용자 인증/인가, 커뮤니티 |
| 진민호 | [@loseminho](https://github.com/loseminho) | 스터디룸 방 관리 |

<br/><br/>

## 🌟 주요 기능

| 기능 | 설명 |
|------|------|
| 🏠 스터디룸 | 화면 공유, 캠, 마이크를 통한 실시간 학습 공간 |
| 📅 스터디 플래너 | 목표 설정 및 일정 관리 |
| 💬 커뮤니티 | 스터디 그룹 탐색 및 팀원 모집 |
| 📁 파일 관리 | S3 연동 이미지 및 파일 업로드 |

<br/><br/>

## 🛠 기술 스택

| 구분 | 사용 기술 |
|------|------------|
| **Language** | `Java` |
| **Framework** | `Spring Boot` |
| **Database** | `MySQL`, `Redis` |
| **Infra** | `AWS(EC2, RDS, S3)`, `Docker`, `Nginx` |
| **DevOps** | `Github Actions`, `Terraform` |
| **Version Control** | `Git`, `Github` |
| **Collaboration** | `Notion`, `Slack`, `Discord` |

<br/><br/>

## 🗂 ERD

<p align="center">
  <img width="900" height="900" alt="image" src="https://github.com/user-attachments/assets/af6dafdf-7e68-4e86-9e69-076aa5b2d5fc"/>
</p>

<br/>

## 🏗 시스템 아키텍처

<img width="900" height="600" alt="image" src="https://github.com/user-attachments/assets/31fe0a33-c6f6-46b4-9913-6b4e3a618b18" />

## CI/CD

<img width="900" height="600" alt="image" src="https://github.com/user-attachments/assets/63799042-abc7-4b97-a9e4-e6b4045bf829" />


## 👤 팀 내 수행 역할

### 개발 프로세스 및 협업 환경 설계

**설계의도**
- 팀 단위 개발에서 발생할 수 있는 코드 충돌과 책임 불명확 문제를 해결하기 위해 **이슈 → 브랜치 → PR → 머지 → 정리** 흐름을 표준화
- 반복적인 브랜치 관리 및 검증 작업을 자동화하여 개발자는 기능 구현에 집중할 수 있는 환경을 구축
- 통합/배포 브랜치에는 검증 절차(CI, 리뷰)를 반드시 거치도록 강제하여 안정적인 코드 품질을 유지

<details>
<summary> 개발 규칙 및 협업 프로세스 </summary>
  
## 1. 브랜치 전략
- **`dev`**: 통합 브랜치
  - 모든 기능 개발은 feature 브랜치를 만들어 `dev`에 PR로 머지
  - 직접 push 및 외부 PR은 제한

- **`main`**: 배포 브랜치
  - 안정화된 코드를 머지하여 배포
  - `dev` → `main` PR은 관리자 혹은 릴리즈 담당자만 생성 및 승인 가능
  - 직접 push 및 외부 PR 제한
    <br/>

## 2. 커밋/PR/Issue 컨벤션

### 타입
- Feat : 새로운 기능 추가
- Fix : 버그 수정
- Env : 개발 환경 관련 설정
- Style : 코드 스타일 수정 (세미 콜론, 인덴트 등의 스타일적인 부분만)
- Refactor : 코드 리팩토링 (더 효율적인 코드로 변경 등)
- Design : CSS 등 디자인 추가/수정
- Comment : 주석 추가/수정
- Docs : 내부 문서 추가/수정
- Test : 테스트 추가/수정
- Chore : 빌드 관련 코드 수정
- Rename : 파일 및 폴더명 수정
- Remove : 파일 삭제

### 메시지 양식
```
Feat: 로그인 함수 추가 -> 제목

로그인 요청을 위한 함수 구현 -> 본문
```
<br/>

## 3. 개발 프로세스
```
1. 이슈 생성

  제목 양식 -> {Issue Type: {이슈내용}}
  예시) Feat: 로그인 함수 추가

2. feature 브랜치 자동생성

  자동으로 생성된 feature 브랜치 이름 (이슈 번호가 1번이라 가정) -> Feat/1

3. 해당 브랜치에서 작업 후 dev 브랜치에 PR 요청 (main 브랜치에는 직접 PR 금지)

4. PR 요청 시,

  - 모든 Status Check(CI) 통과 필요
  - 최소 2명 이상의 승인 필요

5. 승인받은 후 Squash & Merge 진행

6. Merge 후,

  - feature 브랜치 자동 삭제
  - 연관된 이슈 자동으로 닫힘
```


<br/>

## 4. 브랜치 보호 규칙

| 브랜치 | 보호 규칙 |
|--------|-----------|
| main   | 직접 push 금지, Force push 금지, 모든 CI 통과 필수, 관리자만 PR 가능 |
| dev    | 직접 push 금지, 리뷰 최소 2명 필수, 모든 CI 통과 필수 |


</details>

**성과**
- feature 브랜치에서 개발하고 dev 브랜치로 통합하는 개발 규칙을 적용하여 `GitHub-Flow` 기반 브랜치 전략을 설계함으로써 
  **기능 단위 개발 흐름을 명확히 하고, 팀 내 코드 충돌을 구조적으로 방지**
- 이슈 생성 시 작업 브랜치를 자동 생성·머지 이후 자동 삭제하는 `GitHub Actions` 워크플로우를 구축하여 
  **브랜치 관리에 소요되던 반복 작업을 제거하고 협업 생산성을 향상**
- PR 단계에서 자동 빌드·테스트를 실행하고 2인 이상 승인 규칙을 적용하여
  **실행되지 않는 코드의 병합을 사전에 차단하고, 통합 브랜치의 코드 품질을 안정적으로 유지**

<br/>

### 인프라 관리 (Terraform)

**설계의도**
- AWS 콘솔에서 수동 설정 없이, 인프라 구성을 코드로 정의하고 관리하기 위해 **Infrastructure as Code(IaC)** 방식으로 Terraform을 도입
- 팀원들이 Terraform에 대한 기본적인 이해를 갖추고 있었기 때문에, 다른 IaC 도구 대비 **학습 비용과 협업 리스크가 낮은 Terraform을 선택**
- 현재 프로젝트에서 사용 중인 AWS 리소스(EC2, RDS, S3 등)를 코드로 표현하여 **팀원들이 인프라 구성 현황을 쉽게 파악하고 공유할 수 있는 구조를 만들고자 함**
- 프로젝트 기간 이후 AWS 계정이 정리되는 상황을 고려하여, **Terraform 코드만으로도 동일한 인프라를 개인 계정에 재현·이관할 수 있도록 인프라를 관리**

**수행내용**

- AWS 리소스 Terraform 코드로 관리
```hcl
resource "aws_instance" "ec2_1" {
  ami           = "ami-077ad873396d76f6a"
  instance_type = "t3.micro"

  subnet_id              = aws_subnet.subnet_1.id
  vpc_security_group_ids = [aws_security_group.sg_1.id]

  associate_public_ip_address = true

  # 인스턴스에 IAM 역할 설정
  iam_instance_profile = aws_iam_instance_profile.instance_profile_1.name

  tags = {
    Key   = "TEAM"
    Value = "devcos-team05"
    Name  = "team5-ec2-1"
  }

  # 루트 불륨 설정
  root_block_device {
    volume_type = "gp3"
    volume_size = 12
  }

  # EC2 실행 시, 작업진행
  user_data = <<-EOF
${local.ec2_user_data_base}
EOF
}
```

- 인프라 변경 이력 공유
<img width="900" height="600" alt="image" src="https://github.com/user-attachments/assets/23ac17e7-3711-47a9-b5e4-b39648659a97" />

<br/><br/>

### CI/CD 파이프라인 구축

**구현 목적**
- main 브랜치에 머지된 코드가 서버에 자동 반영되도록 CI/CD 파이프라인을 구축

**핵심 구현 내용**

1. main 브랜치 PR 시도 시, 자동 빌드 테스트 진행
- main 브랜치로 변경 사항에 대해 GitHub Actions를 통해 자동 빌드 및 테스트를 수행하도록 구성

```yaml

# PR 이벤트 트리거 (main, dev 브랜치 대상으로)
on:
  pull_request:
    branches:
      - main
    types: [opened, synchronize, reopened]

jobs:
  build-and-test-main:
    if: github.base_ref == 'main' # main 브랜치로 PR이 들어올 때만 실행
    runs-on: ubuntu-latest

  steps:
      # Build (테스트 제외)
      - name: Build project
        run: ./gradlew clean build -x test

      # Test 실행
      - name: Run tests
        run: ./gradlew test

```

2. 도커 이미지 빌드 및 푸시
- 빌드 및 테스트가 완료되면, 애플리케이션을 Docker 이미지로 빌드한 뒤, GitHub Container Registry(GHCR)에 이미지를 푸시하도록 구성

- 이미지는 다음 두 가지 태그 전략으로 관리
  - 릴리즈 태그 기반 이미지: 배포 이력 추적 및 롤백 용도
  
  - latest 태그: 항상 최신 버전을 가리키는 운영용 태그
 
```yaml

buildImageAndPush:
  - name: 빌드 앤 푸시
    uses: docker/build-push-action@v3
    with:
      context: .
      push: true
      tags: |
        ghcr.io/${{ env.OWNER_LC }}/${{ env.DOCKER_IMAGE_NAME }}:${{ needs.makeTagAndRelease.outputs.tag_name }},
        ghcr.io/${{ env.OWNER_LC }}/${{ env.DOCKER_IMAGE_NAME }}:latest
```

3. 배포 스크립트 EC2 서버에 전송
- 운영 환경 배포 시 서비스 중단을 방지하기 위해 Blue-Green 배포 전략을 적용

  **배포 프로세스**

  - 현재 트래픽을 처리 중인 컨테이너(Blue)는 유지

  - 신규 버전 컨테이너(Green)를 별도로 기동

  - 헬스 체크 성공 시 프록시 업스트림을 Green으로 전환

  - 기존 Blue 컨테이너 종료 및 정리

```yaml

- name: AWS SSM Send-Command
    command: |
      # 현재 프록시가 바라보는 업스트림(컨테이너명) 조회
      CURRENT_HOST=$(curl -s -X GET "http://127.0.0.1:81/api/nginx/proxy-hosts/${PROXY_ID}" \
        -H "Authorization: Bearer ${TOKEN}" \
        | jq -r '.forward_host')
      
      echo "🔎 CURRENT_HOST: ${CURRENT_HOST:-none}"
      
      
      # Green(최신 Spring 서버) 역할 컨테이너 실행
      docker rm -f "${GREEN}" > /dev/null 2>&1 || true
      echo "run new container -> ${GREEN}"
      docker run -d --name "${GREEN}" \
        --restart unless-stopped \
        --network "${NET}" \
        -e TZ=Asia/Seoul \
        "${IMAGE}"
      
      
      # 최신 Spring 서버 헬스체크
      echo "⏱ health-check: ${GREEN}"
      TIMEOUT=120
      INTERVAL=3
      ELAPSED=0
      sleep 8 # 초기부팅 여유
      
      while (( ELAPSED < TIMEOUT )); do
        CODE=$(docker exec "${GREEN}" curl -s -o /dev/null -w "%{http_code}" "http://127.0.0.1:${PORT_IN}/actuator/health" || echo 000)
        [[ "${CODE}" == "200" ]] && { echo "✅ ${GREEN} healthy"; break; }
        sleep "${INTERVAL}"
        ELAPSED=$((ELAPSED + INTERVAL))
      done
      [[ "${CODE:-000}" == "200" ]] || { echo "❌ ${GREEN} health failed"; docker logs --tail=200 "${GREEN}" || true; docker rm -f "${GREEN}" || true; exit 1; }
      
                  
      # 업스트림 전환
      NEW_CFG=$(jq -n --arg host "${GREEN}" --argjson port ${PORT_IN} '{forward_host:$host, forward_port:$port}')
      curl -s -X PUT "http://127.0.0.1:81/api/nginx/proxy-hosts/${PROXY_ID}" \
        -H "Authorization: Bearer ${TOKEN}" \
        -H "Content-Type: application/json" \
        -d "${NEW_CFG}" >/dev/null
      echo "🔁 switch upstream → ${GREEN}:${PORT_IN}"

      # 이전 Blue 종료
      if [[ "${BLUE}" != "none" ]]; then
        docker stop "${BLUE}" >/dev/null 2>&1 || true
        docker rm "${BLUE}" >/dev/null 2>&1 || true
        echo "🧹 removed old blue: ${BLUE}"
      fi
      
      # Blue 이미지 정리
      {
        docker images --format '{{.Repository}}:{{.Tag}}' \
          | grep -F "ghcr.io/${OWNER_LC}/${IMAGE_REPOSITORY}:" \
          | grep -v -F ":${IMAGE_TAG}" \
          | grep -v -F ":latest" \
          | xargs -r docker rmi
      } || true

```
<br/><br/>

### 파일 업로드 API 구현

**구현 목적** 
<br/><br/>
프론트엔드에서 S3에 파일과 관련된 기능을 백엔드 API를 통해 처리할 수 있도록 구현

<br/>

**구현 방식** 
<br/><br/>
파일 업로드 방식은 사용 목적과 파일 크기에 따라 MultiPartFile 방식과 Presigned URL 방식을 병행하여 구현

1. MultiPartFile 기반 파일 업로드

  - Spring Boot에서 제공하는 MultipartFile을 활용하여 서버에서 파일을 직접 수신하고 저장하는 방식으로 1차 구현을 진행

    - 클라이언트로 부터 파일을 받아 서버는 S3에 파일을 업로드
  
    - 서버는 받은 파일 정보를 저장
  
    - 클라이언트에게 S3에 저장된 파일의 public URL을 반환

```java

@Transactional
public FileUploadResponseDto uploadFile(
        MultipartFile multipartFile,
        Long userId
) {
    User user = userRepository.findById(userId)
            .orElseThrow(() ->
                    new CustomException(ErrorCode.USER_NOT_FOUND)
            );

    // S3에 저장할 파일 이름
    String storedFileName = createFileName(multipartFile.getOriginalFilename());

    // S3의 저장된 파일의 PublicURL
    String publicURL = s3Upload(storedFileName, multipartFile);

    // FileAttachment 정보 저장
    FileAttachment fileAttachment = fileAttachmentRepository.save(
            new FileAttachment(
                    storedFileName,
                    multipartFile,
                    user,
                    publicURL
            )
    );

    return new FileUploadResponseDto(fileAttachment.getId(), publicURL);
}

```

2. Presigned URL 기반 파일 업로드
  - 대용량 파일 업로드 및 서버 부하를 최소화하기 위해 Presigned URL 기반 업로드 방식을 추가로 도입

    - 클라이언트는 파일 업로드 전, 백엔드로부터 Presigned URL 발급
 
    - 서버는 URL 발급 역할만 수행

```java
public PresignedUrlResponseDto generateUploadPresignedUrl(String folder, String originalFileName) {
      String key = folder + "/" + UUID.randomUUID() + "-" + originalFileName;

      PutObjectRequest objectRequest = PutObjectRequest.builder()
              .bucket(bucket)
              .key(key)
              .build();

      // Presigned URL 발급 요청
      PresignedPutObjectRequest presignedRequest = s3Presigner.presignPutObject(
              request -> request.putObjectRequest(objectRequest)
                      .signatureDuration(Duration.ofMinutes(5L))
      );

      String objectUrl = String.format(
              "https://%s.s3.%s.amazonaws.com/%s",
              bucket,
              region,
              key
      );

      return new PresignedUrlResponseDto(presignedRequest.url().toString(), objectUrl);
}
```
<br/><br/>

## 🚨 트러블 슈팅

### 구글 로그인 redirect_uri_mismatch 문제

**문제 상황**
- 배포 환경에서 구글 로그인 테스트 중 `redirect_uri_mismatch` 오류가 발생하여 로그인 진행 불가

**원인 분석**
- 클라이언트는 HTTPS로 요청을 전송했으나, Nginx를 거쳐 Spring 서버로 전달되는 과정에서 프로토콜 정보가 전달되지 않음
- 이로 인해 Spring 서버가 요청을 HTTP로 인식하여, Google OAuth에 등록된 redirect URI(HTTPS)와 불일치 발생

**해결 방법**
- Nginx에서 클라이언트의 실제 요청 정보를 Spring 서버로 전달하도록 설정
- `X-Forwarded-Proto` 헤더를 포함하여 HTTPS 요청임을 서버가 인식할 수 있도록 구성

```nginx
# Nginx Proxy Manager - Advanced 설정

proxy_set_header Host $host;
proxy_set_header X-Forwarded-Proto $scheme;
proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
```

**결과**
- 해당 설정 적용 후, 서버에서 HTTPS 요청을 정상적으로 인식
- 구글 로그인 성공

<br/>

### 기존 배포 방식의 다운타임 발생 문제

**문제 상황**
- 기존 배포 방식에서는 새로운 버전을 배포하는 과정에서 서비스가 일시적으로 중단되는 다운타임이 발생

**원인 분석**
- 기존 배포 방식은 실행 중인 Spring 컨테이너를 종료한 후 새로운 컨테이너를 기동하는 구조
- 이로 인해 기존 컨테이너 종료 시점부터 신규 컨테이너가 정상 기동될 때까지 요청을 처리할 서버가 없어 서비스 중단이 발생

**해결 방법**
- Nginx 기반 Blue-Green 배포 전략을 도입하여 신규 버전 배포 시에도 서비스가 중단되지 않는 무중단 배포 환경을 구축

- 도입한 배포 프로세스
  1. 현재 트래픽을 처리 중인 컨테이너(Blue)는 유지

  2. 신규 버전 컨테이너(Green)를 별도로 기동

  3. Green 컨테이너에 대해 애플리케이션 헬스 체크 수행

  4. 헬스 체크 성공 시 Nginx 프록시의 업스트림을 Green으로 전환

  5. 트래픽 전환이 완료된 후 기존 Blue 컨테이너 종료 및 정리

**결과**
- 배포 과정 중 서비스 중단 없이 신규 버전 배포 가능
- 헬스체크 성공 이후에만 트래픽을 전환함으로써, 신규 서버 실행이 실패해도 기존 서비스는 영향을 받지 않음

<br/>

### 대용량 업로드 실패 문제

**문제 상황**
- API 테스트 과정에서 기존 MultipartFile 기반 파일 업로드 방식으로는 대용량 파일 업로드 시 요청이 실패하는 문제가 발생

**원인 분석**
- MultipartFile 방식은 클라이언트가 업로드한 파일을 서버가 직접 수신하고 처리한 후 S3로 전달하는 구조
- 대용량 파일의 경우 요청 처리 시간이 길어져 서버 타임아웃이 발생

**접근 방식**
- 서버가 대용량 파일을 직접 처리하는 구조 자체를 제거하기 위해 Presigned URL 기반 파일 업로드 방식을 도입
- 서버는 S3에 업로드 가능한 Presigned URL만 발급
- 클라이언트는 발급받은 Presigned URL을 통해 S3에 직접 파일 업로드
- 이를 통해 서버는 대용량 파일 전송 경로에서 완전히 분리되도록 구조를 개선

**결과**
- 대용량 파일 업로드 실패 문제 해결
- 1.8GB 파일 업로드 기준
  - MultipartFile 방식: 서버 CPU 사용률 약 7%
  
  - Presigned URL 방식: 서버 CPU 사용률 약 1%

- 서버 부하 감소 및 파일 업로드 처리 안정성 향상
