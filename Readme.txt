1、基於lonely公布的nt6 lib
2、直接雙擊startnt32.bat或者startnt64.bat即可，一個是32位driver，一個是64位driver
3、默認不使用數據庫，單機版直接運行
4、使用數據庫的方法就不說了
a、參照"架設mud服務器指南.c"創建數據庫，導入時可以使用nitan_mine.sql，這個已經清空了所有數據的
b、打開include/unixconf.h，找到#undef DB_SAVE，去掉這行

另外，clone/user/user.c中的函數is_admin，如果要使用call之類的命令，請把自己的id加在這裡，或者先call me->set_admin()