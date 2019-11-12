cpu使用率
cpu=$(cat <(grep 'cpu ' /proc/stat) <(sleep 1 && grep 'cpu ' /proc/stat) | awk -v RS="" '{print ($13-$2+$15-$4)*100/($13-$2+$15-$4+$16-$5)}')

sendmail
{
    "bk_app_code": "bk_nodeman",
    "bk_username": "admin",
    "bk_app_secret": "64a84ed3-f5dc-46e2-a922-7e51e414cd9f",
    "receiver": "kent@canway.net",
    "sender": "151963396@qq.com",
    "title": "This is a Test",
    "content": "<html>Welcome to Blueking</html>"
}
