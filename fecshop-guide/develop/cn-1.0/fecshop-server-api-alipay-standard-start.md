Api- Onepage Alipay Standard Start
================

> ��׼֧����ѡ��alipay֧����ʽ֧������ת��ҳ����ص�api

URL: `/payment/alipay/standard/start`

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
| return_url      | ����        |   String     | ֧���ɹ�����ת��fecshop��url    |

**�������ʾ�����£�**

```
{
    return_url: "http://demo.fancyecommerce.com/#/payment/alipay/standard/review"
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
        "redirectUrl": "https://openapi.alipaydev.com/gateway.do?alipay_sdk=alipay-sdk-php-20161101&app_id=2016080500172713&biz_content=%7B%22out_trade_no%22%3A%221100000911%22%2C%22product_code%22%3A%22QUICK_WAP_WAY%22%2C%22total_amount%22%3A%22927.80%22%2C%22subject%22%3A%22Raglan+Sleeves+Letter+Printed+Crew+Neck+Sweatshirt+kahaki-xl%22%7D&charset=UTF-8&format=json&method=alipay.trade.wap.pay&notify_url=http%3A%2F%2Ffecshop.appserver.fancyecommerce.com%2Fpayment%2Falipay%2Fstandard%2Fipn&return_url=http%3A%2F%2Fdemo.fancyecommerce.com%2F%23%2Fpayment%2Falipay%2Fstandard%2Freview&sign=W3z2RHb%2BaC1NvaH8lg1Ug1G%2BRFQYW1yX%2FKaofsVopQp%2BAi84gFzL6%2FL85YnFJNy61X20o%2BObUqrQ5C5tbB5%2Bw%2F0IqXlJEkPAH%2FjVNZxyj2aqZBBPP2hY%2BQIyMVmbnQyEOXYlhYi2rhkVuPw%2BmFoJNFWkC5sSf8lQbOoKBFyljNkdnfelTxVliv7aCVuPsiKLMk6uKthwPv2KYJ9xMHM%2FH1panfC6ERHHwl8bUm6sxbD28vKmTLs5oB%2B%2BwCOreK8QdbE0VU9pK6mYpC6%2FwrTqZZEqUUou9WEOB1RVD%2B1L%2B3rroc0bL9Ru2SJbBhd3XE1B1B7MiR9N2qo3DlVjKr4Ifg%3D%3D&sign_type=RSA2&timestamp=2017-11-01+11%3A30%3A44&version=1.0"
    }
}
```