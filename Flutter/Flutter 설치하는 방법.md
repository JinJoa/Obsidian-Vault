1. https://docs.flutter.dev/get-started/install 에서 컴퓨터 사양에 맞는 걸 다운로드 해준뒤, 압축 풀고 응용프로그램 파일에 옮겨 넣는다.
2. 메인 디렉토리로 돌아가서,  vi .zshrc로 파일을 열어준 다음, 새로운 라인을 추가해 export PATH="$PATH:[PATH_OF_FLUTTER_GIT_DIRECTORY]/bin"
를 추가해준다. 이때 [PATH_OF_FLUTTER_GIT_DIRECTORY]는 finder 하단 경로바에서 복사해서 쓴다.
	![[스크린샷 2023-10-04 오후 12.22.11.png]]
3. 저장을 하고 다시 나온다음, echo $PATH와 env 명령어로 경로가 제대로 설정되었는지 확인한다.