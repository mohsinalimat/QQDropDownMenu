# QQDropDownMenu
模仿QQ下拉窗口


# PhotoShoot
![image](https://github.com/Zws-China/.../blob/master/wedwed.gif)


# How To Use

```ruby

#import "FFDropDownMenuView.h"

/** 下拉菜单 */
@property (nonatomic, strong) FFDropDownMenuView *dropdownMenu;


self.dropdownMenu = [FFDropDownMenuView ff_DefaultStyleDropDownMenuWithMenuModelsArray:[self getMenuModelsArray] menuWidth:FFDefaultFloat eachItemHeight:FFDefaultFloat menuRightMargin:FFDefaultFloat triangleRightMargin:FFDefaultFloat];


/** 获取菜单模型数组 */
- (NSArray *)getMenuModelsArray {


    //菜单模型0
    FFDropDownMenuModel *menuModel0 = [FFDropDownMenuModel ff_DropDownMenuModelWithMenuItemTitle:@"QQ" menuItemIconName:@"menu2"  menuBlock:^{

        NSLog(@"点击了QQ");
        UIAlertView *alert = [[UIAlertView alloc]initWithTitle:@"点击了QQ" message:nil delegate:nil cancelButtonTitle:nil otherButtonTitles:nil, nil];
        [alert show];
        [alert performSelector:@selector(dismissWithClickedButtonIndex:animated:) withObject:nil afterDelay:1.5];

    }];


    //菜单模型1
    FFDropDownMenuModel *menuModel1 = [FFDropDownMenuModel ff_DropDownMenuModelWithMenuItemTitle:@"Line" menuItemIconName:@"menu1" menuBlock:^{
        NSLog(@"点击了Line");
        UIAlertView *alert = [[UIAlertView alloc]initWithTitle:@"点击了Line" message:nil delegate:nil cancelButtonTitle:nil otherButtonTitles:nil, nil];
        [alert show];
        [alert performSelector:@selector(dismissWithClickedButtonIndex:animated:) withObject:nil afterDelay:1.5];
    }];

    //菜单模型2
    FFDropDownMenuModel *menuModel2 = [FFDropDownMenuModel ff_DropDownMenuModelWithMenuItemTitle:@"Twitter" menuItemIconName:@"menu0" menuBlock:^{
        NSLog(@"点击了Twitter");
        UIAlertView *alert = [[UIAlertView alloc]initWithTitle:@"点击了Twitter" message:nil delegate:nil cancelButtonTitle:nil otherButtonTitles:nil, nil];
        [alert show];
        [alert performSelector:@selector(dismissWithClickedButtonIndex:animated:) withObject:nil afterDelay:1.5];
    }];

    NSArray *menuModelArr = @[menuModel0, menuModel1, menuModel2];
    return menuModelArr;
}



/** 显示下拉菜单 */
[self.dropdownMenu showMenu];



```