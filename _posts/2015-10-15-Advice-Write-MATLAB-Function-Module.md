---
layout: post
title: MATLAB函数及模块编写的经验总结
categories:
- MATLAB
- Programming
tags:
- MATLAB
- 函数
- 模块
- 画图
- 经验
---

最近自己写了一些MATLAB的函数集，同时也看了看Kevin sheppard的MFE包里的所有函数。总结了一些编写函数及模块所能用到的实用的经验。

1. 善于用nargin来判断参数个数，用varnargin来使用可变参数个数。
2. 善于用各种小的效用函数。例如：whos，strcmp，strcmpi，lower，error，warning，disp，fprintf，rem，mod等函数以及is类函数。
3. 善于用struct结构的数据，甚至可以用多重strcut。例如result.para，result.std。善用cell类数据结构。
4. 一个函数的开头注释：最先是函数的介绍，第二是用法，第三是输入，第四是输出，第五是自己的comment，第六是examples，最后是copyright。
5. 函数的最后一个input善用options。
6. 善于用句柄函数。例如 g = @(x) min(x,1-x);
7. switch case这种条件结构在函数编写的时候特别有用，同时注意这个结构里面会有个otherwise。while这种循环结构平时用的不多，写函数时
8. 有时候可以在一个m文件中编写多个函数。前提是主函数意外的子函数不需要单独使用，只在主函数中用到。这样做的好处是既不让使用者直接接触到这些不需要用到的子函数，又增强了封装性。
9. Return在子函数里的用处很大。
10. tic和toc都是有返回值的，tic返回值为代码执行时系统时间，toc的返回值为elapsed time。
11. seed0 = randn('state’),这样的代码就可以当seed中。还可以randn('state’,100)。
12. feval这个神奇的函数一定要用好。
13. 画图要规范，不要图省事。下面的一段是MFE里面的画图代码。

``` PYTHON
fig = figure('Position',[100 100 800 600]);
s1=subplot(2,1,1);
h1=plot(dates,[y yhat]);
axis tight;
ax=axis;
spread = ax(4)-ax(3);
ax(3)=ax(3)-.1*spread;
ax(4)=ax(4)+.1*spread;
axis(ax);
legend('Data','Fit');
if dateflag
    datetick('x','keeplimits')
end
t1=title('Data and Fit');
set(h1,'LineWidth',2)
set(s1,'LineWidth',2,'FontSize',12,'FontWeight','Bold')
set(t1,'FontSize',12,'FontWeight','Bold')
% Residual Subplot
s2=subplot(2,1,2);
h2=plot(dates,errors);
axis tight;
ax=axis;
spread = ax(4)-ax(3);
ax(3)=ax(3)-.1*spread;
ax(4)=ax(4)+.1*spread;
axis(ax);
legend('Residual');
if dateflag
    datetick('x','keeplimits')
end
t2=title('Residual');
set(h2,'LineWidth',2)
set(s2,'LineWidth',2,'FontSize',12,'FontWeight','Bold')
set(t2,'FontSize',12,'FontWeight','Bold')
```