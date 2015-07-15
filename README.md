# TBIconTransitionKit

[![CI Status](http://img.shields.io/travis/AlexeyBelezeko/TBIconTransitionKit.svg?style=flat)](https://travis-ci.org/AlexeyBelezeko/TBIconTransitionKit)
[![Version](https://img.shields.io/cocoapods/v/TBIconTransitionKit.svg?style=flat)](http://cocoapods.org/pods/TBIconTransitionKit)
[![License](https://img.shields.io/cocoapods/l/TBIconTransitionKit.svg?style=flat)](http://cocoapods.org/pods/TBIconTransitionKit)
[![Platform](https://img.shields.io/cocoapods/p/TBIconTransitionKit.svg?style=flat)](http://cocoapods.org/pods/TBIconTransitionKit)

Small icons kit with animated button transition.

## Usage

To run the example project, clone the repo, and run `pod install` from the Example directory first.

Just add TBAnimationButton to you UIView with IB or code. You can use it with autolayout.

```objective-c
#import <TBIconTransitionKit/TBAnimationButton.h>

@interface TBViewController ()

@property (weak, nonatomic) IBOutlet TBAnimationButton *button;

@end

@implementation TBViewController

- (void)viewDidLoad
{
    [super viewDidLoad];
    self.button.currentState = TBAnimationButtonStateMenu;
}

- (IBAction)onButton:(TBAnimationButton *)sender
{
  if (sender.currentState == TBAnimationButtonStateMenu) {
    [sender animationTransformToState:TBAnimationButtonStateArrow];
  } else if (sender.currentState == TBAnimationButtonStateArrow) {
    [sender animationTransformToState:TBAnimationButtonStateMenu];
  }
}
```

### Customize the design

- `lineHeight`
- `lineWidth`
- `lineSpacing`
- `lineColor`
- `lineCap`

After the change of one of this properties you have to call `updateAppearance` to update the view.

## Requirements

- iOS 7 or higher
- Automatic Reference Counting (ARC)

## Installation

TBIconTransitionKit is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "TBIconTransitionKit"
```

## Author

- [AlexeyBelezeko](https://github.com/AlexeyBelezeko) 
- [Oleg Turbaba](https://dribbble.com/turbab)

## License

TBIconTransitionKit is available under the MIT license. See the LICENSE file for more info.
