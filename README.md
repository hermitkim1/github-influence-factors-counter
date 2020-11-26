# GitHub influence factors counter

> 현재, **Organization의 영향요인 측정이 가능**합니다. User의 영향요인 측정은 개발 예정입니다.

GitHub influence factors counter를 활용하면 Repositories, Members, Contributors, Stars, Forks, Watches, Commits와 같은 영향요인의 수를 보다 편하게 확인할 수 있습니다. :thumbsup:   
Open Source Software (OSS) 관련 프로젝트에서 편리하게 활용하시기 바랍니다. :smile:   

**OSS 연구/개발 프로젝트에서 Commit 하나 하나의 가치는 중요하지만 Commit 마다 정성적인 가치는 다릅니다.**   
**만약 본 프로그램을 평가에 활용하신다면, <ins>정성적인 가치 평가를 꼭 함께 수행하시기를 기원합니다.</ins>**  :pray:

## Prerequities
- python 3.8 에서 테스트하였습니다.
- clone후 import되어 있는 packages를 별도 설치 바랍니다.

## 사용방법
### 1. 본 레포지토리를 `clone`합니다.
### 2. `auth.json` 생성
GitHub API 사용에 Rating limit이 있기 때문에 설정 하는 것이 좋습니다.   
아래 양식을 바탕으로 `auth.json`을 `main.py`가 있는 위치에 생성합니다.   
```json
{
  "username": "xxxxxxx",
  "personal-access-token": "xxxxxxx"
}
```

### 3. `orgs.json`에 자신의 레포지토리를 기입합니다.
"Name"을 아래와 같이 기입 합니다.
```json
[
  {
    "Name": "cloud-barista"
  }
]
```

### 4. 실행후 결과 생성
실행 후 잠시 기다리면 아래 두가지 결과를 얻을 수 있습니다. (Excel로 열어서 작업하시면 편하실거에요.)

결과1:
`orgs-result.csv` 는 Organization name, Repositories, Members를 포함합니다. 

결과2:
`repos-result.csv`는 Repository, Stars, Forks, Watches, Commits(year)을 포함합니다. 

