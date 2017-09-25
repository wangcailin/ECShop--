# ECShop--
ECShop-常用功能开发

### 后台添加菜单
```php
Ecshop 后台增加一个左侧列表菜单menu菜单需要修改三个文件：
/admin/includes/inc_menu.php
/admin/includes/inc_priv.php
/languages/zh_cn/admin/common.php

1.在/admin/includes/inc_menu.php中增加
$modules['03_promotion']['16_progoods_list']        = 'progoods.php?act=list';
前面03_promotion是比如商品管理，促销管理这样的一级菜单，后面的'16_progoods_list'是下面的二级菜单，这个'16_progoods_list'我们会在common.php里面用到，这是在模板里面用的，
 
2.所以，接下来要在/languages/zh_cn/admin/common.php中添加一个
$_LANG['16_progoods_list'] = '热门促销';
 
3.在权限管理/admin/includes/inc_priv.php中添加一个权限
$purview['16_progoods_list']       = 'progoods_manage'; //热门促销
这样才能操作，当然后面的'progoods_manage'是你自己取的哈
```
