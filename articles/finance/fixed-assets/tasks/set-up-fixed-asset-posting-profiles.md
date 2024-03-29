---
title: ตั้งค่าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร
description: กระบวนงานนี้แสดงวิธีการตั้งค่าโพรไฟล์การลงบัญชีสินทรัพย์ถาวร
author: moaamer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be8001428cf2df111458fddd0ecbcdae0daf9b25
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863085"
---
# <a name="set-up-fixed-asset-posting-profiles"></a>ตั้งค่าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการตั้งค่าโพรไฟล์การลงบัญชีสินทรัพย์ถาวร ตัวอย่างที่ให้ไว้ในบทความคือโพรไฟล์การลงรายการบัญชีพื้นฐาน อย่างไรก็ตาม ต้องมีการสร้างการลงโพรไฟล์สำหรับแผนภูมิบัญชีที่เฉพาะเจาะจงและข้อกำหนดการรายงานทางการเงิน

1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล > สินทรัพย์ถาวร > การตั้งค่า > โพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร**
2. คลิก **สร้าง**
3. ในฟิลด์ **โพรไฟล์การลงรายการบัญชี** ให้พิมพ์ค่า
4. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง คุณจะต้องสร้างโพรไฟล์การลงรายการบัญชีสำหรับธุรกรรมสินทรัพย์ถาวรแต่ละชนิดที่คุณต้องใช้เมื่อทำงานกับสินทรัพย์ถาวร  คู่มือของงานนี้จะเริ่มด้วยธุรกรรมการซื้อสินทรัพย์  
5. ในแถบเครื่องมือ คลิก **เพิ่ม**
6. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า ฟิลด์ **การจัดกลุ่ม** ช่วยให้คุณสามารถกำหนดโพรไฟล์การลงรายการบัญชีไปยังตาราง (การตั้งค่าบัญชีหนึ่งรายการสำหรับสินทรัพย์ถาวรแต่ละรายการ) หรือกลุ่ม (การตั้งค่าบัญชีหนึ่งรายการสำหรับสินทรัพย์ถาวรแต่ละรายการ) สำหรับคู่มืองานนี้ ปล่อยให้มีการตั้งค่าเป็น "ทั้งหมด" เพื่อนำไปใช้กับสินทรัพย์ถาวรทั้งหมดที่มีสมุดบัญชีที่ระบุ  
7. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ สำหรับการซื้อสินทรัพย์ คุณสามารถป้อนบัญชีตรงข้าม หรือปล่อยให้ว่างเพื่อให้มีการกรอกข้อมูลสำหรับธุรกรรมเฉพาะ    
8. ในเมนูแบบหล่นลงภายใต้ fastTab **บัญชีแยกประเภท** ให้เลือก 'การปรับปรุงการซื้อสินทรัพย์' สำหรับธุรกรรมการปรับปรุงการซื้อสินทรัพย์ เราจะใช้บัญชีเดียวกันกับที่ใช้สำหรับธุรกรรมการซื้อสิ้นทรัพย์  
9. คลิก **เพิ่ม**
10. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
11. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ สำหรับการปรับปรุงการซื้อสินทรัพย์ คุณสามารถป้อนบัญชีตรงข้ามหรือปล่อยให้ว่างเพื่อให้มีการกรอกข้อมูลสำหรับธุรกรรมเฉพาะ    
12. ในเมนูแบบหล่นลงภายใต้ fastTab **บัญชีแยกประเภท** เลือก 'ค่าเสื่อมราคา'
13. คลิก **เพิ่ม**
14. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
15. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
16. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
17. ในเมนูแบบหล่นลงภายใต้ fastTab **บัญชีแยกประเภท** ให้เลือก 'การปรับปรุงค่าเสื่อมราคา' สำหรับธุรกรรมการปรับปรุงค่าเสื่อมราคา เราจะใช้บัญชีเดียวกันกับที่ใช้สำหรับธุรกรรมค่าเสื่อมราคา  
18. คลิก **เพิ่ม**
19. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
20. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
21. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
22. ในเมนูแบบหล่นลงภายใต้ fastTab **บัญชีแยกประเภท** เลือก 'การตัดจำหน่าย - การขาย'
23. คลิก **เพิ่ม**
24. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
25. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ สำหรับการตัดจำหน่าย คุณสามารถป้อนบัญชีตรงข้ามหรือปล่อยให้ว่างเพื่อให้มีการกรอกข้อมูลสำหรับธุรกรรมเฉพาะ  
26. ในเมนูแบบหล่นลงภายใต้ fastTab **บัญชีแยกประเภท** เลือก 'การตัดจำหน่าย - เศษซาก' ใช้บัญชีเดียวกันสำหรับ 'การขายการตัดจำหน่าย' และ 'เศษซากการตัดจำหน่าย'  
27. คลิก **เพิ่ม**
28. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
29. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ สำหรับการตัดจำหน่าย คุณสามารถป้อนบัญชีตรงข้ามหรือปล่อยให้ว่างเพื่อให้มีการกรอกข้อมูลสำหรับธุรกรรมเฉพาะ  
30. ขยาย fastTab **การตัดจำหน่าย** คุณต้องตั้งค่าโพรไฟล์การลงรายการบัญชีการตัดจำหน่าย สำหรับทั้งการขายและเศษซาก  เราจะเริ่มต้นด้วยธุรกรรมการตัดจำหน่าย  
31. คลิก **เพิ่ม**
32. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
33. ในฟิลด์ **ลงรายการบัญชีค่า** เลือก 'ค่าการซื้อสินทรัพย์'
    * มูลค่าการซื้อสินทรัพย์จะระบุค่าการซื้อสินทรัพย์และการปรับปรุงการซื้อสินทรัพย์สำหรับทั้งปี  นอกจากนี้คุณยังสามารถกำหนดบัญชีสำหรับชนิดธุรกรรมเหล่านี้แยกต่างหาก  
    * คุณสามารถตั้งค่ากระบวนการตัดจำหน่ายให้ใช้บัญชีที่แตกต่างกัน โดยขึ้นอยู่กับว่าผลการตัดจำหน่ายเป็นกำไรหรือขาดทุน  ฉันจะตั้งค่าชนิดมูลค่าการขายเป็น "ทั้งหมด" เพื่อใช้บัญชีเดียวกันสำหรับการตัดจำหน่ายทุกชนิด  
34. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
35. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
36. คลิก **เพิ่ม**
37. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
38. ในฟิลด์ **ลงรายการบัญชีค่า** เลือก 'ค่าเสื่อมราคา (ปีก่อนหน้านี้)'  
38. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
39. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
40. คลิก **เพิ่ม**
41. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
42. ในฟิลด์ **ลงรายการบัญชีค่า** เลือก 'ค่าเสื่อมราคา (ปีนี้)'
43. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
44. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
45. คลิก **เพิ่ม**
46. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
47. ในฟิลด์ **ลงรายการบัญชีค่า** เลือก 'ค่าเสื่อมราคา (ปีก่อนหน้านี้)'
48. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
49. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
50. คลิก **เพิ่ม**
51. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
52. ในฟิลด์ **ลงรายการบัญชีค่า** เลือก 'การปรับปรุงค่าเสื่อมราคา (ปีนี้)'
53. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
54. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
55. คลิก **เพิ่ม**
56. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
57. ในฟิลด์ **ลงรายการบัญชีค่า** เลือก 'มูลค่าตามบัญชีสุทธิ'
58. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
59. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
60. ในฟิลด์ **การขายหรือเศษซาก**  เลือก 'เศษซาก'
61. คลิก **เพิ่ม**
62. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
63. ในฟิลด์ **ลงรายการบัญชีค่า** เลือก 'ค่าการซื้อสินทรัพย์'
64. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
65. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
66. คลิก **เพิ่ม**
67. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
67. ในฟิลด์ **ลงรายการบัญชีค่า** เลือก 'ค่าเสื่อมราคา (ปีก่อนหน้านี้)'  
68. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
69. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
70. คลิก **เพิ่ม**
71. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
72. ในฟิลด์ **ลงรายการบัญชีค่า** เลือก 'ค่าเสื่อมราคา (ปีนี้)'
73. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
74. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
75. คลิก **เพิ่ม**
76. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
77. ในฟิลด์ **ลงรายการบัญชีค่า** เลือก 'ค่าเสื่อมราคา (ปีก่อนหน้านี้)'
78. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
79. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
80. คลิก **เพิ่ม**
81. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
82. ในฟิลด์ **ลงรายการบัญชีค่า** เลือก 'การปรับปรุงค่าเสื่อมราคา (ปีนี้)'
83. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
84. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
85. คลิก **เพิ่ม**
86. ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า
87. ในฟิลด์ **ลงรายการบัญชีค่า** เลือก 'มูลค่าตามบัญชีสุทธิ'
88. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
89. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
