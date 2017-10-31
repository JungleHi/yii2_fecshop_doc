Api- Customer ע���ύ
================

> ע���˻�����д��Ϣ�ύ��ִ�е�api

URL: `/customer/register/account`

��ʽ��`json`

��ʽ��`post`


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


| ��������        | �Ƿ����    |  ����       |  ����     |
| ----------------| -----:      | :----:      |:----:     |
| email           | ����        |   String     | ע���˻�email    |
| password        | ����        |   String     | ע������         |
| firstname       | ����        |   String     | firstname        |
| lastname        | ����        |   String     | lastname         |
| is_subscribed   | ����        |   boolean    | �Ƿ����ʼ�     |
| captcha         | ����        |   String     | ��֤��           |

**�������ʾ�����£�**

```
{
    email: "zqy2345678@126.com",
    password: "111111",
    firstname: "terry",
    lastname: "water",
    is_subscribed: true,
    captcha: "8272"
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
        "content": "register success"
    }
}
```