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
	나의 경우 안드로이드와 Xcode에서 이슈가 생겼다. 
	안드로이드)
	 **✗** **cmdline-tools component is missing**
	1. Android Studio > Check for Updeates... -> 새로운 버전이 있길래 새로 깔아줌.
	2. **Run `path/to/sdkmanager --install "cmdline-tools;latest"`** 이 명령어를 사용하거나, Tools > SDK Manager > SDK Tools에서 언급된 툴을 체크 후 OK를 누르면 된다. ![[스크린샷 2023-10-04 오후 12.39.24.png]]
	 **✗** **Android license status unknown.**
	 1.  **Run `flutter doctor --android-licenses` to accept the SDK licenses.** 실행하면 여러줄의 라이센스 조항이 나오는데 전부 'y'를 치면 된다.
	 Xcode)
	  1. 업데이트 확인후
	  2.         **sudo xcode-select --switch/Applications/Xcode.app/Contents/Developer**
	  3.      **sudo xcodebuild -runFirstLaunch**
	  두 명령어를 순차적으로 쳐준다.
이제 다시 flutter doctor 명령어를 치면 이슈가 없다고 나온다.


6. 새로운 flutter파일을 만들고 싶은 디렉토리로 이동한뒤, 다음 명령어들을 치면
	flutter create hello_flutter
	cd hello_flutter
	flutter run

   ![[스크린샷 2023-10-04 오후 12.46.26.png]] 이렇게 뜬다. 이중 1 또는 2를 누르면 flutter앱의 초기 화면이 뜬다.
   맥으로 열때, ![[스크린샷 2023-10-04 오후 12.49.47.png]]
   크롬으로 열때,![[스크린샷 2023-10-04 오후 12.52.53.png]]