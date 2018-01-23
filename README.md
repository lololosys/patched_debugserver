# patched_debugserver
Patched debugserver with platform-application entitlement that will work in LiberiOS


hdiutil attach /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/ DeviceSupport/7.0.3\ \(11B508\)/DeveloperDiskImage.dmg

cp /Volumes/DeveloperDiskImage/usr/bin/debugserver .

./jtool --inplace --sign --ent entitlements.xml debugserver
