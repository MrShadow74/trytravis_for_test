MrShadow74_infra
MrShadow74 Infra repository

Homework #1
������ ������� �� GitHub
������ ���� anton_emelianov.txt
�������� ������ Pull Request

Homework #2 ChatOps
������� ����� play-travis
��������� ���������� �� Slack
��������� ���������� � Travis

Homework #3
������� ����� ����� cloud-bastion

������ ����� ������� � GCP
������� ��� ����� �������� f1_micro
������� ������� ��� GCP firewall � ������ vpn-16721

bastion_IP = 34.89.219.137
someinternalhost_IP = 10.156.0.4

� ������� Pritunl ������ VPN-������ �� ����� bastion
������ ������������ test
��������� � ��������� ����������� ��� openvpn ������� � ��������� ����������� � ����� someinternalhost
�������� Let's Encrypt 

������������� �������:
������� � ��������� ����������� ssh-����������� �� ����� someinternalhost �� ��������� ����� � ����������� ssh jump host

alias �������� � ~/.ssh/config �����:

Host someinternalhost
HostName 10.156.0.4
User eaa
IdentityFile ~/.ssh/id_rsa
ProxyCommand ssh -A 34.89.219.137 nc %h %p