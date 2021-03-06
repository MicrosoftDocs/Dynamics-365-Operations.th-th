---
title: กำหนดความสามารถของทรัพยากร
description: ความสามารถของทรัพยากรอธิบายสิ่งที่ทรัพยากรการดำเนินงานสามารถทำได้
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93b30cbe660d224f0a92f4e412d2b1ba33af3f9b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977849"
---
# <a name="define-resource-capabilities"></a>กำหนดความสามารถของทรัพยากร

[!include [banner](../../includes/banner.md)]

ความสามารถของทรัพยากรอธิบายสิ่งที่ทรัพยากรการดำเนินงานสามารถทำได้ ในระหว่างการวางแผน ความต้องการของแต่ละงานและการดำเนินงานจะถูกจับคู่กับความสามารถของทรัพยากรที่พร้อมใช้งาน คู่มืองานนี้จะช่วยคุณสร้างความสามารถทรัพยากรและกำหนดให้กับทรัพยากร  ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF


## <a name="create-a-resource-capability"></a>สร้างความสามารถของทรัพยากร
1. ไปที่ความสามารถของทรัพยากร
2. คลิก สร้าง
3. ในฟิลด์ความสามารถ ให้พิมพ์รหัสของความสามารถของทรัพยากร
    * สำหรับการดำเนินงานที่ได้รับมอบหมาย คุณสามารถใช้รหัสความสามารถเพื่อระบุว่าทรัพยากรต้องมีความสามารถนี้เพื่อดำเนินการ  
4. ในฟิลด์คำอธิบาย ให้ป้อนคำอธิบายของความสามารถ

## <a name="assign-capability-to-a-resource"></a>กำหนดความสามารถให้กับทรัพยากร
1. คลิก เพิ่ม
2. ในฟิลด์ทรัพยากร ให้พิมพ์รหัสของทรัพยากร
    * ความสามารถของทรัพยากรสามารถถูกกำหนดให้กับทรัพยากรอีกหนึ่งรายการหรือมากกว่า  
3. ในฟิลด์การหมดอายุ ให้ป้อนวันที่
    * คุณสามารถใช้ฟิลด์นี้เพื่อระบุว่าทรัพยากรมีความสามารถสำหรับเฉพาะเวลาที่จำกัดเท่านั้น  
4. ในฟิลด์ระดับความสำคัญ ให้ป้อนตัวเลข
    * เมื่อคุณจัดกำหนดการงานและการดำเนินงาน คุณสามารถระบุว่าจะเลือกทรัพยากรตามระดับความสำคัญหรือไม่  ถ้าคุณเลือกที่จะดำเนินการนี้ และทรัพยากรมากกว่าหนึ่งสามารถทำงานหรือการดำเนินงานโดยเรียงตามวันร้องขอ จะมีการเลือกทรัพยากรที่มีระดับความสำคัญต่ำสุดที่เกี่ยวข้องกับความสามารถที่ต้องการ  
5. ในฟิลด์ระดับ ให้ป้อนตัวเลข
    * เมื่อคุณระบุว่างานหรือการดำเนินงานต้องการความสามารถเฉพาะ คุณยังสามารถระบุระดับต่ำสุดที่ต้องการได้อีกด้วย  ใช้ระดับความสามารถเพื่อแยกความแตกต่างของทรัพยากรที่สามารถทำงานเดียวกันได้ แต่ที่ความเร็ว จุดแข็ง ขนาด และอื่นๆ ที่แตกต่างกัน  

