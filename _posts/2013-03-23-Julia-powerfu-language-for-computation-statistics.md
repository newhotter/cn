---
layout: post
title: Julia,强大的科学计算与统计语言
categories:
- Julia
- Statistics
tags:
- Julia
- R
- Python
- 统计
- Matlab
---

   [Julia](http://www.julialang.org)是2012年新推出来的一种用来进行科学计算与统计的语言，国外目前对Julia普遍看好。据说，Julia推出来的动机就是提供一种能够同时替代Matlab、R、Python的解决办法。

> We want a language that’s open source, with a liberal license. We want the speed of C with the dynamism of Ruby. We want a language that’s homoiconic, with true macros like Lisp, but with obvious, familiar mathematical notation like Matlab. We want something as usable for general programming as Python, as easy for statistics as R, as natural for string processing as Perl, as powerful for linear algebra as Matlab, as good at gluing programs together as the shell. Something that is dirt simple to learn, yet keeps the most serious hackers happy. We want it interactive and we want it compiled.
> 
> (Did we mention it should be as fast as C?)

Julia目前的发展速度惊人，已经出现了各式各样的packages。

这里是一张主流语言和程序的运算速度对比： 

$$$$

$$

<table>

<thead>

<tr><td></td><th class="system">Fortran</th><th class="system">Julia</th><th class="system">Python</th><th class="system">R</th><th class="system">Matlab</th><th class="system">Octave</th><th class="system">Mathematica</th><th class="system">JavaScript</th><th class="system">Go</th></tr>

</thead>

<thead>

<tr><td></td><td class="version">gcc 4.8.1

</td><td class="version">0.2</td><td class="version">2.7.3

</td><td class="version">3.0.2

</td><td class="version">R2012a

</td><td class="version">3.6.4

</td><td class="version">8.0

</td><td class="version">V8 3.7.12.22

</td><td class="version">go1

</td></tr>

</thead>

<tbody>

<tr><th>fib</th><td class="data">0.26</td><td class="data">0.91</td><td class="data">30.37</td><td class="data">411.36</td><td class="data">1992.00</td><td class="data">3211.81</td><td class="data">64.46</td><td class="data">2.18</td><td class="data">1.03</td></tr>

<tr><th>parse_int</th><td class="data">5.03</td><td class="data">1.60</td><td class="data">13.95</td><td class="data">59.40</td><td class="data">1463.16</td><td class="data">7109.85</td><td class="data">29.54</td><td class="data">2.43</td><td class="data">4.79</td></tr>

<tr><th>quicksort</th><td class="data">1.11</td><td class="data">1.14</td><td class="data">31.98</td><td class="data">524.29</td><td class="data">101.84</td><td class="data">1132.04</td><td class="data">35.74</td><td class="data">3.51</td><td class="data">1.25</td></tr>

<tr><th>mandel</th><td class="data">0.86</td><td class="data">0.85</td><td class="data">14.19</td><td class="data">106.97</td><td class="data">64.58</td><td class="data">316.95</td><td class="data">6.07</td><td class="data">3.49</td><td class="data">2.36</td></tr>

<tr><th>pi_sum</th><td class="data">0.80</td><td class="data">1.00</td><td class="data">16.33</td><td class="data">15.42</td><td class="data">1.29</td><td class="data">237.41</td><td class="data">1.32</td><td class="data">0.84</td><td class="data">1.41</td></tr>

<tr><th>rand_mat_stat</th><td class="data">0.64</td><td class="data">1.66</td><td class="data">13.52</td><td class="data">10.84</td><td class="data">6.61</td><td class="data">14.98</td><td class="data">4.52</td><td class="data">3.28</td><td class="data">8.12</td></tr>

<tr><th>rand_mat_mul</th><td class="data">0.96</td><td class="data">1.01</td><td class="data">3.41</td><td class="data">3.98</td><td class="data">1.10</td><td class="data">3.41</td><td class="data">1.16</td><td class="data">14.60</td><td class="data">8.51</td></tr>

</tbody>

</table>