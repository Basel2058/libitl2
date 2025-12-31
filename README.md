Arabic is Below: 

libitl2: A library for Islamic calendar and prayer times
========================================================

`libitl2` is a fork from
[libitl](http://projects.arabeyes.org/project.php?proj=ITL). This fork aims
initially to:
* Move the code from the SVN SCM to git SCM
* Modernize the build system by moving it from `autotools` to `cmake`
* Do static analysis on the existing code and fix the found bugs
* Make the library cross-platform (i.e., runs natively on Unix/Linux, 
   Mac, and Windows)

Compiling
---------
In order to compile the library, you will need the following tools:
* A modern C compiler (e.g., GCC or Clang). Building the library has been tested
with GCC 4.8.1
* `cmake` (Tested with 2.8.11.2)

To compile the library and the demo programs, perform the followig 
commands in the `itl2` directory:

```shell
mkdir build
cd build
cmake ..
make
./demo_prayer # To run the prayer demo program
```

Static Analysis
---------------
We are using `ccc-analyzer` from Clang to perform the static analysis.
To use `ccc-analyzer`, you need to perform the follwoing:
```shell
cmake -DCMAKE_C_COMPILER=/usr/share/clang/scan-build/ccc-analyzer ..
/usr/share/clang/scan-build/scan-build make
```
It is important to note that Clang might be installed on different directories 
on different machines.

LICENSE
-------
The original `libitl` uses LGPL license shown in [LICENSE](LICENSE). `libitl2`
uses the same license as `libitl`.

AUTHORS
-------
The original authors of `libitl` can be found in [AUTHORS](AUTHORS). `libitl2`
is developed and maintained currently by Mohamed A. Bamakhrama.


______________________________

libitl2: مكتبة للتقويم الإسلامي ومواقيت الصلاة

libitl2 هي تفرّع (Fork) من
libitl. يهدف هذا التفرّع في بدايته إلى:
	•	نقل الشفرة المصدرية من نظام إدارة الإصدارات SVN إلى نظام Git
	•	تحديث نظام البناء بنقله من autotools إلى cmake
	•	إجراء تحليل ساكن (Static Analysis) على الشفرة الحالية وإصلاح الأخطاء المكتشفة
	•	جعل المكتبة متعددة المنصات (أي تعمل أصليًا على أنظمة Unix/Linux وMac وWindows)

التجميع (Compiling)

⸻

لتجميع المكتبة، ستحتاج إلى الأدوات التالية:
	•	مُصرّف C حديث (مثل GCC أو Clang). تم اختبار بناء المكتبة باستخدام GCC 4.8.1
	•	أداة cmake (تم اختبارها بالإصدار 2.8.11.2)

لتجميع المكتبة وبرامج العرض التجريبية، نفّذ الأوامر التالية في مجلد itl2:

mkdir build
cd build
cmake ..
make
./demo_prayer # لتشغيل البرنامج التجريبي لمواقيت الصلاة

التحليل الساكن (Static Analysis)

⸻

نستخدم أداة ccc-analyzer من Clang لإجراء التحليل الساكن. لاستخدام ccc-analyzer، يجب تنفيذ ما يلي:

cmake -DCMAKE_C_COMPILER=/usr/share/clang/scan-build/ccc-analyzer ..
/usr/share/clang/scan-build/scan-build make

من المهم ملاحظة أن Clang قد يكون مُثبّتًا في مسارات مختلفة على أجهزة مختلفة.

الرخصة (LICENSE)

⸻

تستخدم مكتبة libitl الأصلية رخصة LGPL الموضّحة في ملف LICENSE.
وتستخدم libitl2 الرخصة نفسها المستخدمة في libitl.

المؤلفون (AUTHORS)

⸻

يمكن العثور على المؤلفين الأصليين لـ libitl في ملف AUTHORS.
أما libitl2 فيتم تطويرها وصيانتها حاليًا بواسطة محمد أ. بامخرمة.


