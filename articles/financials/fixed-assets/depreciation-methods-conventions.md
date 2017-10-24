---
title: "วิธีการคิดค่าเสื่อมราคาและแบบแผนการคิดค่าเสื่อมราคา"
description: "บทความนี้แสดงภาพรวมของแบบแผนการคิดค่าเสื่อมราคาและวิธีการคิดค่าเสื่อมราคาที่ได้รับการสนับสนุนโดย Microsoft Dynamics 365 for Finance and Operations, Enterprise edition"
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d802933f29b3e08704480035925b2fbf6743e996
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="depreciation-methods-and-conventions"></a>วิธีการคิดค่าเสื่อมราคาและแบบแผนการคิดค่าเสื่อมราคา

[!include[banner](../includes/banner.md)]


บทความนี้แสดงภาพรวมของแบบแผนการคิดค่าเสื่อมราคาและวิธีการคิดค่าเสื่อมราคาที่ได้รับการสนับสนุนโดย Microsoft Dynamics 365 for Finance and Operations, Enterprise edition

คุณสามารถเลือกวิธีการและแบบแผนการคิดค่าเสื่อมราคาต่างๆ ได้  วัตถุประสงค์ของวิธีคือเพื่อ ปันส่วนค่าเสื่อมราคาของสินทรัพย์ถาวรในรอบระยะเวลาทางบัญชี ค่าเสื่อมราคาของสินทรัพย์ถาวรคือ ราคาการซื้อสินทรัพย์ ลบด้วยมูลค่าซาก ถ้ามี 

ถ้าคุณกำลังใช้แบบแผนการคิดค่าเสื่อมราคา และคุณแก้ไขวันที่รันค่าเสื่อมราคาล่าสุดสำหรับสินทรัพย์ ซึ่งทำให้ค่าเสื่อมราคาบางค่าถูกข้ามไป ค่าเสื่อมราคาสำหรับปีที่แล้วอาจมากกว่า หรือน้อยกว่าที่คาดไว้ ค่าเสื่อมราคาถูกปรับปรุง โดยจำนวนรอบระยะเวลาการคิดค่าเสื่อมราคาที่ได้รับผลกระทบจากการปรับเปลี่ยนวันที่รันค่าเสื่อมราคาล่าสุด

ตัวอย่างเช่น ถ้าคุณกำลังใช้แบบแผนการคิดค่าเสื่อมราคาครึ่งปีในช่วงสามปี ค่าเสื่อมราคาโดยปกติเกิดขึ้นในช่วงเวลา 3 1/2 ปี ถ้าคุณเปลี่ยนวันที่รันค่าเสื่อมราคาล่าสุดในระหว่าง 3 1/2 ปี ปีที่แล้วของการคิดค่าเสื่อมราคาย้ายจำนวนรอบระยะเวลาที่ได้รับผลกระทบออกไป ถ้าคุณย้ายวันที่ไปสามเดือน ปีที่แล้วจะมีค่าเสื่อมราคามูลค่าเก้าเดือน โดยปกติจะเป็นค่าเสื่อมราคามูลค่าหกเดือน

คุณสามารถเลือกจากแบบแผนการคิดค่าเสื่อมราคาต่อไปนี้


-   ครึ่งปี
-   เต็มเดือน
-   กลางไตรมาส
-   กลางเดือน (วันที่ 1 ของเดือน)
-   กลางเดือน (วันที่ 15 ของเดือน)
-   ครึ่งปี (เริ่มต้นของปี)
-   ครึ่งปี (ปีหน้า)

คุณสามารถเลือกจากวิธีการคิดค่าเสื่อมราคาต่อไปนี้
-   อายุการใช้งานแบบเส้นตรง
-   ยอดดุลที่ลดลง
-   ธรรมดา
-   ตัวคูณ
-   ปริมาณการใช้
-   อายุการใช้งานคงเหลือแบบเส้นตรง
-   ยอดดุลที่ลดลง 200%
-   ยอดดุลที่ลดลง 175%
-   ยอดดุลที่ลดลง 150%
-   ยอดดุลที่ลดลง 125%

 



<a name="see-also"></a>ดูเพิ่มเติมที่
--------

[ค่าเสื่อมราคาของสินทรัพย์ถาวร](fixed-asset-depreciation.md)

[การคิดค่าเสื่อมราคาตามอายุการใช้งานแบบเส้นตรง](Straight-line-service-life-depreciation.md)

[การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง](reduce-balance-depreciation.md)

[การคิดค่าเสื่อมราคาด้วยตนเอง](manual-depreciation.md)

[การคิดค่าเสื่อมราคาตามอัตรา](factor-depreciation.md)

[การคิดค่าเสื่อมราคาตามปริมาณการใช้](consumption-depreciation.md)

[การคิดค่าเสื่อมราคาตามอายุการใช้งานคงเหลือแบบเส้นตรง](straight-line-life-remaining-depreciation.md)

[การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 125%](125-percent-reducing-balance-depreciation.md)

[ค่าเสื่อมราคายอดดุลที่ลดลง 150%](150-percent-reducing-balance-depreciation.md)

[การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 175%](175-percent-reducing-balance-depreciation.md)

[การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 200%](200-percent-reducing-balance-depreciation.md)




