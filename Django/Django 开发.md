# 启用media

第一步：settings.py
```python
import os

# media files 用户上传图片、视频
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')  # 用于指定上传文件的存储路径
MEDIA_URL = '/media/'  # 用于指定url路径
```
第二步：url.py
```python
from django.urls import path, re_path
from django.views.static import serve
from django.conf import settings
 
#以及：
# 上传文件目录
    re_path(r'^media/(?P<path>.*)$', serve, {'document_root': settings.MEDIA_ROOT}, name='media'),
```
第三步：根目录创建 `media` 文件夹