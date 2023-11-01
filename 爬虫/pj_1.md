```python
import requests
from lxml import etree
import csv
url = 'https://so.gushiwen.cn/mingjus/default.aspx?tstr=%e6%98%a5%e5%a4%a9'

headers = {
    'User-Agent': 'Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) '
                  'Chrome/118.0.0.0 Mobile Safari/537.36 Edg/118.0.2088.46'

}

session = requests.Session()
response = session.get(url, headers=headers)
data = response.content.decode()
tree = etree.HTML(data)

the1 = tree.xpath('//div[@class="left"]/div[@class="sons"]/div[@class="cont"]/a[1]/text()')
the2 = tree.xpath('//div[@class="left"]/div[@class="sons"]/div[@class="cont"]/a[2]/text()')

for a,b in zip(the1,the2):
    c = " --- ".join([a,b])
    print(c)


with open('data.csv', mode='w', encoding='utf-8', newline='') as file:
    writer = csv.writer(file)

    header = ['名句', '作者']  # 头部信息
    writer.writerow(header)  # 写入头部信息

    for a, b in zip(the1, the2):
        data = [a, b]
        writer.writerow(data)

```