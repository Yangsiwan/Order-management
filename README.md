주문관리 프로그램(Order-Management Program) - by juyoungIt
==========================================================

# make utility 를 이용한 컴파일 방법
* 일반모드 - make main
* 디버깅모드 = main_debug

# 프로그램 사용방법
프로그램 사용에 대한 도움말은 프로그램 실행 중 사용자에게
자세하게 소개됨. 프로그램에서 유도하는 방향으로 그대로
따라가면서 사용하기 원하는 옵션들을 사용하여 프로그램을
활용하면 되겠음

# 각 기능에 대한 설명
> ### 1. create - 주문정보 추가
>	> + 주문정보의 추가를 사용자가 직접 타이핑 하여 추가
>	> + 입력할 정보에 대한 내용은 시스템에서 자세히 안내
>	> + 주문상품, 수량, ID, 연락처, 주소, 결제수단 순차입력
>	> + 주문시간, 청구가격의 시스템 내에서 계산하여 반영

> ### 2. read - 주문정보 조회
>	> + 특정 key값(ID, 연락처) 를 이용하여 정보조회
>	> + 검색 시 모든 ID 또는 연락처를 정확히 입력해야 함
>	> + 검색 성공 시 주문정보를 화면에 출력

> ### 3. update - 저장한 주문내용 수정
>	> + 수정할 주문정보를 특정 key값으로 검색(ID)
>	> + 주문시간, 주문자 ID는 수정불가
>	> + 주문내용 변경 시 청구가격 내용 시스템에서 자동반영

> ### 4. delete - 주문내용 삭재
>	> + 특정 key값(ID)으로 삭제할 주문정보 탐색
>	> + 해당 key값을 가진 주문정보를 삭제
>	> + 삭제기능 내에서 조각모음 수행X
>	> + delete 후 조각모음 수행할 것을 권장

> ### 5. list - 모든 주문내용 출력
>	> + 저장된 모든 주문내용을 리스트 형식으로 출력
>	> + 총 저장된 주문내용 수 정보 출력

> ### 6. search - 저장된 주문내용 검색
> 	> + 저장된 주문정보를 특정 key값으로 탐색
>	> + 검색된 주문의 수와 해당정보를 리스트로 출력
>	> 1. 시간값(time)
>	> 	+ 주문접수 시간으로 검색
>	> 	+ 입력문자열을 포함하는 모든 시간값의 주문내용 출력
>	> 2. 제품명(product code)
>	>	+ 제품명을 코드화한 제품코드로 주문내용 검색
>	> 	+ 상품명에 대응하는 제품코드는 프로그램에서 제공
>	>	+ 특정 제품을 주문한 주문내용을 모두 검색
>	> 3. ID
>	>	+ 특정 내용을 포함하는 모든 ID 값을 가진 주문내용 검색
>	>	+ 완전 일치가 아닌 부분포함도 검색대상에 포함
>	> 4. 주소
>	>	+ 동일한 주소지를 가진 주문내용 검색
>	>	+ 완전일치만 검색의 대상에 포함
>	> 5. 연락처
>	>	+ 특정내용을 포함하는 연락처를 가진 주문내용 검색
>	>	+ 완전 일치가 아닌 부분포함도 검색대상에 포함
>	> 6. 결제수단
>	>	+ 동일한 결제수단 코드를 가진 주문내용 검색
>	>	+ 결제수단명을 코드화한 코드를 key 값으로 검색
>	>	+ 결제수단에 대응하는 코드는 프로그램에서 제공
>	>	+ 특정 결제수단으로 결제한 모든 주문내용 검색

> ### 7. show margin - 주문내역 출력
>	> + 현재 저장되어 있는 주문내용을 인해 발생하는 수익정보 출력

> ### 8. show report - 주문정보 보고서 출력
>	> + 현재 저장되어 있는 주문데이터를 보고서화 하여 출력
>	> + 총 주문내용 리스트, 상품별, 결제수단별 수익정보 포함

> ### 9. load file - 주문정보 로드(파일)
>	> + 파일로부터 주문내용을 로딩
>	> + 로드 전 기존의 내용을 유지하며 로드, 초기화 후 로드 모두지원

> ### 10. save file - 주문내역을 파일에 저장
>	> + 현재 저장된 모든 주문 데이터를 파일에 저장(백업)

> ### 11. save report - 보고서를 파일에 저장
>	> + 현재 저장된 모든 주문에 대한 보고서 내용을 별도 파일에 저장

> ### 12. gather piece - 조각모음
>	> + 삭제로 인해 발생하는 빈공간을 없애주는 역할
>	> + delete 수행 후 반드시 수행할 것을 권장
>	> + 조각모음 미수행 상태에서 다른 작업 수행 시 오류발생 가능성 있음

> ### 13. sort - 정렬
>	> + 특정 key 값(time, ID)으로 저장되어 있는 주문정보를 재정렬
>	> + 각각의 key 값들에 대한 오름/내림차순 정렬 지원
