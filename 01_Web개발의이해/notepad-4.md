# 4. 개발환경 설정 - BE

===================================

# 4.1 JDK 다운받기 및 설치하기

JAVA언어를 작성된 프로그램을 실행하기 위해선 JRE(Java SE Runtime Environment)가 필요합니다.
JAVA언어를 사용하는 개발자가 아니라 JAVA언어로 만들어진 프로그램을 실행하는 사용자라면 JRE만 컴퓨터에 설치하면 됩니다.
보통 사용자 입장에서 JAVA를 설치한다는 것은 JRE를 설치하는 것을 말합니다.
JAVA언어를 사용하는 개발자는 JAVA언어로 작성된 소스(Source)를 컴파일하고 관리할 필요가 있습니다.
이때 사용되는 도구를 JDK(Java SE Development Kit)라고 말합니다.
JDK안에는 JRE도 포함되어 있습니다.
컴파일한 결과를 실행하기 위해서는 JRE가 필요하기 때문입니다.

## JDK 다운로드 및 설치

JDK는 Oracle사이트에서 무료로 다운로드하여 설치할 수 있습니다.

## 1. window용 설치

브라우저로 다음의 URL을 입력하여 이동합니다.
http://www.oracle.com/technetwork/java/index.html


"Java SE"를 클릭합니다.

JDK 최신버전은 9입니다.
그런데, 현재 가장 많이 사용되는 버전은 8입니다.
본 과정에서는 JDK8을 사용하도록 하겠습니다.
위의 그림과 같이 스크롤을 내려 "Java SE OOO/OOOO" 부분에 있는 "JDK Download" 버튼을 클릭합니다.

JDK를 다운로드 받으려면 먼저 라이센스(License)에 동의해야합니다.
"Accept License Agreement" 앞에 있는 레디오 버튼을 클릭합니다.

본인이 사용하는 운영체제에 맞는 JDK를 다운로드 해야합니다.
맥운영체제를 사용한다면 MacOS에 해당하는 "jdk-8u151-macosx-x64.dmg"를 클릭하고, MS윈도우 32비트 운영체제를 사용한다면 "jdk-8u151-windows-i586.exe"를 클릭하여 다운로드 받습니다.
참고로 MS윈도우 64비트 운영체제의 경우에는 "jdk-8u151-windows-x64.exe"를 다운로드 받습니다.

다운받은 MS Widnows 64bit용 JDK "jdk-8u151-windows-x64.exe"파일을 더블클릭하여 실행하면 위의 그림과 같은 환영 메시지가 보여집니다.
Next버튼을 클릭합니다.

JDK가 설치될 경로(Path)를 지정합니다.
JDK가 설치되는 경로를 JAVA_HOME경로라고도 말합니다.
해당 경로를 꼭 기억해주세요.
환경설정을 할 때 알아야 합니다.
Next버튼을 클릭합니다.

JDK설치가 끝나면 JRE가 설치될 경로를 설정하게 됩니다.
Next버튼을 클릭합니다.

설치가 진행되고 있습니다.
잠시만 기다려 주세요.

설치가 완료되었습니다.

## 2. mac os용 설치

브라우저에서 다음의 URL로 이동합니다.
http://www.oracle.com/technetwork/java/javase/downloads/index.html


JDK Download 링크를 클릭합니다.

jdk-8u121-macosx-x64.dmg 를 다운로드 받습니다.

다운로드 받은 파일을 더블 클릭하면 위와 같은 창이 열립니다.

JDK설치 마법사가 실행됩니다.

맥의 관리자 ID와 암호를 입력하라는 창이 보여집니다.
본인의 맥 아이디와 암호를 입력하세요.

설치가 완료되었습니다.

# 4.2 환경설정하기

JDK를 설치한 이후에는 JDK를 콘솔(console) 환경에서 잘 실행될 수 있도록 시스템 환경 설정을 해야 합니다.
시스템 환경 설정을 하는 방법은 운영체제에 따라서 다릅니다. 

## JAVA 환경설정

JDK설치가 완료되었다면, JDK에 대한 시스템 환경설정을 해야 합니다.
시스템 환경설정을 하는 방법은 운영체제마다 다릅니다.
운영체제 마다 시스템 환경설정하는 방법은 다르지만, 설정해야 할 환경변수의 이름은 같습니다.
설정해야 할 환경변수는 다음과 같은 3가지입니다.

* JAVA_HOME : JAVA가 설치된 경로를 지정
* CLASSPATH : JAVA 클래스가 있는 경로들을 지정
* PATH : JAVA 실행파일이 있는 경로를 추가

JAVA_HOME, CLASSPATH는 시스템 환경변수에 새롭게 추가될 환경 변수이고, PATH는 기존에 존재하는 환경 변수입니다.

## 1. MS Windows 10에서의 환경설정

MS Windows 10에서 JDK 관련된 환경변수를 설정해 보도록 하겠습니다.

찾기 버튼을 누른 다음에 "시스템 환" 까지 입력합니다.
그러면 검색 결과에 "시스템 환경 변수 편집"이라는 결과가 보여질 것입니다.
"시스템 환경 변수 편집"을 선택합니다.

창이 열리면 "환경변수" 버튼을 클릭합니다.

시스템 변수 영역의 "새로 만들기"버튼을 클릭합니다.

변수이름엔 "JAVA_HOME"을 변수 값엔 JDK가 설치된 경로를 입력합니다.
(파일 탐색기에서 해당 경로로 이동한 후 복사하여 붙이기를 추천합니다.)

"JAVA_HOME" 환경변수가 시스템 변수 영역에 추가된 것을 확인할 수 있습니다.

같은 방법으로 "CLASSPATH" 환경변수를 추가합니다.
값은 ".;%JAVA_HOME%\lib\tools.jar" 로 입력합니다.
"%JAVA_HOME%"은 앞에서 설정한 JAVA_HOME 환경변수의 값으로 치환하라는 의미입니다.

시스템 변수 영역에서 PATH를 찾아서 선택한 후 "편집" 버튼을 클릭한 후 위의 그림과 같은 창이 열리면 우측의 "새로 만들기" 버튼을 클릭한 후 "%JAVA_HOME%\bin"을 입력합니다.

"윈도키 + R"을 입력하여 실행창이 열리도록 한 후, "cmd"라고 입력하고 엔터를 입력합니다.
이 때 cmd 콘솔(console)창이 열리게 됩니다.
해당 콘솔창에서 다음과 같이 내용을 입력합니다.

```
java -version
javac -version
```

java 명령은 JAVA로 작성된 프로그램을 실행할 때 사용하는 명령이고, javac 명령은 java로 작성된 프로그램을 컴파일할 때 사용하는 명령입니다.
실행 결과가 보인다면 설치가 잘 된 것입니다.
만약 java는 잘 실행되는데 javac가 제대로 실행되지 않는다면, 시스템 환경 변수 설정이 잘못 설정되었거나 JDK가 아닌 JRE만 설치되었을 때입니다.
환경변수에 오타가 있는지 확인하고 알맞게 수정하여 주세요.
환경변수가 수정되었다면 cmd 콘솔창을 닫고 다시 cmd 콘솔창을 열어서 명령을 실행해야 합니다.

## 2. Mac OS에서의 환경설정

설치가 완료된 이후에, 터미널을 연 후 아래와 같이 명령을 내립니다.

```
cd /Library/Java/JavaVirtualMachines
ls -la
```

그러면 아래와 같이 보일 것입니다.
위에서 사용한 명령은 맥 터미널 명령입니다. ( 리눅스도 같은 명령을 사용할 수 있습니다. )
필자의 경우 2가지 버전의 jdk가 설치되어 있기 때문에 jdk1.8.0_121.jdk 와 jdk1.8.0_91.jdk 2가지가 보입니다.
처음 설치했다면 경로가 하나만 보일 것입니다.

```
cd /Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home  
```

위와 같은 명령으로 경로를 이동해보세요.
중간에 있는 jdk1.8.0_121.jdk는 본인이 설치한 jdk와 같은 경로여야 합니다.
해당 경로를 JAVA_HOME 경로라고 합니다.
해당 경로에서 ls -la 명령을 내려보면 윈도우에서 설치한 JDK와 같은 내용이 보이는 것을 알 수 있을 것입니다.
이제 맥에서 JDK를 사용하기 위해서 환경설정을 해야 합니다.
먼저 다음과 같은 명령을 실행합니다.

```
sudo su -
```

위의 명령은 터미널에서 관리자로 권한을 바꾸겠다는 것을 의미합니다.

```
vi /etc/paths
```

위의 명령은 vi라는 에디터로 /etc/paths 라는 파일을 편집하겠다는 것을 의미합니다.
vi 에디터는 처음 사용하면 굉장히 어렵습니다.
인터넷에서 vi 에디터에 대한 사용법을 미리 공부한 후 사용해주세요.
에디터로 /etc/paths라는 파일을 열었다면 맨 아랫줄에 다음의 경로를 추가합니다.

```
/Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home/bin
```

그리고 파일을 저장합니다.
이렇게 저장을 한 후, 다시 터미널을 열면 어디서든 java명령을 실행할 수 있습니다.
이번엔 다음과 같은 명령으로 JAVA_HOME 과 CLASSPATH 환경변수를 지정합니다.

```
vi /etc/profile
```

위의 명령을 실행한 후 맨 아랫줄에 다음의 내용을 추가합니다.

```
export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home
export CLASSPATH=.:$JAVA_HOME/lib/tools.jar
```

CLASSPATH=다음에 있는 문자열은 점(.) 과 콜론(:)입니다.
점은 현재 경로를 말하고 콜론은 구분자입니다.
CLASSPATH로 현재 경로와 $JAVA_HOME/lib/tools.jar를 지정하라는 것을 의미합니다.
자 위와 같이 설정하였다면 터미널을 종료 후 다시 실행합니다.
그리고 아래와 같이 명령을 내려봅시다.

```
java -version
```

결과가 출력된다면 설치가 잘 된 것입니다.


## 간단한 JAVA 프로그램 컴파일 및 실행

메모장을 열어 "Hello.java"라는 파일로 다음의 내용을 저장합니다.

```
public class Hello{
     public static void main(String args[]){
       System.out.println("hello world");
     }
}
```

어떤 디렉토리에 저장해도 상관은 없습니다.
저는 c:\temp 폴더에 저장하였습니다.
cmd 콘솔창을 연 후 다음과 같이 입력합니다.
c:\temp 가 아닌 다른 디렉토리에 저장하였을 경우에는 본인이 저장한 디렉토리를 입력하면 됩니다. 

```
cd c:\temp
```
```
javac Hello.java
```

위의 명령은 Hello.java소스파일을 컴파일하라는 명령입니다.

컴파일 되면 Hello.class파일이 생성됩니다.

Hello.class파일이 생성되었다면, 다음의 명령으로 실행합니다.

```
java Hello
```

"hello world"가 잘 출력되었다면, JDK설치부터 환경변수설정까지 잘 되었다는 것을 알 수 있습니다.


4.3 이클립스 다운받기 및 설치하고 인코딩 설정하기

## 이클립스란?

IBM에서 웹 스피어 스튜디오 애플리케이션 디벨로퍼(WebSpheare Studio Application Developer)란 이름으로 JAVA언어를 이용하여 개발되었던 것인데, 핵심 부분을 오픈 소스로 공개하여 지금의 이클립스로 발전하게 되었습니다.
이클립스는 윈도우, 맥, 리눅스 등 다양한 운영체제에서 동작하며, JAVA를 비롯한 다양한 프로그래밍 언어를 개발할 수 있는 통합 개발 환경( Integrated Development Environment, IDE)이라고 말할 수 있습니다.
통합 개발 환경이란 코딩, 디버그, 컴파일, 배포 등 프로그램 개발에 관련된 모든 작업을 하나의 프로그램 안에서 처리할 수 있도록 환경을 제공하는 소프트웨어라고 생각하면 됩니다.
이클립스는 플러그인 구조로 쉽게 기능을 추가할 수 있는 구조로 되어 있습니다.
이런 구조 때문에 이클립스 기반으로 만들어진 다양한 도구들이 존재합니다.
또한 이클립스는 윈도우, 맥, 리눅스 운영체제를 지원하기 때문에 대부분의 환경에서 사용할 수 있다는 장점이 있습니다.
2001년 세상에 첫선을 보인 이래로 지속적으로 발전하여 최고의 개발 도구 중의 하나로 사랑받고 있습니다.

## 이클립스 다운로드및 설치

웹 브라우저로 이클립스 사이트에 접속합니다.
하단에 있는 Packages 링크를 클릭합니다.

이클립스 사이트
이클립스를 이용하여 자바 웹 어플리케이션을 개발할 때 사용하려면 "Eclipse IDE for Java EE Developers"를 다운로드 받아야 합니다.
본인의 운영체제에 맞는 버전을 다운로드 받습니다.
목록을 살펴보면 알겠지만, 다양한 이클립스 버전이 있는 것을 알 수 있습니다.
Windows사용자는 자동으로 윈도우와 관련된 다운로드 링크가 보입니다.
저는 64bit를 다운로드 받도록 하겠습니다.

다운로드 링크를 클릭하여 다운로드 합니다.
약 340메가 정도의 파일이 다운로드 됩니다.

이클립스는 압축만 해제하면 간단히 설치할 수 있습니다.
삭제할 때도 압축을 해제한 폴더만 삭제하면 됩니다.
다운로드 받은 파일인 "eclipse-jee-oxygen-2-win32-x86_64.zip"의 압축을 해제합니다.
압축을 해제하면 eclipse란 폴더가 있고, 그 안에는 아래 그림과 같은 파일들이 있는 것을 확인할 수 있습니다.

이클립스 실행과 이클립스의 구성요소
파일 중에서 eclipse.exe파일을 더블클릭하여 실행합니다.
실행하면 다음과 같이 workspace경로를 물어보는 창이 열립니다.
workspace란 이클립스로 관리하는 프로젝트가 저장되는 경로를 의미합니다.
앞으로 이클립스로 개발하는 모든 내용이 저장되는 폴더라고 생각하면 됩니다.

폴더를 지정한 후 "Lanuch"버튼을 클릭하면 버전에 따라서 모양이 약간 다르지만, 로그화면이 보여지면서 실행되게 됩니다.

처음 실행되면 이클립스 "Welcome"탭이 보여집니다.
각 링크를 클릭하면서 내용을 살펴보세요.
이클립스와 관련된 다양한 내용에 대하여 살펴볼 수 있을 것입니다.

내용을 살펴보았다면, "Welcome" 탭의 X버튼을 클릭하여 해당 창을 닫습니다.
창을 닫으면 아래의 그림과 같은 화면이 보여집니다.

이클립스를 다운로드 받을 때 보면, 다양한 종류의 이클립스가 있던 것을 볼 수 있었습니다.
이클립스는 플러그인(Plugin)이란 구조로 만들어져 있습니다.
이클립스에 다양한 플러그인을 설치함으로써 다양한 방식으로 사용할 수 있습니다.
이클립스에 아무 플러그인도 설치하지 않았다면, 빈 윈도우 화면이 보여질 것입니다.
"Eclipse IDE for Java EE Developers" 는 자바와 자바 웹 개발을 위한 플러그인들이 설치된 버전이라고 생각하면 됩니다.
(1)번 영역은 퍼스팩티브(Perspective)라고 합니다.
퍼스팩티브는 여러개의 뷰(View)와 에디터 영역, 메뉴 등으로 구성되어 있습니다.
우리는 자바 개발과 자바웹 개발을 위한 퍼스팩티브를 사용할 것입니다.
(2)번 영역은 뷰(View)라고 합니다.
이클립스는 다양한 뷰를 제공해줍니다.
파일 탐색기와 유사항 뷰부터 시작해서 서버실행화면을 보여주는 뷰 등 다양한 뷰를 제공합니다.
(3)번 영역은 에디터(Editor) 영역이라고 합니다.
보통 에디터가 위치하기 때문입니다. 에디터 영역에서 앞으로 JAVA코드를 작성할 것입니다.

## 이클립스 설치 후 인코딩 설정하기

프로젝트 내에서 JAVA, HTML, xml등의 다양한 종류의 파일이 사용되는데 파일마다 인코딩하는 방법이 다르면 글자가 깨지는 현상이 발생합니다.
이런 문제가 발생하지 않도록 인코딩을 설정해 두는 것이 좋습니다.
이 과정에서는 UTF-8로 설정하도록 하겠습니다.
아래와 같이 인코딩을 설정해 주세요.

Window -> Preferences 메뉴를 클릭합니다.

Preferences 다이얼로그가 열리면, General -> Workspace 메뉴를 활성화하고, 하단의 Text file encoding 메뉴에서 Other 라디오버튼을 클릭하고 UTF-8 로 선택하고 Apply 버튼을 클릭합니다.
이렇게 설정하면 주로 자바 파일들에 대한 기본 인코딩이 UTF-8 로 설정됩니다.

CSS Files
좌측 메뉴에서 Web을 활성화해주고 CSS Files 메뉴를 클릭하면 우측 메뉴가 바뀌는데 우측의 Encoding 항목에서 UTF-8을 선택하고 Apply 버튼을 눌러줍니다.
같은 방법으로 HTML Files, JSP Files 의 인코딩 설정도 바꿔줍니다.


# 4.4 HelloWorld 컴파일하고 실행하기

## Java Code Conventions (프로그래머들끼리의 약속) 

* 클래스명 : 첫글자를 대문자로
* 프로젝트명, 패키지명 : 소문자

## 실습코드
```
package first;

public class Hello {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```

### 참고자료
구글 Java 코딩 컨벤션 - https://google.github.io/styleguide/javaguide.html

자바 코딩 규칙 (Java Code Conventions) - https://myeonguni.tistory.com/1596

Code Conventions for the Java Programming Language: Contents - https://www.oracle.com/java/technologies/javase/codeconventions-contents.html


# 4.5 Tomcat 다운받기 및 설치하기

## Apache Tomcat이란?

아파치 톰캣(Apache Tomcat)은 아파치 소프트웨어 재단(Apache Software Foundation, ASF)에서 개발한 세계에서 가장 많이 사용되는 WAS(Web Application Server)입니다.
컴퓨터에 운영체제를 설치해야만 컴퓨터를 사용할 수 있는 것처럼, 자바를 이용하여 작성된 웹 어플리케이션은 WAS가 있어야만 실행할 수 있습니다.
이때 가장 많이 사용되는 WAS가 아파치 톰캣이라고 말할 수 있습니다.
아파치 톰캣은 오픈소스 소프트웨어로써 누구나 무료로 사용할 수 있습니다.
참고로 Tomcat은 '수고양이'를 뜻합니다. 톰과 제리의 톰이 생각나기도 합니다.

## Apache Tomcat 다운로드 및 설치

아파치 톰캣은 http://tomcat.apache.org 에서 다운로드 받을 수 있습니다.
http://tomcat.apache.org 로 이동한 후 "Tomcat 8"을 선택합니다.
2017년 12월 기준 최신 버전은 "Tomcat 9"입니다만, 이번 수업에서는 "Tomcat 8"을 다운로드 하도록 하겠습니다.
Tomcat 8버전은 JDK 7이상에서 동작하며 Servlet Spec 3.1을 지원합니다.
Tomcat 9버전은 JDK 8이상에서 동작하며 Servlet Spec 4.0을 지원합니다.
좌측 "Download"메뉴 아래에 있는 "Tomcat 8"링크를 클릭합니다.

8.5.24 버전의 zip파일을 다운로드 합니다. (MAC OS 사용자는 tar.gz 파일을 다운로드 합니다.)
다운로드 받은 파일을 압축 해제합니다.

압축을 해제하면 다음과 같은 파일과 폴더들이 있는 것을 확인할 수 있습니다.

Apach Tomcat 실행
아파치 톰캣 설치 폴더 아래에 있는 bin폴더를 보면 확장자가 bat인 윈도우용 배치파일과 확장자가 sh인 쉘스크립트(shell script)파일이 있는 것을 확인할 수 있습니다.
쉘스크립트 파일은 linux나 맥 운영체제에서 실행 가능한 파일입니다.
윈도우 사용자라면 startup.bat파일을 더블 클릭하여 실행하고, 맥 운영체제나 linux를 사용하는 사용자는 startup.sh을 더블 클릭하여 실행합니다.


## MAC OS 사용자의 경우

1. 다운로드 받은  tar.gz  확장자의 톰캣파일의 압축을 해제합니다.
관리의 편의를 위해 압축해제 한 폴더를 ~/ 경로의 apps 폴더로 옮깁니다.

```
mkdir ~/apps
cd ~/apps
mv ~/Downloads/apache-tomcat-8.5.24 ~/apps/
```

2. 쉘확장자를 가진 파일의 실행권한을 줍니다.

```
chmod +x ./bin/*.sh
```

3. 제대로 실행 권한이 생성 되었는지 확인해 보기 위해 ls -al 로 해당 폴더의 파일 목록을 봅니다.
해당 파일명 앞에 -rwxr-xr-x@ 와 같이 권한 마지막 부분에 x가 보인다면 실행권한이 부여 된 것입니다.

```
ls -al

-rw-r-----@  1 username  staff   34894 Mar  5 22:11 bootstrap.jar
-rw-r-----@  1 username  staff    1664 Mar  5 22:13 catalina-tasks.xml
-rw-r-----@  1 username  staff   15815 Mar  5 22:11 catalina.bat
-rwxr-x--x@  1 username  staff   23387 Mar  5 22:11 catalina.sh
-rw-r-----@  1 username  staff  207125 Mar  5 22:11 commons-daemon-native.tar.gz
-rw-r-----@  1 username  staff   25145 Mar  5 22:11 commons-daemon.jar
-rw-r-----@  1 username  staff    2040 Mar  5 22:11 configtest.bat
-rwxr-x---@  1 username  staff    1922 Mar  5 22:11 configtest.sh
-rwxr-x---@  1 username  staff    8509 Mar  5 22:11 daemon.sh
-rw-r-----@  1 username  staff    2091 Mar  5 22:11 digest.bat
-rwxr-x---@  1 username  staff    1965 Mar  5 22:11 digest.sh
-rw-r-----@  1 username  staff    3574 Mar  5 22:11 setclasspath.bat
-rwxr-x---@  1 username  staff    3680 Mar  5 22:11 setclasspath.sh
-rw-r-----@  1 username  staff    2020 Mar  5 22:11 shutdown.bat
-rwxr-x---@  1 username  staff    1902 Mar  5 22:11 shutdown.sh
-rw-r-----@  1 username  staff    2022 Mar  5 22:11 startup.bat
-rwxr-x---@  1 username  staff    1904 Mar  5 22:11 startup.sh
-rw-r-----@  1 username  staff   49335 Mar  5 22:11 tomcat-juli.jar
-rw-r-----@  1 username  staff  405109 Mar  5 22:11 tomcat-native.tar.gz
-rw-r-----@  1 username  staff    4574 Mar  5 22:11 tool-wrapper.bat
-rwxr-x---@  1 username  staff    5483 Mar  5 22:11 tool-wrapper.sh
-rw-r-----@  1 username  staff    2026 Mar  5 22:11 version.bat
-rwxr-x---@  1 username  staff    1908 Mar  5 22:11 version.sh
```

4. 터미널에서 다음과 같이 명령어를 실행해 줍니다.

```
./bin/startup.sh 
```

5. 이 때 아래와 같은 오류가 나오면, 다음의 명령어 chmod +x bin/catalina.sh 를 실행해 줍니다.

```
Cannot find bin/catalina.sh
The file is absent or does not have execute permission
This file is needed to run this program
```

다음과 같이 해당 파일을 생성하고 실행권한도 생성해 줍니다.

```
chmod +x bin/catalina.sh
```

6. 그리고 다시 다음의 명령어로 톰캣을 실행해 줍니다.

```
./bin/startup.sh 
```

7. 톰캣이 시작되었다는 메시지는 출력되지만 8080포트로 접근이 되지 않을 때는 root 권한으로 서버를 시작해 줍니다.

```
sudo ./bin/startup.sh 
```

- 쉘 파일의 실행 권한을 주고 서버를 실행 했음에도 http://localhost:8080/ 로 접근이 되지 않을 때 sudo 명령어를 통해 서버를 시작해야 합니다.

콘솔창이 열리면서 다음과 같이 실행되는 것을 알 수 있습니다.
tomcat은 기본적으로 8080포트로 실행됩니다.
실행된 화면을 보면 "http-nio-8080"이라는 문자열을 볼 수 있는데 8080으로 실행되는 것을 표현하고 있는 것입니다.
tomcat설정파일을 수정함으로써 실행되는 포트를 바꿀 수 있습니다.
앞에서도 설명했지만, 컴퓨터를 구분하기 위해서 사용되는 것이 도메인이나 ip이고, 컴퓨터에 설치되어 있는 여러개의 소프트웨어 서버를 구분하기 위해 사용되는 값이 포트(port)라고 하였습니다.

웹 브라우저를 실행한 후 주소창에 http://localhost:8080 나 http://127.0.0.1:8080 으로 입력해 보도록 하겠습니다.
localhost는 현재 사용중인 컴퓨터를 나타내는 도메인(domain)주소이고 127.0.0.1은 현재 사용 중인 컴퓨터를 나타내는 ip주소입니다.
웹 브라우저로 현재 컴퓨터에서 8080포트로 동작하는 서버에 접속하라는 의미입니다.
Tomcat이 기본으로 제공하는 웹 사이트가 보여지는 것을 확인할 수 있습니다.

아파치 톰켓 설치 폴더 아래의 bin폴더에 있는 shutdown.bat파일이나 shutdown.sh파일을 더블클릭하여 실행하면 아파치 톰캣이 종료됩니다.
혹은, 실행 중인 창을 닫아도 아파치 톰캣은 종료됩니다.
아파치 톰켓이 종료 된 후 http://localhost:8080으로 다시 접속해보면, 아래의 그림과 같이 오류 화면이 보여지는 것을 확인할 수 있습니다.

이번 학습에서는 아파치 톰캣을 설치하고, 실행해 보았습니다.


# 4.6 HelloWorld 서블릿 컴파일 및 실행하기

## URL 주소

http://localhost:8080/{프로젝트이름}/{URL Mapping값}
http://localhost:8080/firstweb/HelloServlet

```
package examples;

import java.io.IOException;
import java.io.PrintWriter;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

/**
 * Servlet implementation class HelloServlet
 */
@WebServlet("/HelloServlet")
public class HelloServlet extends HttpServlet {
	private static final long serialVersionUID = 1L;
       
    /**
     * @see HttpServlet#HttpServlet()
     */
    public HelloServlet() {
        super();
        // TODO Auto-generated constructor stub
    }
    
	/**
	 * @see HttpServlet#doGet(HttpServletRequest request, HttpServletResponse response)
	 */
	protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		response.setContentType("text/html;charset=UTF-8");
		PrintWriter out = response.getWriter();
		out.println("<h1>Hello World</h1>");
	}

}
```
