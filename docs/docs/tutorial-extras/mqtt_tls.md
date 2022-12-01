---
sidebar_position: 3
---

# MQTTʹ��X509����ͨѶ���豸��֤

 IoTSharp֧��MQTTЭ��ͨ�� TLS 1.2 ����ͨѶ�� ������ͨ��X509֤������豸��֤��¼�� 

## ����

�� appsettings.Production.json����Ҫ ָ�������� ������EnableTlsΪtrue

~~~ json
  "MqttBroker":
  {
	  "DomainName":"http://demo.iotsharp.net:2927/",
	  "EnableTls":"true"
  }
~~~

�����docker ���ӳ��Ŀ¼  �� ����������ǽ������ļ��� ֤��Ŀ¼ӳ���ڵ�ǰ�ļ��С� 

```
    volumes:
       - "./appsettings.Production.json:/app/appsettings.Production.json"
       - "./data/security:/app/security"
```       

## ��ǩ����֤����豸֤��

��ϵͳ����Ա�˺Ŵ�����->֤�飬 ���ǩ�� �� ˢ�½��棬 ��ʾָ����Ϣ�� ˵��ǩ���ɹ��� 
�½�һ��֤�飬 ѡ��X509 ��֤��ʽ�� �������֤����棬 �������֤�飬 Ȼ�����ء� 

##  ʹ��mqtt.fx ͨ��x509֤������
�½����ӣ� ���ö˿�Ϊ 8883 �� ѡ�� SSL/TLS ,��ѡ�����ã� ѡ��TLS �汾Ϊ 1.2   �� ��ѡ�� Self Sigend certificates , ����ѡ���֤��ca.crt �� �豸֤�� client.crt���Լ��豸˽Կ client.ke , ����ѡ�� PEM format   ���ȷ�ϡ� ���Ӽ��ɡ� ����ͼ��ʾ:

![](/img/iotsharp/mqtt_x509.png)

�й� MQTT�������ң����������� �� ��ο� ����½ڡ� 
