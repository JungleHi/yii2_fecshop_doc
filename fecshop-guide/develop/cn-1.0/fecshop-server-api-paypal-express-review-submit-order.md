Api- Cart Paypal Express Review SubmitOrder
================

> ���ﳵҳ����paypal��ť����ת��paypal��¼��Ȼ����continue��ת��fecshopҳ�棬
> ҳ���ʼ���󣬱༭������Ϣ��Ȼ�����ύ����ʵ�api

URL: `/payment/paypal/express/submitorder`

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


| ��������          | �Ƿ����    |  ����       |  ����     |
| ----------------  | -----:      | :----:      |:----:     |
| address_id        | ����        |   String    | ����û���¼�˻���ʹ�õ��Ǳ����address��Ϣ����������Ҫ����address id   |
| billing           | ����        |   Array     | �������û���Ϣ�͵�ַ��Ϣ   |
| token             | ����        |   String    | Paypal Token    |
| PayerID           | ����        |   String    | Paypal PayerID  |
| shipping_method   | ����        |   String    | ������ݵ�code  |

**�������ʾ�����£�**

```
{
    address_id:118,
    billing:{
        first_name: "test",
        last_name: "facilitator",
        email: "zqy234api1-facilitator-1@126.com",
        telephone: "2121",
        street1: "4114 Sepulveda Blvd.",
        street2: "4114 Sepulveda Blvd.",
        country: "US",
        state: "NY",
        city: "New York",
        zip: "10021"
    },
    token: "EC-1TN688728J034651L",
    PayerID: "FKL4V7D5GCACY",
    shipping_method: "fast_shipping"
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
    "data": []
}
```