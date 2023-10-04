1. https://docs.flutter.dev/get-started/install 에서 컴퓨터 사양에 맞는 걸 다운로드 해준뒤, 압축 풀고 응용프로그램 파일에 옮겨 넣는다.
2. 메인 디렉토리로 돌아가서,  vi .zshrc로 파일을 열어준 다음, 새로운 라인을 추가해 export PATH="$PATH:[PATH_OF_FLUTTER_GIT_DIRECTORY]/bin"
를 추가해준다. 이때 [PATH_OF_FLUTTER_GIT_DIRECTORY]는 finder 하단 경로바에서 복사해서 쓴다.
	![[스크린샷 2023-10-04 오후 12.22.11.png]]
3. 저장을 하고 다시 나온다음, echo $PATH와 env 명령어로 경로가 제대로 설정되었는지 확인한다.![[스크린샷 2023-10-04 오후 12.27.12.png]]
4. soure .zshrc명령어로 재부팅 한 뒤에 which flutter를 한다.
	![[스크린샷 2023-10-04 오후 12.29.19.png]]
	바로 which flutter를 할 경우, 다음과 같이 명령어를 찾지 못한다. 
	![[스크린샷 2023-10-04 오후 12.27.41.png]]
5. flutter doctor 명령어 이후에 나오는 체크리스트를 해결한다. ![[스크린샷 2023-10-04 오후 12.31.49.png]]
	안드로이드와 Xcode에서 이슈가 생겼다.
	안드로이드)
	1. Android Studio > Check for Updeates... -> 새로운 버전이 있길래 새로 깔아줌.
	2. **Run `path/to/sdkmanager --install "cmdline-tools;latest"`** 이 명령어를 사용하거나, Tools > SDK 