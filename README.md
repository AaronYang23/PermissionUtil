# PermissionUtil
动态权限申请工具

导入：  

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
  
  	dependencies {
	        implementation 'com.github.AaronYang23:PermissionUtil:v1.0'
	}
  
  
  
  
  使用：
  
  	//初始化设置包名用于跳转应用权限管理设置
  	 PermissionUtils.setPackageName("包名") 
   
  	 //检查权限
   	PermissionUtils.checkManyPermissons（Context context, String[] permissions）{...}
   
   
   	//单个权限申请
   	PermissionUtils.requestSinglePermission(Activity activity, String permission, int requestCode) {...}
   
   
  	 //多个权限申请
  	 PermissionUtils.requestManyPremisson(Activity activity, String[] permissions, int requestCode){...}
