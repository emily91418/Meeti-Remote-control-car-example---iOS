Meeti-Remote-control-car-example---iOS
======================================

Remote Control Car Example - Usage of MeetiFramework



# About Meeti-iOS
https://github.com/MOBAGEL/MeetiFramework

# Web to  Apply for Testing Account for Meeti 
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
Segue for login  
1.The main purpose for login is to get its token. After getting the token, unless it fails otherwise you don't have to call login again


      
### remoteControlViewController 
Default capabilities for remote controller car

1. MUST login to the group before sending a message to that group  
> {
  [[MeetiServer sharedInstance] joinToGroup:EXAMPLE_GROUP_ID shandle:^(NSString *responseString) {
        NSLog(@"Join to group success %@",responseString);
    } fhandle:^(NSString *responseString, NSError *error) {
        NSLog(@"Join to group Fail %@ , error = %@",responseString,error);
    }];
  }

### cameraViewController  
Segue where you can take a photo
