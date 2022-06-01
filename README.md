# Ansible을 이용하여 Agent 서버의 CronJob 등록 

## 1. Ansible Playbook Task 순서
1. Agent 서버의 shellScript 디렉터리 생성 
2. Master 서버에 있는 shellScript 파일을 Agent 서버로 copy 후, 실행을 위해 0744로 변경 
3. Agent history 디렉터리 생성 
4. 혹시나 모를 기존의 동일 명으로된 cronjob 삭제 
5. cron 등록 
   - name 설정 
   - month, weekday, day, hour, minute 설정 
   - cron job 등록 유저 설정 
   - job 설정
<br />    
<br />    

## 2. Master 서버에서의 Command
```
$ ansible-playbook enroll_cron.yml -k
```