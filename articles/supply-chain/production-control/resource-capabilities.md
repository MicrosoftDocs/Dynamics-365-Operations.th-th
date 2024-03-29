---
title: ความสามารถของทรัพยากร
description: บทความนี้ให้ข้อมูลเกี่ยวกับความสามารถของทรัพยากร ความสามารถที่เป็นความสามารถของทรัพยากรการดำเนินงานที่ดำเนินกิจกรรมเฉพาะ บทความอธิบายถึงความสามารถและแนวคิดที่เกี่ยวข้อง เช่นระดับแคล่วและระดับความสำคัญ และความสามารถในการใช้เพื่อเลือกทรัพยากรที่เหมาะสมสำหรับกิจกรรม
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrCapability, WrkCtrTable, WrkCtrCapRes, WrkCtrApplicableResources
audience: Application User
ms.reviewer: kamaybac
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 260537767d083445aa908c850526a5472c529763
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572780"
---
# <a name="resource-capabilities"></a>ความสามารถของทรัพยากร

[!include [banner](../includes/banner.md)]

บทความนี้ให้ข้อมูลเกี่ยวกับความสามารถของทรัพยากร ความสามารถที่เป็นความสามารถของทรัพยากรการดำเนินงานที่ดำเนินกิจกรรมเฉพาะ บทความอธิบายถึงความสามารถและแนวคิดที่เกี่ยวข้อง เช่นระดับแคล่วและระดับความสำคัญ และความสามารถในการใช้เพื่อเลือกทรัพยากรที่เหมาะสมสำหรับกิจกรรม

ความสามารถคือ ความสามารถของทรัพยากรการดำเนินงานในการดำเนินการกิจกรรมที่เฉพาะ  ทรัพยากรการดำเนินงานสามารถมีมากกว่าหนึ่งความสามารถถูกกำหนดไว้ และความสามารถสามารถถูกกำหนดให้มากกว่าหนึ่งทรัพยากร คุณสามารถกำหนดความสามารถให้กับทรัพยากรอย่างชั่วคราว โดยกำหนดวันเริ่มต้นและวันหมดอายุในการกำหนดความสามารถ เมื่อความสามารถของทรัพยากรหมดอายุ ทรัพยากรไม่สามารถถูกจัดตารางสำหรับโครงการหรือการผลิตที่ต้องการความสามารถนั้นได้ ความสามารถที่หมดอายุไปแล้วสามารถต่ออายุได้ คุณสามารถลบความสามารถที่จัดเตรียมไว้ โดยไม่เกี่ยวกับความสัมพันธ์ของกระบวนการผลิต หรือส่วนหนึ่งของกระบวนการผลิตของใบสั่งผลิตที่ใช้งานอยู่ โดยทั่วไป ต้องระวังเมื่อคุณลบความสามารถ เพื่อทดแทน ให้พิจารณาการปรับปรุงวันหมดอายุของทรัพยากรที่มีความสามารถ ความสามารถสามารถถูกกำหนดให้กับทรัพยากรทุกชนิด: เครื่องมือ ผู้จัดจำหน่าย เครื่องจักร สถานที่ สิ่งอำนวยความสะดวก หรือทรัพยากรบุคคล

## <a name="level"></a>ระดับ
หลาย ๆ ทรัพยากรมักมีความสามารถในการทำงานเดียวกัน แต่ในระดับของความชำนาญแตกต่างกัน (ตัวอย่างเช่น ความแข็งแรง ความเร็วในการประมวลผล หรือความถูกต้อง) ดังนั้น เมื่อคุณกำหนดความสามารถให้กับทรัพยากร คุณสามารถระบุการค่า **ระดับ** ได้ ระดับมีค่าทางตัวเลขอย่างง่าย ถ้าคุณระบุว่าความสามารถใดเป็นความต้องการทรัพยากรสำหรับกระบวนการผลิต คุณยังสามารถระบุค่า **ระดับต่ำสุดที่จำเป็น** สำหรับความสามารถได้ จากนั้นกลไกจัดการการจัดกำหนดการจะเลือกเฉพาะทรัพยากรที่มีความสามารถที่ต้องการในระดับที่เท่ากับ หรือเกินกว่าระดับต่ำสุดที่ระบุในความต้องการทรัพยากรที่ถูกระบุในความต้องการทรัพยากร

## <a name="priority"></a>ระดับความสำคัญ
ทรัพยากรการดำเนินงานที่มีความสามารถเดียวกันสามารถถูกกำหนดระดับความสำคัญได้ จากนั้น ถ้าหลาย ๆ ทรัพยากรมีความสามารถที่ตอบสนองความต้องการจัดกำหนดการในระดับที่ต้องการ และมีกำลังการผลิตที่ว่าง กลไกการจัดกำหนดการสามารถเลือกจากทรัพยากรดังกล่าวได้ ถ้า **ระดับความสำคัญ** ถูกเลือกไว้ในฟิลด์ **การเลือกทรัพยากรหลัก** ในหน้า **พารามิเตอร์การจัดกำหนดการ** ทรัพยากรที่มีระดับความสำคัญสูงสุด (เป็นค่าทางตัวเลขต่ำสุดในฟิลด์ **ระดับความสำคัญ** ) จะถูกเลือกเป็นลำดับแรกในระหว่างการจัดกำหนดการ

## <a name="resource-requirements"></a>ความต้องการทรัพยากร
เมื่อคุณกำหนดความต้องการทรัพยากรสำหรับกระบวนการผลิต คุณสามารถระบุความสามารถหนึ่งรายการหรือมากกว่าเป็นความต้องการ ในระหว่างการจัดกำหนดการการผลิต ความสามารถที่ถูกกำหนดในความต้องการทรัพยากรในขั้นตอนของกระบวนการผลิตจะ ถูกจับคู่กับความสามารถที่ถูกกำหนดสำหรับทรัพยากร ทรัพยากรที่มีความสามารถที่ตอบสนองความต้องการจะถูกเลือก ถ้าหลาย ๆ ทรัพยากรมีความสามารถในการทำงานเดียวกันแต่ความชำนาญแตกต่างกัน (เช่น ความแข็งแรง ความเร็วในการประมวลผล หรือความถูกต้อง) คุณสามารถกำหนดหลาย ๆ ความสามารถหรือใช้ระดับความสามารถ อย่างใดอย่างหนึ่ง เพื่อคัดเลือกความสามารถของทรัพยากรได้ ดังตัวอย่างต่อไปนี้

-   ในกระบวนการผลิต เวลาของกระบวนการดูรายละเอียดถูกตั้งค่าเป็น 10 หน่วยต่อชั่วโมง แต่ความต้องเองถูกกำหนดเป็น ดูรายละเอียด
-   คุณมีเครื่องจักรสองเครื่องสำหรับดูรายละเอียด M1 และ M2
-   ความสามารถในการดูรายละเอียดถูกกำหนดให้ทั้งสองทรัพยากร เครื่องจักร M1 และ เครื่องจักร M2
-   เครื่องจักร M1 สามารถดูรายละเอียดสองหน่วยต่อชั่วโมง และเครื่องจักร M2 สามารถดูรายละเอียด 11 หน่วยต่อชั่วโมง

ในตัวอย่างนี้ ทั้งสองเครื่องจักรสามารถถูกเลือกโดยกลไกจัดการการจัดกำหนดการ เนื่องจากทั้งสองตอบสนองความต้องการความสามารถพื้นฐาน (การดูรายละเอียด) อย่างไรก็ตาม เครื่องจักร M1 เครื่องสามารถดูรายละเอียดเพียงสองหน่วยต่อชั่วโมง เนื่องจากอัตรานี้น้อยกว่า 10 หน่วยต่อชั่วโมงที่ระบุไว้ในกระบวนการผลิตมาก เครื่องจักร M1 จะทำให้เกิดปัญหาการผลิตถ้าถูกเลือก มีสองวิธีในการแก้ไขปัญหานี้และตรวจสอบให้แน่ใจว่าเครื่องจักร M2 ถูกเลือกแทน:

-   สร้างสองความสามารถแยกต่างหาก: การดูรายละเอียดความเร็วต่ำและการดูรายละเอียดความเร็วสูง กำหนดการดูรายละเอียดความเร็วต่ำเป็นการดูรายละเอียดที่มีระยะเวลากระบวนการหนึ่งถึงเก้าหน่วยต่อชั่วโมง กำหนดการดูรายละเอียดความเร็วต่ำเป็นการดูรายละเอียดที่มีระยะเวลากระบวนการ 10 ถึง 19 หน่วยต่อชั่วโมง จากนั้นกำหนดความสามารถในการดูรายละเอียดความเร็วต่ำให้กับเครื่องจักร M1 และกำหนดความสามารถในการดูรายละเอียดความเร็วสูงให้กับเครื่องจักร M2 ในตอนท้าย เปลี่ยนความต้องการความสามารถของทรัพยากรในกระบวนการผลิตเป็นการดูรายละเอียดความเร็วสูง จากนั้นกลไกจัดการการจัดกำหนดการจะเลือกเครื่องจักรที่ถูกต้อง (M2)
-   ใช้ระดับความสามารถในการคัดเลือกความสามารถในการดูรายละเอียดที่ถูกกำหนดให้กับเครื่องจักรสำหรับดูรายละเอียด ระบุว่าเครื่องจักร M1 มีความสามารถในการดูรายละเอียดที่ระดับ 2.0 และเครื่องจักร M2 มีความสามารถในการดูรายละเอียดที่ระดับ 11.0 จากนั้นระบุว่า 10.0 เป็นระดับต่ำสุดที่จำเป็นสำหรับความสามารถในการดูรายละเอียดในกระบวนการผลิต จากนั้นกลไกจัดการการจัดกำหนดการจะกำหนดว่าเครื่องจักร M2 เท่านั้นที่ตอบสนองความต้องการทรัพยากร

## <a name="competencies-for-human-resources"></a>ความสามารถของทรัพยากรบุคคล
เมื่อคุณมีทรัพยากรการดำเนินงานประเภท **ทรัพยากรบุคคล** ที่ถูกเชื่อมโยงกับผู้ปฏิบัติงานในฝ่ายทรัพยากรบุคคล คุณสามารถใช้ประโยชน์จากความสามารถของผู้ปฏิบัติงานด้วยเช่นกันเมื่อคุณกำหนดความต้องการทรัพยากรสำหรับกระบวนการผลิต กล่าวคือ คุณยังสามารถระบุความต้องการสำหรับทักษะเฉพาะ หลักสูตร ใบรับรอง หรือตำแหน่งได้ด้วยเช่นกัน จากนั้นกลไกจัดการการจัดกำหนดการสามารถเลือกทรัพยากรที่จะถูกเชื่อมโยงกับผู้ปฏิบัติงาน และการเลือกจะขึ้นอยู่กับความสามารถของผู้ปฏิบัติงานเหล่านั้น ความสามารถนั้นจะถูกตั้งค่าใน ทรัพยากรบุคคล ไม่ใช่ในหน้า **ความสามารถของทรัพยากร** เมื่อคุณกำหนดทักษะ หลักสูตร ใบรับรอง หรือตำแหน่งเป็นความต้องการทรัพยากร คุณต้องใช้ฟังก์ชันทรัพยากรบุคคล และเชื่อมแต่ละทรัพยากรในประเภท **ทรัพยากรบุคคล** ไปยังผู้ปฏิบัติงานที่สอดคล้องกัน ถ้าคุณไม่ได้ใช้งานฟังก์ชันทรัพยากรบุคคล คุณสามารถกำหนดความสามารถในหน้า **ความสามารถของทรัพยากร** ที่คล้ายหรือซ้ำกับความสามารถจากทรัพยากรบุคคลได้ อย่างไรก็ตาม หน้า **ความสามารถของทรัพยากร** จะไม่ประกอบด้วยฟังก์ชันที่ต้องใช้เพื่อรักษาทักษะ หลักสูตร ใบรับรอง หรือตำแหน่ง





[!INCLUDE[footer-include](../../includes/footer-banner.md)]