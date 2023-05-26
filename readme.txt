Unzip The Downloaded Files
Copy "graphics.h" And "winbgim.h" Files To "include" Folder Of Dev C++ Directory [ Default Location is C:\Program Files\Dev-Cpp\MinGW64\include\ ]
Copy "libbgi.a" To "lib" Folder Of Dev C++ Directory [ Default Location is C:\Program Files\Dev-Cpp\MinGW64\lib ]
Now Open Dev C++ , File => New => Project => Basic => Console Application
Go To Project => Project Options [ or CTRL + H ]


Select Parameter Tab From Project Options. In Linker Add Following Codes [Remove Any Code If Exist ]
-lbgi
-lgdi32
-lcomdlg32
-luuid
-loleaut32
-lole32



Select TDM-GCC x.x.x 32-bit Release From Drop Down Menu [Where x.x.x is Version ]


#include<graphics.h>
int main()
{
    int gd=DETECT,gm;
    initgraph(&gd,&gm,"");
    circle(200,200,100);
    getch();
}