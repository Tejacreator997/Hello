How to Install nginx in Amazon Linux 2023 server?

1.Login  to server with admin access
$ sudo sudo

2.Update the package repository  Before installing nginx
#sudo dnf update -y

3.Install nginx 
#sudo dnf install nginx -y

4.Start the nginx service
#sudo systemctl start nginx

5.Verify nginx service is started or not
#sudo systemctl status nginx

6.Enable nginx services start on server boot
#sudo systemctl enable nginx

7.Enable nginx service to start on boot 
#sudo systemctl enable nginx

8.verify after server reboot nginx sevice in started or not
#sudo systemctl status nginx

9.Enable nginx inbound rule in security group of instance in EC2

port :80
Protocal :http
source :Anywhere

10.Take Public Ip of instance and browse from any internet browse
verify :it will show "Welcome to nginx!"