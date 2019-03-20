1、获取所有系统管理用户：
/user/findAll?token=fade014e255c42b8b856e2d4408c5dd5
{
    "code": "0000",
    "message": "查找所有用户信息数据成功",
    "page": {
        "offset": 0,
        "limit": 2147483647,
        "pageNumber": 1,
        "pageSize": 20,
        "totalCount": 3,
        "pageCount": 1
    },
    "data": [
        {
            "id": "321bc2db8e81410099112c611509193d",
            "userName": "zht",
            "loginName": "zht",
            "password": null,
            "salt": null,
            "mobile": "18826214582",
            "roleId": "kefu1e48d4b39b4b4aab03602bfe1de9",
            "roleName": "客服002",
            "userIcon": "",
            "createTime": 1553095843000,
            "lastTime": null,
            "state": "10"
        },
        {
            "id": "321bc2db8e81410099142c611509193d",
            "userName": "vv",
            "loginName": "vv",
            "password": null,
            "salt": null,
            "mobile": "13536524756",
            "roleId": "kefu1e48d4b39b4b4aab03602bfe1de9",
            "roleName": "客服001",
            "userIcon": null,
            "createTime": 1507861921000,
            "lastTime": null,
            "state": "10"
        },
        {
            "id": "3709027e482f489dbf5a79ab17649bd6",
            "userName": "系统管理员",
            "loginName": "admin",
            "password": null,
            "salt": null,
            "mobile": "13800138000",
            "roleId": "7d1e48d4b39b4b4aab03602bfe1de9a5",
            "roleName": "系统管理",
            "userIcon": null,
            "createTime": 1502784334000,
            "lastTime": 1502784338000,
            "state": "10"
        }
    ]
}


2、获取所有的角色
/user/findRoles?token=fade014e255c42b8b856e2d4408c5dd5

{
    "code": "0000",
    "message": "查找所有角色数据成功",
    "page": null,
    "data": [
        {
            "id": "7d1e48d4b39b4b4aab03602bfe1de9a5",
            "roleName": "超级管理"
        },
        {
            "id": "business48d4b39baab03602bfe1723g",
            "roleName": "商家管理"
        },
        {
            "id": "kefu1e48d4b39b4b4aab03602bfe1de9",
            "roleName": "客服管理"
        }
    ]
}

3、新增系统用户
   /user/add
   {
	"userName":"我",
    "loginName":"uu",
    "password":"123456",
    "roleId":"kefu1e48d4b39b4b4aab03602bfe1de9",
    "roleName":"客服003",
    "mobile":"168123465689",
    "state":"10"
  }
  
  
4、超级管理员分配用户权限
   /role/saveRolePerm
   {
	"roleId":"id",
	"lis":[
			{"resourceId":"a813312e0111e8b09a000c290040be"},
			{"resourceId":"bfb6844b1ddf41ceaa0b842710bc99b0"},
			{"resourceId":"c748751f6c074eb1944de5c213c28c9a"}
	      ]
    }
