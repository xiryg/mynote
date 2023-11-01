```python
from selenium import webdriver
from selenium.webdriver.chrome.options import Options
from lxml import etree

# 初始化 Selenium 配置
options = Options()
options.add_argument('--headless')  # 使用无头模式运行Chrome浏览器，即不显示浏览器界面。
options.add_argument('--disable-gpu') # 禁用GPU加速，可在某些环境中提高稳定性。
options.add_argument('--no-sandbox') # 禁用沙盒模式，可在某些环境中解决权限问题。
options.add_argument('--disable-dev-shm-usage') # 禁用/dev/shm临时文件系统，可在某些环境中减少内存占用。

# 使用 Chrome 浏览器驱动
driver = webdriver.Chrome(options=options)

url = 'http://www.weather.com.cn/weather/101010100.shtml'
driver.get(url)

# 获取页面源代码
html = driver.page_source

# 使用 lxml 库解析 HTML 文档
tree = etree.HTML(html)
the1 = tree.xpath('//*[@id="curve"]/div[1]/em[1]/text()')
the2 = tree.xpath('//*[@id="curve"]/div[5]/em[1]/text()')
print(the1,the2)

# 关闭浏览器
driver.quit()
```