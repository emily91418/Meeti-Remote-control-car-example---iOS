Meeti-Remote-control-car-example---iOS
======================================

Remote Control Car Example - Usage of MeetiFramework



# About Meeti-iOS
https://github.com/MOBAGEL/MeetiFramework

# Web to  Apply for Testing Account for Meeti 帳號網站
http://meeti.mobagel.com

# Notice of Development    
1.Please enter APP ID and APP SecretKey when using this framework in AppDelegate.m  
2.The default group id is provided in AppDelegate.h   


# Commands for Remote Control Car  
  
### Basic Commands  
1	Initialize remote control car   
t Remote control car takes a photo  
l0	Turn off left light   
l1	Turn on left light   
r0	Turn off right liht   
r1	Turn on right light   
ｂ	Drive back   
f	  Go forward   
lf	Turn left   
rf  Turn right  
s	  Stop   

# Introduction to Main Objects  

### loginViewController  
實現登入的頁面  
1.Login 功能主要是取token， 待token取到後，除非token失效，否則不必再呼叫Login


      
### remoteControlViewController 
實作遙控車的預設的功能

1.輸入訊息前一定要加入群組中  
> {
  [[MeetiServer sharedInstance] joinToGroup:EXAMPLE_GROUP_ID shandle:^(NSString *responseString) {
        NSLog(@"Join to group success %@",responseString);
    } fhandle:^(NSString *responseString, NSError *error) {
        NSLog(@"Join to group Fail %@ , error = %@",responseString,error);
    }];
  }

### cameraViewController  
實現照相機的功能
