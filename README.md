20200716_P1_安裝docker及docker-compose過程寫入腳本(.sh)

寫入腳本setting.sh這支程式裡

1.開啟虛擬機器(centos7)，建議使用user進入(建議別使用root)

2.建議使用MobaXterm 遠端連線程式，ssh遠端連線，進入後打開終端機

  #開啟終端機輸入
	
	#設定sudo權限
	
	su root
	
	grep wheel /etc/group
	
	usermod -aG wheel user1
	
	#需重新啟動遠端連線程式
	
	exit
	
	exit
	
	r
	
	#設定sudo免打sudo密碼
	
	sudo visudo
	
	#找到Allows people in group wheel to run all commands
	
	#(加註解)#%wheel ALL=(ALL)	ALL
	
	#找到Same thing without a password
	
	#(解除註解，刪除#)%wheel ALL=(ALL)	NOPASSWD: ALL
	
	#完成存檔離開，:wq
	
	#需重新啟動遠端連線程式
	
	exit
	
	exit
	
	r
	
	#安裝git
	
	sudo yum install git-all
  
    git clone https://github.com/og80218/2020_docker-dockercompose_installation-process_script.git
	
	#下載完成後
	
	cd 2020_docker-dockercompose_installation-process_script
	
	sh setting.sh
	
	#啟動完成後
	
	#有顯示'docker env. is ready to run.'表示安裝完成。
	
	#看自己帳號有無設定docker 群組
	
	grep docker /etc/group
	
	#設定docker 群組
	
	sudo usermod -aG docker user1
	
#註記:欲修改images，可至資料夾dockerfile目錄下