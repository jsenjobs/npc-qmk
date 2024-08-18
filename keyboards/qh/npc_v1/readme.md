# 注意，小红点只能在连接usb的一侧使用

# 1 修改左右手的ps/2 io

    // right
    #define PS2_CLOCK_PIN B0
    #define PS2_DATA_PIN  B1
    // track point test
    #define PS2_CLOCK_PIN A8
    #define PS2_DATA_PIN  A9
# 2 编译左右手
    
    qmk flash -kb qh/npc_v1 -km vial -bl dfu-util-split-left
    qmk flash -kb qh/npc_v1 -km vial -bl dfu-util-split-right
    
    编译完成，直接ctrl-c结束，在.build目录下有对应uf2固件
    
