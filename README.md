# FigureBest v4.4
FigureBestv4.4 SCI绘图美化

FigureBest（简称：FB）是图图基于MATLAB开发的懒人式数据图美化软件。可自动识别绘图类型(plot,bar,boxplot,scatter,surf,...)，提供高端的配色方案并一键美化;具备强大批处理功能，同步调节多张图；旧版已有取色器、滤波器、动画制作、高清导出...

[2022.07.15]

![image](https://user-images.githubusercontent.com/104671948/179134287-ade0dad3-a12f-4cc3-975d-dfbbf59f50d0.png)

![image](https://user-images.githubusercontent.com/104671948/179134612-29a156f1-6c06-41a4-a586-afd37d6c089c.png)


![image](https://user-images.githubusercontent.com/104671948/179134649-40eb2b42-af46-41c7-81f7-c27cdba36a19.png)

![image](https://user-images.githubusercontent.com/104671948/179134727-7582ba0e-2b12-4723-af8a-448a73288872.png)

![image](https://user-images.githubusercontent.com/104671948/179134794-d5c0586c-2158-4f4c-94cb-a230d8006c53.png)


# 启动函数 fb.m
可以选择和之前一样添加路径；也可以直接运行fb.m启动，我在这里也写一遍fb.m，请认真阅读，其实也是一个重要教程。

```
% % FigureBest start
% @图通道
% 支持 macos,windows,matlab after or 2016a
disp('FB is starting...')

%% encoding check
% ---------------------------
% PASS: UTF8 OR GBK
% WARNING: 'OTHERS'
DefaultCharacterSet = feature('DefaultCharacterSet');
locale = feature('locale');
encoding = locale.encoding;
if ~strcmp(DefaultCharacterSet,'GBK') | ~strcmp(encoding,'GBK')
    disp(['[DefaultCharacterSet]' DefaultCharacterSet '; ' '[encoding]' encoding])
    disp('Chaos character MAY occur if were NOT GBK, while main functions wonnot be affected!')
    disp('Please change the encoding IF possible')
end

%% set path
% ---------------------------
folderOfThis = fileparts(mfilename('fullpath')); % get the folder of current .m
addpath(genpath(folderOfThis)); % add path and subpath (temporary)
savepath % add path and subpath (permanent)
cd(folderOfThis) % change current folder
clear folderOfThis

%% start fb
% ---------------------------
% % 如何安装启动fb?
% 第一步：解压代码包
% 第二步：将所有文件放置在合适的不常动的位置；确保拥有读写权限；否则会存在功能隐患
% 第三步：运行fb.m函数（第一次启动时）
% 第四步：之后启动，满足第二步的情况下，输入fb即可快速启动
% 上方内容主要用于自动设置路径
%
% % 提升速度与排查?
% 第一次运行之后，可以注释上方set path内容提升启动速度/不自动切换路径；
% 如果运行有卡顿或者java报错，请合理增大java堆内存,在：预设-常规-java堆内存
% 如果无法写入，切换current folder到桌面
% 每次替换许可证后将上方注释打开一次
% 遇到问题通常打开set path注释都可以解决
FigureBest_v4
```

# 使用教程

- [1] 4.0: https://www.bilibili.com/video/BV1Fh411S7cM

- [2] 4.1: https://www.bilibili.com/video/BV1i64y1o7Fo

- [3] 4.2: https://www.bilibili.com/video/BV1vb4y1r7d5

- [4] 4.3: https://www.bilibili.com/video/BV17L4y1x78W

- [5] 4.4: https://www.bilibili.com/video/BV1m34y1H7QB
