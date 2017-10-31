Api- Customer �����������ó�ʼ��
================

> �������뷢�͸��û�������û����������������ӽ�����վ��VUE���ʵ�api

URL: `/customer/forgot/resetpassword`

��ʽ��`json`

��ʽ��`get`


һ�����󲿷�
---------

#### 1.Request Header


| ��������          | �Ƿ����    |  ����        |  ����     |
| ------------------| -----:      | :----:       |:----:     |
| access-token      | ����        |   String     | ��localStorageȡ������ֵ��ʶ���û���¼״̬�ı�ʾ���û���¼�ɹ�������˷���access-token��VUE���浽localStorage�У�����һ�������localStorageȡ�����ŵ�request header��   |
| fecshop-uuid      | ����        |   String     | ��localStorageȡ������ֵ���û���Ψһ��ʾ��VUE��һ�η��ʷ���ˣ�����˻᷵��fecshop-uuid ��VUE���䱣�浽���أ������ÿһ��������Ҫ����fecshop-uuid    |
| fecshop-currency  | ����        |   String     | ��localStorageȡ������ֵ����ǰ�Ļ���ֵ  |
| fecshop-lang      | ����        |   String     | ��localStorageȡ������ֵ����ǰ������code  |


#### 2.Request Body Form-Data��


| ��������        | �Ƿ����    | ����        | ����            |
| ----------------| -----:      | :----:      | :----:          |
| resetToken      | ����        |   String    | ��������token   |

**�������ʾ�����£�**

```
{
    resetToken: "zaow-pri7o_w_p2DTLFs1z0iC4xonLIY_1509445774"
}
```

�������ز���
----------

#### 1.Reponse Header

| ��������          | �Ƿ����    |  ����        |  ����     |
| ------------------| -----:      | :----:       |:----:     |
| access-token      | ѡ��        |   String     | �û���¼�ɹ�������˷���access-token��VUE���浽localStorage�У�����һ�������localStorageȡ�����ŵ�request header��   |
| fecshop-uuid      | ����        |   String     | �û���Ψһ��ʾ��VUE��һ�η��ʷ���ˣ�����˻᷵��fecshop-uuid ��VUE���䱣�浽���أ������ÿһ��������Ҫ����fecshop-uuid    |

#### 2.Reponse Body Form-Data��

��ʽ��`json`

| ��������        | �Ƿ����    |  ����       |  ����        |
| ----------------| -----:      | :----:      |:----:        | 
| code            | ����        |   Number    | ����״̬�룬200 ������ɣ������ķ���״̬����ϸ�ο�:[Api- ״̬��](fecshop-server-return-code.md) |
| message         | ����        |   String    | ����״̬�ַ�������  |
| data            | ����        |   Array     | ������ϸ����        |

�������ݾ�����

```
{
    "code": 200,
    "message": "process success",
    "data": {
        "resetPasswordActive": true
    }
}
```