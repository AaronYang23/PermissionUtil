# PermissionUtil
[![Release](https://img.shields.io/github/release/AaronYang23/PermissionUtil.svg?style=flat)](https://jitpack.io/#AaronYang23/PermissionUtil)

动态权限申请工具
--

封装的关于Android6.0动态获取用户权限的功能


## Import using Gradle 

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
  
  	dependencies {
	        implementation 'com.github.AaronYang23:PermissionUtil:v1.0'
	}
  
  
  
## How to Use
1、设置包名，用于禁止再次弹窗之后可以跳转到手机对于应用的权限设置界面

  	//初始化设置包名用于跳转应用权限管理设置
  	 PermissionUtils.setPackageName("包名") 
	 
2、检查权限是否获取

  	 //检查权限
   	PermissionUtils.checkManyPermissons（Context context, String[] permissions）{...}
	
	//检查一组权限是否全部获取
	

3、例子

   	//单个权限申请
   	if (PermissionUtils.checkPermisson(mContext, Manifest.permission.WRITE_EXTERNAL_STORAGE)) {
            //to do something
        } else {
            PermissionUtils.requestSinglePermission((Activity) mContext, Manifest.permission.WRITE_EXTERNAL_STORAGE, 2);
        }
	
   
  	//多个权限申请：
	String[] permissons = {Manifest.permission.ACCESS_COARSE_LOCATION, Manifest.permission.BLUETOOTH,  Manifest.permission.CAMERA};
        if (PermissionUtils.checkManyPermissons(this, permissons)) {
            //to do something
        } else {
            PermissionUtils.requestManyPremisson(this, permissons, 1);
        }
	

## Known issues


## Reference


