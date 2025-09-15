---
layout: page
title: Nextflow 시작하기
parent: 튜토리얼
---

# Nextflow 시작하기

이 가이드는 Nextflow를 처음 사용하는 분들을 위한 단계별 설치 및 실행 가이드입니다.

## 사전 요구사항

- Java 8 이상 (Java 11 권장)
- Unix 계열 운영체제 (Linux, macOS)

## 설치

### 1. 자동 설치 (권장)

```bash
curl -s https://get.nextflow.io | bash
```

### 2. 수동 설치

```bash
wget -qO- https://get.nextflow.io | bash
chmod +x nextflow
sudo mv nextflow /usr/local/bin/
```

### 3. 설치 확인

```bash
nextflow -version
```

## 첫 번째 워크플로우

### Hello World 예제

`hello.nf` 파일을 생성하고 다음 내용을 입력합니다:

```groovy
#!/usr/bin/env nextflow

process sayHello {
    input:
    val name

    output:
    stdout

    script:
    """
    echo 'Hello $name!'
    """
}

workflow {
    Channel.of('World', 'Korea', 'Nextflow') | sayHello | view
}
```

### 실행

```bash
nextflow run hello.nf
```

### 예상 출력

```
N E X T F L O W  ~  version 23.04.0
Launching `hello.nf` [peaceful_pasteur] DSL2 - revision: a9012339ce

executor >  local (3)
[d7/c8a4e5] process > sayHello (3) [100%] 3 of 3 ✓

Hello World!
Hello Korea!
Hello Nextflow!
```

## 기본 개념

### 프로세스 (Process)
- 실행 가능한 작업 단위
- 입력, 출력, 스크립트로 구성

### 채널 (Channel)
- 데이터 흐름을 관리
- 프로세스 간 데이터 전달

### 워크플로우 (Workflow)
- 프로세스들의 실행 순서 정의
- 데이터 흐름 제어

## 다음 단계

- [기본 개념](basic-concepts.html) 학습
- [데이터 처리](data-processing.html) 방법
- [설정 관리](configuration.html) 이해

## 문제 해결

### 일반적인 오류

1. **Java 버전 오류**
   ```bash
   java -version  # Java 8+ 확인
   ```

2. **권한 오류**
   ```bash
   chmod +x nextflow
   ```

3. **경로 문제**
   ```bash
   export PATH=$PATH:$PWD  # 현재 디렉토리를 PATH에 추가
   ```
