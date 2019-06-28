Learning Spring Framework
-------------------------

##Requirement
* Ant

##문서 생성
* `spring-framework-reference-kr`폴더에서 `ant`명령어를 실행합니다.
* 빌드하는데 7분정도 걸림
* 루트에 `ivy-cache`와 `integration-repo`폴더 생성됨
* `integration-repo/org.springframework/spring-framework-reference/3.2.0.BUILD-20120114131116`폴더 안에 PDF와 HTML 문서 생성됨
* (현재 PDF변환시 한글이 제대로 변환되지 않습니다. )

##PDF변환시 한글 변환문제 해결방법
* 문서 생성을 1회 수행합니다.
* `integration-repo`폴더를 삭제합니다.
* `config`폴더의 `build-docbook.xml`을 `spring-build/lib/docbook/build-docbook.xml`에 덮어씁니다.
* `config`폴더의 `pdf.xsl`를 `spring-build/lib/docbook/src/styles/pdf.xsl`에 덮어씁니다.
* 문서 생성을 다시 수행합니다.
* (현재 적용되어있는 글꼴은 `나눔고딕 Regular`입니다.)

##PDF에 사용되는 글꼴변경방법
* `config/font`폴더의 `font.tff`와 `font.xml`파일을 삭제합니다.
* 변경하려는 글꼴(tff파일)을 `config/font`폴더에 복사합니다.
* tff파일의 이름을 `font.tff`로 수정합니다.
* `buildFontXml.bat`파일을 실행시킵니다.