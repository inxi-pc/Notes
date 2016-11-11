# cheezmall b2b 测试结果

* Brand

| Controller | URL | 参数组合 | 结果 |
| --- | --- | --- | --- |
| AdminBrandManagementBrandApproveController | POST /admin/brand/brand_management/approve  | brand_id=1（错误参数名） | Response(302)，响应无错误信息，控制台无错误信息，数据库未改动 |
| AdminBrandManagementBrandApproveController | POST /admin/brand/brand_management/approve  | brandId=1(status参数缺失) | Response(302)，响应无错误信息，控制台报错，数据库未改动 |
| AdminBrandManagementBrandApproveController | POST /admin/brand/brand_management/approve  | brandId=1&status=1(正常参数) | Response(302)，响应无错误信息，控制台无错误信息，数据库正常修改 |
| AdminBrandManagementBrandCreateController | POST /admin/brand/brand_management/create | en_name=1(错误参数名) | Response(302)，响应无错误信息，控制台无错误信息，数据库未插入 |
| AdminBrandManagementBrandCreateController | POST /admin/brand/brand_management/create | enName=“test”(参数缺失) | Response(302)，响应无错误信息，控制台报错，数据库未插入 |
| AdminBrandManagementBrandCreateController | POST /admin/brand/brand_management/create | enName=“test”&chName=“test”&imgList=“test"(正常参数) | Response(302)，响应无错误信息，控制台无错误信息，数据库正常插入 |
| AdminBrandManagementBrandDeleteController | POST /admin/brand/brand_management/delete | brand_id=1(错误参数名) | Response(302)，响应无错误信息，控制台无错误信息，数据库未删除  |
| AdminBrandManagementBrandDeleteController | POST /admin/brand/brand_management/delete | brandId=1(正常参数) | Response(302)，响应无错误信息，控制台无错误信息，数据库正常删除  |
| AdminBrandManagementBrandUpdateController | POST /admin/brand/brand_management/update | brand_id=1（错误参数名）  | Response(302)，响应无错误信息，控制台无错误信息，数据库未改动 |
| AdminBrandManagementBrandUpdateController | POST /admin/brand/brand_management/update | brandId=1&englishName＝“test”（参数缺失） | Response(302)，响应无错误信息，控制台无错误信息，数据库未改动 |
| AdminBrandManagementBrandUpdateController | POST /admin/brand/brand_management/update | brandId=1&englisthName=“test”&chineseName=“test” (正常参数) | Response(302)，响应无错误信息，控制台无错误信息，数据库未改动 |
| AdminBrandManagementExcelExportController | POST /admin/brand/brand_management/generate  | 无参数 | Response(302)，响应无错误信息，控制台报错，无数据输出 |

* Category

| Controller | URL | 参数组合 | 结果 |
| --- | --- | --- | --- |
| AdminCategoryManagementCategoryCreateController | POST /admin/product/category_management/create | nae=“test”(参数名错误) | Response(302)，响应无错误信息，控制台报错，数据库未插入  |
| AdminCategoryManagementCategoryCreateController | POST /admin/product/category_management/create | name=“test”&chinese_name=“test”（参数缺失） | Response(302)，响应无错误信息，控制台报错，数据库未插入 |
| AdminCategoryManagementCategoryCreateController | POST /admin/product/category_management/create | name=test&chinese_name=test&parent_id=1&level=1&skuPropertyList=[{"key":1, "value": [1, 2]}]&productPropertyList=[{"key":1, "type": 1}]&commission=1&agreeReturnRate=1（正常参数） | Response(302)，响应无错误信息，控制台无错误信息，数据库正常插入 |
| AdminCategoryManagementCategoryDeleteController | POST /admin/product/category_management/delete | categoryId=1897（参数名错误） | Response(302)，响应无错误信息，控制台报错，数据库未删除 |
| AdminCategoryManagementCategoryDeleteController | POST /admin/product/category_management/delete | category_id=1897（正常参数） | Response(302)，响应无错误信息，控制台无错误信息，数据库正常删除 |
| AdminCategoryManagementCategoryPropertyQueryController | POST /admin/product/category_management/query_property | categoryId=1897（参数名错误） | Response(302)，响应无错误信息，控制台无错误信息，无数据输出 |
| AdminCategoryManagementCategoryPropertyQueryController | POST /admin/product/category_management/query_property | category_id=1897（正常参数） | Response(302)，响应无错误信息，控制台报错，无数据输出 |
| AdminCategoryManagementCategoryUpdateController | POST /admin/product/category_management/update | categoryId=1897（参数名错误） | Response(302)，响应无错误信息，控制台报错，数据库未改动 |
| AdminCategoryManagementCategoryUpdateController | POST /admin/product/category_management/update | category_id=1897&name=“test”（参数缺失） | Response(302)，响应无错误信息，控制台报错，数据库未改动 |
| AdminCategoryManagementCategoryUpdateController | POST /admin/product/category_management/update | name=wtaasd&chinese_name=taeasd&parent_id=1&level=1&skuPropertyList=[{"key":1, "value": [1, 2]}]&productPropertyList=[{"key":1, "type": 1}]&commission=1&agreeReturnRate=1&category_id=1897（正常参数） | Response(302)，响应无错误信息，控制台无错误信息，数据库未改动 |


* User

| Controller | URL | 参数组合 | 结果 |
| --- | --- | --- | --- |
| AdminUserManagementUserCreateController | POST /admin/user/user_management/create | emai=“test"（参数名错误） | Response(302)，响应无错误信息，控制台无错误信息，数据库未插入 |
| AdminUserManagementUserCreateController | POST /admin/user/user_management/create | email=“test”（参数缺失） | Response(302)，响应无错误信息，控制台无错误信息，数据库未插入 |
| AdminUserManagementUserCreateController | POST /admin/user/user_management/create | email=test&password=test（参数正常） | Response(302)，响应无错误信息，控制台无错误信息，数据库正常插入 |
| AdminUserManagementUserDeleteController | POST /admin/user/user_management/delete | userId=891（参数名错误） | Response(302)，响应无错误信息，控制台无错误信息，数据库未删除 |
| AdminUserManagementUserDeleteController | POST /admin/user/user_management/delete | user_id=891（参数正常） | Response(302)，响应无错误信息，控制台无错误信息，数据库正常删除 |
| AdminUserManagementUserUpdateController | POST /admin/user/user_management/update | userId=891（参数名错误） | Response(302)，响应无错误信息，控制台无错误信息，数据库未改动 |
| AdminUserManagementUserUpdateController | POST /admin/user/user_management/update | user_id=891（参数缺失） | Response(302)，响应无错误信息，控制台无错误信息，数据库未改动 |
| AdminUserManagementUserUpdateController | POST /admin/user/user_management/update | user_id=891&role_id=2（参数正常） | Response(302)，响应无错误信息，控制台无错误信息，数据库正常改动 |
| AdminUserManagementUserExcelExportController | GET /admin/user/user_management/generate | 无参数 | Response(302)，响应无错误信息，控制台无错误信息，无excel文件获取 |


