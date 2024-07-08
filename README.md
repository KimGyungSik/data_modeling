# :books: 핵심 데이터 모델링 (Book) 정리
### 도서 링크 : https://www.yes24.com/Product/Goods/89872186


---

## :scroll: 목차


* ### 1. 데이터 모델링 이론  
* ### 2. 개념 모델링  
* ### 3. 논리 모델링  
* ### 4. 물리 모델링

---


## :dart: 1. 데이터 모델링 이론
* ## :balloon: 데이터 모델링 이란?
  * ### 모델링 : 실제를 본떠서 만든 것
  * ### 데이터 모델링 : 실제 업무에 맞게 데이터의 특성과 구조를 만드는 것
  * ### ER 모델 : 개체(Entity)와 개체간의 관계(Realationship)로 표현하는 모델
  * ### ERD : ER 모델을 그림(Diagram)으로 표현한 것
  * ### 데이터 구조를 자신이 읽고 쓰기 편하게 ...
  * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/593d8f9f-8d55-4ee3-ac89-85dedad52b1b" width="500">
  * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/98f491dd-50a5-42d6-81a8-40a8fc366089" width="500">

* ## :balloon: ER 모델 구성 요소 (엔티티, 관계, 속성, 식별자)
  * ## :star: 엔티티 (class,table)
    * ### 클래스 정의와 유사 
    * ### 현실 세계에 실제로 존재하는 실체
    * ### 업무를 구현하는 데 필요하고 관리해야 하는 주체,대상, 행위 등의 모든 집합적인 것
    * ### 인스턴스(iv묶음)의 집합체
    * ### 슈퍼타입/서브타입 엔티티는 일반화/특수화 과정을 통해 도출됨
      * #### 일반화 (상향식) : 여러가지 객체로 부터 공통된 점을 추출하여 새로운 객체를 만듬 (추상화)
      * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/663cef99-0010-4296-98ac-5071955a8863" width="500">
      * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/7401bb74-b85d-404f-ab81-5eceacc72db4" width="500">

    * ### 엔티티 생성 관점 3가지
      * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/225b8d3c-55a9-487d-b094-9df20e5bf25a" width="500">

  * ## :star: 관계 (선긋기) 
    * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/8872d5c9-18a8-47c6-b8c2-9c6faf2d6ca3" width="500">
    * ### 관계수 : 두 엔티티 간의 대응되는 행의 개수
      * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/0d82fc80-63ee-43db-afd5-7b5c0e685533" width="500">
    * ### 선택성 : 관련 행(row)의 존재가 필수(|) 또는 선택(O) 여부
      * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/9f6bb51d-c934-450a-b39a-fdd830d5e8a2" width="500">
    * ### 식별자 상속 
      * #### 한 엔티티의 식별자(PK)가 다른 엔티티의 PK가 되는 경우 -> `식별 관계`
      * #### 한 엔티티의 식별자(PK)가 다른 엔티티의 PK가 되는 않는 경우 -> `비식별 관계(대부분)`
      * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/c0dad9c5-a50b-483a-878f-ee70659b7c59" width="500">
    * ### 관계 유형 (기본 관계, 재귀적 관계, 병렬 관계, 슈퍼타입/서브타입 관계)
      * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/cfbccb3c-8c0f-4bb0-b415-298a6824e200" width="500">
    * ### 교차 테이블을 사용하는 이유 2가지
      * #### 병렬관계 해소
        * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/ddafafe3-a219-40e8-ab43-1b4bf9af3a89" width="500">
      * #### M:N 관계 해소
  * ## :star: 속성 (iv)
    * ### 속성명(iv이름)
    * ### 식별자여부(pk인지 아닌지)
    * ### 옵셔널리티(NOT NULL인지 아닌지)
    * ### 도메인(컬럼이 가질 수 있는 범위)
    
  * ### 단순 속성(기본형)과 복합 속성(참조형)
    * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/105c596c-0862-448a-beaf-5b045d968901" width="500">
  * ### 저장 속성(원래 존재하는 속성)과 파생 속성(계산된 속성)
    * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/fc09e881-4c44-4cca-8e91-a2960013fb94" width="500">
  * ### 단일 값 속성(1개)과 다중 값 속성(n개)
    * #### 다중 값 속성은 모델링 과정에서 정규화를 통해 별도 엔티티로 분리해야함 
    * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/06e3987f-8fbe-4fcb-b54f-e097c7f622ae" width="500">

  * ## :star: 식별자 (유일성, 최소성, 불변성, 존재성)
    * ### 식별자란? 엔티티에서 인스턴스를 개별적으로 식별할 수 있는 속성
    * ### 유일성 : 엔티티의 모든 인스턴스를 유일하게 식별할 수 있어야함
    * ### 최소성 : 유일성을 만족하는 최소 속성들로 구성
    * ### 불변성 : 변하면 안됨 why? 다른 테이블의 FK로서 사용될 수 있기 떄문
    * ### 존재성 : 값이 존재해야함
    * ### 식별자 유형
      * #### 본질 식별자 / 인조 식별자
      * #### 주 식별자 / 보조 식별자
    * ### 식별자를 최소 속성으로 구성하지 않은 경우
      * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/ecf24c03-fa22-48f8-bf2d-db9af59f4c4b" width="500">
    * ### 식별자 속성의 값이 변하는 경우
      * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/81027d2f-6f1c-4be6-b258-284dd14e4e31" width="500">
    * ### 본질 식별자(업무에서 자연적으로 가지는 특성) / 인조 식별자(시스템에서 필요에 의해 추가한 속성)
      * <img src="https://github.com/KimGyungSik/data_modeling/assets/139200972/44204c66-f075-447c-b553-3e70550e0d6b" width="500">



* ## :balloon: 관계형 데이터 모델 이론
  * ## :star: 관계형 데이터 모델(릴레이션)
    * 사진
  * ## :star: 관계형 모델의 키
    * 사진
    * ### 슈퍼키 : 튜플을 고유하게 식별 할 수 있는 속성 집합
    * ### 후보키 : 튜플을 고유하게 식별 할 수 있는 최소한의 속성 집합
    * ### 기본키 : PK(NN + UQ), 유일성 + 최소성
    * ### 대체키 : 기본키가 아닌 후보키
    * ### 외래키 : 어떤 릴레이션의 어트리뷰트 값이 다른 릴레이션에 속한 어트리뷰트의 기본키를 참조하는 경우
  * ## :star: 제약 조건
    * ### 키 제약조건 : UNIQUE
    * ### 실체 무결성 : NOT NULL
    * ### 영역 무결성 : 도메인에 속한 값
    * ### 참조 무결성 : 참조 FK
  * ## :star: 함수 종속
    * 사진
  * ## :star: 정규화
    * ### 정규화 : 중복 제거하기 위해 테이블을 쪼개는 것
      * #### 데이터를 입력, 수정, 삭제할 떄 발생하는 이상 현상을 최소화하기 위해 좀 더 작은 단위의 테이블로 설계
    * #### 1. 이상현상 최소화 
    * #### 2. 유연성 증가 
    * #### 3. 재활용 높음
    * #### 4. 데이터 품질 문제 감소, 저장공간 최소화
    * #### 5. 데이터 입력, 수정, 삭제시 작업을 최소화
    * #### 정규화를 너무 많이 할 경우 다시 역정규화 할 수 있음
  * ### 제 1 정규화 : 모든 열의 값은 원자값을 가져야함, 관계형 테이블은 중복되는 행이 없어야함
    * 사진
  * ### 제 2 정규화 : 부분 종속 해소, 후보키에 종속적이지 않거나 후보키 일부 어트리뷰트에 종속적인 어트리뷰트는 별도 릴레이션으로 분리해야함
    * 사진
  * ### 제 3 정규화 : 이행적 종속 해소, 키가 아닌 어떤 어트리뷰트가 다른 어트리뷰트에 종속된 경우 별도 릴레이션으로 분리
    * 사진

---

## :dart: 2. 개념 모델링 
* ## :balloon: 데이터 모델링 접근 방법 : 데이터 모델링 작업 흐름