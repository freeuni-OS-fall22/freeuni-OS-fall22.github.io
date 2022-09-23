## M1 troubleshoot
პრობლემა არის დაკავშირებული xcode-ის command line tools ის ახალ ვერსიასთან. workaround არის რომ წაშალოთ ახალი ვერსია და დააყენოთ ძველი. ამისთვის:
1. `xcode-select -p`-ით ნახეთ ახლანდელი ვერსია სად არის დაყენებული და წაშალეთ `rm -rf`-ს გამოყენებით:
```bash
$ xcode-select -p
/Library/Developer/CommandLineTools
$ sudo rm -rf /Library/Developer/CommandLineTools
# verify uninstall
$ xcode-select -p
xcode-select: error: unable to get active developer directory...
```
2. https://developer.apple.com/download/all/?q=command ამ ლინკზე გადადით, შეიყვანეთ apple ID და მოძებნეთ "Command Line Tools for Xcode 13.4"
![image](https://user-images.githubusercontent.com/6597974/192002676-9678ef9a-4240-4bf6-8e8e-0e2a9eb76dd7.png)
3. გადმოწერეთ ეს dmg და დააყენეთ
4. `xcode-install -p`-ით გადაამოწმეთ რო მართლა დაყენდა და ამის მერე სტანდარტულ ინსტრუქციას მიყევით.
