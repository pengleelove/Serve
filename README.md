# Serve
1. 代码主要有一个功能是获取设备UDID
代码如下，此次仅仅是学习git的使用，以前没有使用过，以后有好的代码会与大家一起分享，另外，还希望大神都不要见笑，因为我也是刚起步，很多还有不懂之处，希望多多给予指导。



-(NSString*) uuid {
CFUUIDRef puuid = CFUUIDCreate( nil );
CFStringRef uuidString = CFUUIDCreateString( nil, puuid );
NSString * result = (NSString *)CFBridgingRelease(CFStringCreateCopy( NULL, uuidString));
CFRelease(puuid);
CFRelease(uuidString);
return result ;

}
