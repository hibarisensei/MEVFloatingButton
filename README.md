# MEVFloatingButton
An iOS **drop-in** UITableView, UICollectionView, UIScrollView superclass **category** for showing a customizable floating button on top of it. 

[![BuddyBuild](https://dashboard.buddybuild.com/api/statusImage?appID=58932c0b55013001004c3ff0&branch=master&build=latest)](https://dashboard.buddybuild.com/apps/58932c0b55013001004c3ff0/build/latest?branch=master)
[![Version](https://img.shields.io/cocoapods/v/MEVFloatingButton.svg?style=flat)](http://cocoapods.org/pods/MEVFloatingButton)
[![License](https://img.shields.io/packagist/l/doctrine/orm.svg)](http://cocoapods.org/pods/MEVFloatingButton)
[![Platform](https://img.shields.io/cocoapods/p/MEVFloatingButton.svg?style=flat)](http://cocoapods.org/pods/MEVFloatingButton)
[![Language](http://img.shields.io/badge/language-objective--c-blue.svg?style=flat)](https://developer.apple.com/library/mac/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html)

![MEVFloatingButton](https://cloud.githubusercontent.com/assets/1849990/13462466/db001be6-e087-11e5-92a1-79c8ecefb715.gif "An iOS **drop-in** UITableView, UICollectionView, UIScrollView superclass **category** for showing a customizable floating button on top of it.")

 
## Features
* Multiple animation types.
* Different display modes.
* Different screen positions.
* Customizable button icon.
* Multiple delegate methods.

## Demo
[Demo App](https://appetize.io/app/rkaym9brp1yva59ejat5xdh9yc)

## Usage

To run the example project, clone the repo, and run `pod install` from the Example directory first.

#### Requirements

Requires iOS SDK version > 8.0


#### Installation
---

##### CocoaPods 

MEVFloatingButton is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'MEVFloatingButton'
```

##### Manual 

Simply include `UIScrollView+FloatingButton.h` and `UIScrollView+FloatingButton.m` from `/Pod/Classes/` folder in your App’s Xcode project. 

#### How to use
---
##### Step 1

```objective-c
#import "UIScrollView+FloatingButton.h"
```

##### Step 2

Add datasource and delegate methods.

```objective-c
@interface ViewController () <MEVFloatingButtonDelegate>
```

```objective-c
#pragma mark - MEScrollToTopDelegate Methods

- (void)floatingButton:(UIScrollView *)scrollView didTapButton:(UIButton *)button;
- (void)floatingButtonWillAppear:(UIScrollView *)scrollView;
- (void)floatingButtonDidAppear:(UIScrollView *)scrollView;
- (void)floatingButtonWillDisappear:(UIScrollView *)scrollView;
- (void)floatingButtonDidDisappear:(UIScrollView *)scrollView;
```

##### Step 3

Create a `MEVFloatingButton`object.

```objective-c
MEVFloatingButton *button = [[MEVFloatingButton alloc] init];
button.animationType = MEVFloatingButtonAnimationFromBottom;
button.displayMode = MEVFloatingButtonDisplayModeWhenScrolling;
button.position = MEVFloatingButtonPositionBottomCenter;
button.image = [UIImage imageNamed:@"Icon0"];
button.imageColor = [UIColor groupTableViewBackgroundColor];
button.backgroundColor = [UIColor darkGrayColor];
button.outlineColor = [UIColor darkGrayColor];
button.outlineWidth = 0.0f;
button.imagePadding = 20.0f;
button.horizontalOffset = 20.0f;
button.verticalOffset = -30.0f;
button.rounded = YES;
button.hideWhenScrollToTop = YES;
```

Set the object to your UIScrollView/UITableView/UICollectionView.

```objective-c
[self.tableView setFloatingButtonView:button];
```

Set the delegate.

```objective-c
[self.tableView setFloatingButtonDelegate:self]
```


## Sample Project

For more info check the **Examples** project. Everything is there.

## Change Log

See [Changelog.md](https://github.com/manuelescrig/MEVFloatingButton/blob/master/CHANGELOG.md)

## Author

Manuel Escrig Ventura, [@manuelescrig](https://www.twitter.com/manuelescrig/)

## Credits

Icons made by Elegant Themes from www.flaticon.com 

## License

MEVFloatingButton is available under the MIT license. 
See [License.md](https://github.com/manuelescrig/MEVFloatingButton/blob/master/LICENSE.md)
