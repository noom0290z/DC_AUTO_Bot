# DC_AUTO_Bot
디시인사이드 자동글쓰기 매크로(파이썬 GUI, 배포용exe 파일 포함)

<h2> * dist 폴더안에 응용프로그램(dc_auto.exe)</h2>

Selenium이란

웹테스트 자동화 도구로 많이 사용되고 있으며
 JS로 렌더링이 완료된 후의 결과물에 접근할 수 있다.
 즉, 실제로 브라우저를 조작할 수 있게끔 해주는 도구이다.


#selenium 설치
$ sudo pip install selenium

#config파일 사용을 위한 configparser 설치
$ sudo pip install configparser

selenium으로 이용할 브라우저로는 크롬을 선택했다. 
selenium으로 크롬을 조작하려면 크롬 드라이버가 필요하다.

https://sites.google.com/a/chromium.org/chromedriver/downloads

위 주소에서 다운로드 받아 파이썬 코드 파일과 같은 경로에 위치시켜 주자.

----------------------

 파이참으로 제작시 파이참안에서 라이브러리를 검색 후 다운로드받고 실행하면된다.
 
 이미지나,크롬드라이버는 "프로젝트폴더/venv/Include" 안에 넣고 경로를 설정해주면된다.

 * 실행파일 제작시(배포목적 .exe파일)

 pyinstaller 을 이용하여 배포파일을 만들었다.

 selenium,urllib3 같은 라이브러리는 따로 복사해서 "프로젝트폴더/venv/Lib/site-packages"에

 넣고난 뒤 pyinstaller를 돌려야 정상적으로 실행이된다.  
 
 ex) pyinstaller.exe --onefile --windowed --icon=venv\Include\logo.ico --clean dc_auto.py
  
 ondefile, windowed 등의 옵션은 직접찾아보기바란다.

-------------------------------------------------------------------------------

 실행파일은 프로젝트폴더안의 dist폴더 안에 생겨 그 안에 파일을 배포하면된다.
 (이미지 나 드라이버는 경로폴더(venv/include)를 만들어서 따로넣어주었다.)
 
 ![excute](https://user-images.githubusercontent.com/26120409/47325510-15e0d380-d69f-11e8-9427-97413c429eb2.png)
 ![auto](https://user-images.githubusercontent.com/26120409/47321122-b084e680-d68e-11e8-9dc6-c184cb529f0d.png)

 -----------------------------------------------------------------------------

파이참과 anaconda설치후 
GUI는 Qt Designer 이용하여 제작하였고 ui파일을 파이썬코드로 변환한뒤 함수를 만들어 버튼에 이벤트를 연결해주었다. 
(https://wikidocs.net/5226 참고)

* PyQt는 이름에서 알 수 있듯이 Qt라는 GUI 프레임워크의 파이썬 바인딩입니다.
현재 공식적으로 지원하는 Qt 메이저 버전은 Qt4와 Qt5입니다. 그래서 Qt의 파이썬 바인딩인 PyQt도 PyQt4와 PyQt5로 두 가지 버전이 제공됩니다. 
아나콘다 배포판에서 공식적으로 지원하는 PyQt5를 사용합니다.
