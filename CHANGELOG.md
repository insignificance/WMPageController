## [2.4.0 [API CHANGED][BETA]]()
**[IMPORTANT] WMPAGECONTROLLER ARE NO LONGER ADAPT VIEW'S FRAMES & SOME GESTURES CONFLICTS!!**
### [DELETE] Some properties have been deleted.
- `viewFrame / menuHeight / menuBGColor / menuViewBottomSpace / otherGestureRecognizerSimultaneously`
### [ADD] Two datasource methods have been added.
- `-pageController:preferredFrameForMenuView:` 
- `-pageController:preferredFrameForContentView:`
### [GUIDE]
- If you want a right frame of menuView or contentView, implement `-pageController:preferredFrameForMenuView: & -pageController:preferredFrameForContentView:` methods and give WMPageController a right frame.
- Call `-forceLayoutSubViews` to re-layout view's frames, these will recall the datasource methods above.
- Change menuView's backgroundColor by setting `self.menuView.backgroundColor = perferredColor` directly.(AFTER THE VIEW IS LOADED, e.g. in viewDidLoad)
- Deal gesture's conflicts by implement `UIGestureRecognizerDelegate` IF NEEDED, see [UIGestureRecognizerDelegate](https://developer.apple.com/documentation/uikit/uigesturerecognizerdelegate) for more information.

## [1.0.0 ~ 2.3.1 [OLD VERSION]]()
**OLD VERSION & NO LONGER MAINTAIN**