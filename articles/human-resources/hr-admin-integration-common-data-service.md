---
title: ตั้งค่าคอนฟิกการรวม Dataverse
description: บทความนี้อธิบายการรวมระหว่าง Microsoft Dataverse และ Dynamics 365 Human Resources
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fdc8d15138904336ce7e7b85fe286c815f0743f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869936"
---
# <a name="configure-dataverse-integration"></a>ตั้งค่าคอนฟิกการรวม Dataverse


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

คุณสามารถเปิดหรือปิดการรวม Microsoft Dataverse กับ Dynamics 365 Human Resources นอกจากนี้คุณยังสามารถดูรายละเอียดของการซิงโครไนส์ ลบข้อมูลการติดตาม และรีซิงค์ตารางเพื่อช่วยในการแก้ไขปัญหาข้อมูลระหว่างสภาพแวดล้อมของทั้งสองได้

> [!NOTE]
> หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการอัปเดต Dataverse (ซึ่งก่อนหน้านี้เรียกว่า Common Data Service) และการอัปเดตศัพท์ โปรดดูที่ [Microsoft Dataverse คืออะไร](/powerapps/maker/data-platform/data-platform-intro)

เมื่อคุณปิดการรวม ผู้ใช้สามารถทำการเปลี่ยนแปลงในทรัพยากรบุคคลหรือ Dataverse แต่การเปลี่ยนแปลงดังกล่าวจะไม่มีการซิงค์ระหว่างสภาพแวดล้อมทั้งสอง

ตามค่าเริ่มต้น การรวมข้อมูลระหว่างทรัพยากรบุคคลและ Dataverse จะถูกปิดไว้

คุณอาจต้องการปิดการรวมในสถานการณ์เหล่านี้:

- คุณกำลังกรอกข้อมูลโดยใช้กรอบงานการจัดการข้อมูลและต้องนำเข้าข้อมูลหลายครั้งเพื่อให้ได้รับเป็นสถานะที่ถูกต้อง

- แต่ก็ยังมีปัญหากับข้อมูลในทรัพยากรบุคคลหรือ Dataverse อย่างใดอย่างหนึ่ง ถ้าคุณปิดการรวมคุณสามารถลบเรกคอร์ดในสภาพแวดล้อมหนึ่งได้โดยไม่ต้องลบเรกคอร์ดนั้นออกจากเรกคอร์ดอื่น เมื่อคุณเปิดการรวมกลับขึ้นมา เรกคอร์ดในสภาพแวดล้อมที่ไม่มีการลบออกจะซิงค์กลับไปยังสภาพแวดล้อมที่มีการลบออก การซิงโครไนส์เริ่มต้นในครั้งถัดไปที่มีการรวม **Dataverse ที่พลาดการซิงค์** การร้องขอเรียกใช้ชุดงาน

> [!WARNING]
> เมื่อคุณปิดการรวมข้อมูลโปรดตรวจสอบให้แน่ใจว่าคุณไม่ได้แก้ไขเรกคอร์ดที่เหมือนกันในสภาพแวดล้อมทั้งสอง เมื่อคุณเปิดการรวมกลับขึ้นมา เรกคอร์ดที่คุณแก้ไขครั้งสุดท้ายจะถูกซิงค์ ดังนั้น ถ้าคุณไม่ได้ทำการเปลี่ยนแปลงที่เหมือนกันบนเรกคอร์ดในสภาพแวดล้อมทั้งสอง การสูญเสียข้อมูลอาจเกิดขึ้น

## <a name="access-the-dataverse-integration-page"></a>เข้าถึงหน้าการรวม Dataverse

1. ในอินสแตนซ์ทรัพยากรบุคคลซึ่งคุณต้องการดูหรือตั้งค่าคอนฟิกการตั้งค่าสำหรับการรวมกับ Dataverse เลือกไทล์ **การจัดการระบบ**

    [![ไทล์การจัดการระบบ](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. เลือกแท็บ **ลิงค์**

    [![แท็บลิงค์](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. ภายใต้ **การรวม** เลือก **การตั้งค่าคอนฟิก Dataverse**

    [![Dataverse ลิงค์การตั้งค่าคอนฟิก](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>เปิดหรือปิดการรวมข้อมูลระหว่างทรัพยากรบุคคลและ Dataverse

- เมื่อต้องการเปิดการรวมให้ตั้งค่าตัวเลือก **การเปิดใช้การรวม Dataverse** เป็น **ใช่** บนหน้า **การรวม Microsoft Dataverse**

    > [!NOTE]
    > เมื่อคุณเปิดการรวม ข้อมูลจะถูกซิงค์ในครั้งถัดไปที่การรวม **Dataverse พลาดการซิงค์** เรียกใช้ชุดงาน ข้อมูลทั้งหมดควรพร้อมใช้งานหลังจากชุดงานเสร็จสมบูรณ์

- เมื่อต้องการปิดใช้งานการรวมให้ตั้งตัวเลือกเป็น **ไม่**

[![การเปิดหรือปิด Dataverse](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> เราขอแนะนำให้ปิดการรวม Dataverse ในขณะที่ทำงานการย้ายข้อมูล การอัพโหลดข้อมูลขนาดใหญ่อาจส่งผลกระทบต่อประสิทธิภาพการทำงานได้อย่างมาก ตัวอย่างเช่นการอัพโหลดผู้ปฏิบัติงาน 2000 คน สามารถใช้เวลาหลายชั่วโมงเมื่อมีการเปิดใช้งานการรวม และน้อยกว่าหนึ่งชั่วโมงเมื่อปิดใช้งาน ตัวเลขที่ระบุในตัวอย่างนี้ใช้เพื่อวัตถุประสงค์ในการสาธิตเท่านั้น จำนวนเวลาที่ใช้ในการนำเข้าเรกคอร์ดมีความแตกต่างกันอย่างมากตามปัจจัยหลายอย่าง

## <a name="view-data-integration-details"></a>ภาพรวมของรายละเอียดการรวมข้อมูล

บนแท็บด่วน **การจัดการ** ของหน้า **การรวม Microsoft Dataverse** คุณสามารถดูวิธีการเชื่อมโยงแถวร่วมกันระหว่างทรัพยากรบุคคลและ Dataverse

- เมื่อต้องการดูแถวของตาราง ให้เลือกฟิลด์ **ตาราง Dataverse** กริดแสดงแถวทั้งหมดที่เชื่อมโยงกับตารางที่เลือก

> [!NOTE]
> ไม่ใช่ตาราง Dataverse ทั้งหมดที่แสดงอยู่ในปัจจุบัน เฉพาะตารางที่สนับสนุนการใช้ฟิลด์ที่กำหนดเองเท่านั้นที่จะปรากฏในกริด ตารางใหม่จะพร้อมใช้งานโดยผ่านการเผยแพร่ของทรัพยากรบุคคลอย่างต่อเนื่อง

กริดประกอบด้วยฟิลด์ต่อไปนี้:

- **ตาราง Dataverse** – ชื่อตารางใน Dataverse
- **การอ้างอิงตาราง Dataverse** – ตัวระบุที่ Dataverse ใช้ในการระบุเรกคอร์ด ค่านี้เทียบเท่ากับค่า **RecId** ของทรัพยากรบุคคล คุณสามารถค้นหาตัวระบุเมื่อคุณเปิดตาราง Dataverse ใน Microsoft Excel
- **ชื่อเอนทิตีทรัพยากรบุคคล** – เอนทิตี Human Resources ที่มีการซิงค์ข้อมูลครั้งล่าสุดกับ Dataverse เอนทิตี้สามารถมีคำนำหน้า Dataverse หรือคำนำหน้าอื่น
- **การอ้างอิงทรัพยากรบุคคล** – ค่า **RecId** ที่เชื่อมโยงกับเรกคอร์ดในทรัพยากรบุคคล
- **ลบออกจาก Dataverse แล้ว** – ค่าที่บ่งชี้ว่าแถวถูกลบออกจาก Dataverse หรือไม่

> [!NOTE]
> เรกคอร์ดในทรัพยากรบุคคลจะตรงกับแถวใน Dataverse

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>ลบการเชื่อมโยงของเรกคอร์ดในทรัพยากรบุคคลออกจากแถว Dataverse

ถ้าคุณประสบปัญหาในระหว่างการซิงโครไนส์ข้อมูลระหว่างทรัพยากรบุคคลและ Dataverse คุณอาจสามารถแก้ไขปัญหาเหล่านั้นได้ด้วยการล้างการติดตามและปล่อยให้ตารางการติดตามถูกรีซิงค์ ถ้าคุณลบการเชื่อมโยงออกแล้วเปลี่ยนหรือลบแถวใน Dataverse การเปลี่ยนแปลงจะไม่ถูกซิงค์กับทรัพยากรบุคคล ถ้าคุณทำการเปลี่ยนแปลงในทรัพยากรบุคคลเรกคอร์ดการติดตามใหม่จะถูกสร้างขึ้นและแถวจะถูกอัปเดตใน Dataverse

- เมื่อต้องการลบการเชื่อมโยงของเรกคอร์ดทรัพยากรบุคคลและแถว Dataverse เลือกตารางในฟิลด์ **ตาราง Dataverse** แล้วเลือก **ล้างข้อมูลการติดตาม**

[![การล้างข้อมูลการติดตาม](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

เมื่อต้องการเรียกใช้การซิงโครไนส์แบบสมบูรณ์บนตารางหลังจากที่คุณล้างการติดตามแล้วให้ดูที่กระบวนงานถัดไป

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>ซิงค์ตารางระหว่างทรัพยากรบุคคลและ Dataverse

ใช้ขั้นตอนนี้เมื่อ:

- การเปลี่ยนแปลงจาก Dataverse ใช้เวลานานเกินไปกว่าที่จะปรากฏในทรัพยากรบุคคล

- คุณต้องรีเฟรชตารางการติดตามหลังจากล้างการติดตาม

เมื่อต้องการเรียกใช้การซิงโครไนส์ทั้งหมดในตารางระหว่างทรัพยากรบุคคลและ Dataverse:

1. เลือกตารางในฟิลด์ **ตาราง Dataverse**

2. เลือก **ซิงค์เดี๋ยวนี้**

[![การเรียกใช้การซิงโครไนส์แบบสมบูรณ์](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[ตาราง Dataverse](hr-developer-entities.md)<br>
[ตั้งค่าคอนฟิกตารางเสมือน Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[คำถามที่ถามบ่อยเกี่ยวกับตารางเสมือน Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Microsoft Dataverse คืออะไร](/powerapps/maker/data-platform/data-platform-intro)<br>
[การอัปเดตศัพท์](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
