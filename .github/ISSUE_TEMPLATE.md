* [x] I've read and understood the [*CONTRIBUTING guidelines and have done my best effort to follow](https://github.com/CocoaPods/CocoaPods/blob/master/CONTRIBUTING.md).

# Report

## What did you do?

Run `pod install`

## What did you expect to happen?
Install all pod dependencies correctly - Works.
## What happened instead?
Pods installed correctly.
## CocoaPods Environment

ℹ Please replace this with the output of `pod env`.

### Stack

```
   CocoaPods : 1.0.1
        Ruby : ruby 2.0.0p648 (2015-12-16 revision 53162) [universal.x86_64-darwin15]
    RubyGems : 2.0.14.1
        Host : Mac OS X 10.11.4 (15E65)
       Xcode : 7.3.1 (7D1014)
         Git : git version 2.7.4 (Apple Git-66)
Ruby lib dir : /System/Library/Frameworks/Ruby.framework/Versions/2.0/usr/lib
Repositories : forcedotcom - https://github.com/forcedotcom/SalesforceMobileSDK-iOS-Specs.git @ 62e9a9c8072bf4aaf834bd693c0bbcf9b92bb71d
               master - https://github.com/CocoaPods/Specs.git @ 789d843002aee159a603930889d4c127c65f97d2
```

### Installation Source

```
Executable Path: /usr/local/bin/pod
```

### Plugins

```
cocoapods-deintegrate : 1.0.0
cocoapods-plugins     : 1.0.0
cocoapods-search      : 1.0.0
cocoapods-stats       : 1.0.0
cocoapods-trunk       : 1.0.0
cocoapods-try         : 1.0.0
```

### Podfile

```ruby
# Uncomment this line to define a global platform for your project

platform :ios, '9.0'

target 'PTPMobile' do
source 'https://github.com/forcedotcom/SalesforceMobileSDK-iOS-Specs.git' # need to be first 
source 'https://github.com/CocoaPods/Specs.git'

use_frameworks!
pod 'SalesforceSDKCore'
pod 'SalesforceNetwork'
pod 'SalesforceRestAPI'
pod 'FMDB'
pod 'SmartStore'
pod 'SmartSync'
pod 'AWSS3', '~> 2.3.0'
end
```


## Project that demonstrates the issue

Build fails due to no Headers in the Pods/Headers directory

git@gitlab.com:pillarpost/ptp-mobile-all.git
