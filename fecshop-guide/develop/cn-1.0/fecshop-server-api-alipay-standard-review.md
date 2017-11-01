Api- Onepage Alipay Standard Review
================

> ��׼֧����ѡ��alipay֧����ʽ֧���ɹ��󷵻�fecshopҳ����ص�api�����ڷ���֧����
> ,��֤��ǰ�����Ƿ�֧���ɹ���

URL: `/payment/alipay/standard/review`

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


| ��������        | �Ƿ����    |  ����       |  ����     |
| ----------------| -----:      | :----:      |:----:     |
| total_amount    | ����        |   String    | �������ܽ��    |
| timestamp       | ����        |   String    | ֧��ʱ��   |
| sign            | ����        |   String    | ǩ�������ڰ�ȫ��֤�� |
| trade_no        | ����        |   String    | ֧�����Ķ�����     |
| sign_type       | ����        |   String    | ǩ������  |
| auth_app_id     | ����        |   String    | ֧������appId�����������֤��  |
| charset         | ����        |   String    | ����  |
| seller_id       | ����        |   String    | �̼�id�����������֤  |
| method          | ����        |   String    | �����api��method  |
| app_id          | ����        |   String    | appid  |
| out_trade_no    | ����        |   String    | ��ϸ��֧�����ӿ�  |
| version         | ����        |   String    | ֧����֧���ӿڵİ汾��  |


**�������ʾ�����£�**

```
{
    total_amount: "927.80",
    timestamp: "2017-11-01 11:39:51",
    sign: "UynUHkgJWkWYIz3F7/bqu+nJcjKsGYijDsERELtnUBGBDa9utAsMdMv7AC6tN+/ANFoXh6yzmNh+gJ7Sws4Ka4Ea8PiAHCQCRPUhZ6lPCfKUB0RPq9bdVZ6yBoF54iODEjveeIsjAQR3pnSLzy5xf+oZyLsYWLxuFuLR/2OfJeuIU1quFH4kKCGAIYbgzfCk77cQ9mpufE4W9jKqH3A2EILJR8X78E6B09sMki+FysZ+ZiFkIJNUQTk9liDXN+98g89Tf+AUOAlm16UnyLMCHJvhc9/GCMRP8WNMOaisuC8VKqMpEFPHF5g/8LFy9fA2JCFnZt5JRvqIZR6vv6swEw==",
    trade_no: "2017110121001004590200337793",
    sign_type: "RSA2",
    auth_app_id: "2016080500172713",
    charset: "UTF-8",
    seller_id: "2088102170055546",
    method: "alipay.trade.wap.pay.return",
    app_id: "2016080500172713",
    out_trade_no: "1100000914",
    version: "1.0"
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
    "data": {}
}
```