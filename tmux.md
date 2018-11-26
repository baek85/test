# Start Session
	새 세션 생성
	tmux new -s <session-name>

	세션 이름 수정
	ctrl + b, $

	세션 종료
	(tmux에서) exit

	세션 중단하기 (detached)
	ctrl + b, d

	세션 목록 보기 (list-session)
	tmux ls

	세션 다시 시작
	tmux attach -t <session-number or session-name>

	새 윈도우 생성
	ctrl + b, c

	세션 생성시 윈도우랑 같이 생성
	tmux new -s <session-name> -n <window-name>

	윈도우 이름 수정
	ctrl + b, ,

	윈도우 종료
	ctrl + b, &
	ctrl + d

	윈도우 이동
	ctrl + b, 0-9 : window number
		    n : next window
		    p : prev window
		    l : last window
		    w : window selector
		    f : find by name



	틀 나누기
	ctrl + b, % : 횡 분할
		  " : 종 분할

	틀 이동
	ctrl + b, q 그리고 화면에 나오는 숫자키
	ctrl + b, o : 순서대로 이동
	ctrl + b, arrow : 방향키로 숑숑

	틀 삭제
	ctrl + b, x
	ctrl + d

	틀 사이즈 조절
	(ctrl + b, :)
	resize-pane -L 10
		    -R 10
		    -D 10
		    -U 10

	틀 레이아웃 변경
	ctrl + b, spacebar

	단축키 목록
	ctrl + b, ?

	키 연결 및 해제 bind and unbind
	(ctrl + b, :)
	bind-key [-cnr] [-t key-table] key command [arguments]
	unbind-key [-acn] [t key-table] key

	옵션 설정 `set` and `setw`
	set -g <option-name> <option-value>  : set-option
	setw -g <option-name> <option-value> : set-window-option
	
	
# Make own environment

# Save & load setting
