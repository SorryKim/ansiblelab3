
Quiz. CentOS7 에 대해서만 다음의 내용을 진행해 보세요
	
git hub 에 repo 를 하나 만든다. 로컬에서 개발자는 index.html 파일을 간단히 작성하여 원격저장소에 push 한다.

앤서블 플레이 북이 실행되면 원격저장소로 부터 처음에는 clone 이 된다. 해당 정보는 웹서버의 기본 디렉토리로 clone 되어야 하며 http://192.168.121.X/ansiblelab3  으로 접속시 개발자가 push 한 내용을 확인할 수 있어야 한다.
	
만약 개발자가 index.html 파일 내용을 수정하여 다시 원격저장소에 push 했다면 이후 playbook 을 실행했을 대에는 pull 해야 하고 이는 새로운 페이지로 갱신이 되어야 한다.

clone, update(pull) 이 발생한다면 매번 관리자가 systemctl restart httpd 를 할 수는 없다. trigger 를 이용하여 clone , update 가 발행하면 자동으로 httpd 를 재실행하고 해당 내용은 변수에 담겨 debug 로 처리된다. 
