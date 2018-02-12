# Linux Class - a problem getting persistence at home?

Hi guys! I had this problem on my home computer: I knew I had installed a functional USB key for
Ubuntu 16.04 with persistence; I had that confirmed on a school computer, but it wouldn’t work on
my laptop. I used a program called **UNetbootin** to create it. However, the **UNetbootin** boot
menu wouldn’t show up at home and instead it would only take me through Ubuntu’s native GRUB
menu (resulting in *no persistence*).

**Perhaps your background with creating your USB is different, but consider my solution in my
case. It may help you with yours.**

I realized that my computer (running Windows 10 64bit) has an option enabled in its UEFI, called
**Secure Boot**. It prevents unknown software from running during booting. I had to **turn that
off**. But that was just one half of my problem. The school is running Windows 7 and I am running
Windows 10. I guess the program I used *didn’t support Windows 10*. As soon as I **enabled**
another UEFI option, **Legacy Support**, I gained new options in my booting menu, showing up
after reboot and pressing Esc for Startup Menu (as prompted) and then F9 for Boot Device
Options. The last one of them “*USB Hard Drive - SanDisk*” (in my case) was the one.
Now it works perfectly fine. 

The problem with Secure Boot is also mentioned towards the end of chapter 5 in the book.

So: **Secure Boot and Legacy Support options in your UEFI/BIOS!** Check them out!

-Pavel.


