---
title: "การรวม Microsoft Project client"
description: "การวางแผนและการรักษากำหนดการโครงการอาจซับซ้อน ดังนั้นผู้จัดการโครงการต้องใช้เครื่องมือที่ช่วยในการจัดการงานนี้ การรวมกับ Microsoft Project Client ให้การสนับสนุนในการเปิดและจัดการโครงสร้างการแบ่งงานของโครงการ"
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4a3445417d5ae88e2ff3676962a82921a7ab475d
ms.contentlocale: th-th
ms.lasthandoff: 03/26/2018

---

# <a name="microsoft-project-client-integration"></a>การรวม Microsoft Project client

[!include [banner](../includes/banner.md)]

การวางแผนและการรักษากำหนดการโครงการอาจซับซ้อน ดังนั้นผู้จัดการโครงการต้องใช้เครื่องมือที่ช่วยในการจัดการงานนี้ การรวมกับ Microsoft Project Client ให้การสนับสนุนในการเปิดและจัดการโครงสร้างการแบ่งงานของโครงการ ผู้จัดการโครงการสามารถประกาศการเปลี่ยนแปลงใดๆ กลับไปยังโครงสร้างการแบ่งงานของโครงการ Finance and Operations

> [!NOTE]
> ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations การอัพเดตเดือนกรกฎาคม 2017 คุณต้องติดตั้ง KB 4054797 และ 4055884

## <a name="configure-the-microsoft-project-client-add-in"></a>ตั้งค่าคอนฟิก add-in ของไคลเอนต์ Microsoft Project
ในการเปิดใช้งานการรวมกับ Microsoft Project Client จะต้องติดตั้ง add-in ของ Microsoft Dynamics 365 ในแอพลิเคชัน Microsoft Project ของไคลเอนต์ของผู้ใช้ ซึ่งทำได้โดยการเปิด **พื้นที่ทำงานการจัดการโครงการ**

•   คลิก **ตั้งค่าคอนฟิกadd-in ไคลเอนต์ของโครงการ** จากส่วน **ลิงค์** > **การตั้งค่า** ของพื้นที่ทำงาน

•   คลิก **เปิด** แล้วคลิก **รัน** เมื่อได้รับการพร้อมท์

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>เปิดและแก้ไขโครงสร้างการแบ่งงานแบบร่างที่มีอยู่ใน Microsoft Project Client
ถ้าโครงการใน Finance and Operations ได้สร้างโครงสร้างการแบ่งงานขึ้นแล้ว โครงสร้างการแบ่งงานสามารถถูกเปิดได้ในแอพลิเคชัน Microsoft Project Client ถ้าโครงสร้างการแบ่งงานอยู่ในสถานะร่าง เมื่อต้องการเปิดจากหน้า **โครงการ** คลิกลิงค์ **เปิดใน Microsoft Project** จากแท็บ **แผน** หน้านี้ยังสามารถเปิดได้จากภายในแอพลิเคชัน Microsoft Project Client โดยการคลิก **เปิด** ในแท็บ **Microsoft Dynamics 365** เลือก **นิติบุคคล** และ **โครงการ** จากรายการ

> [!NOTE]
> ถ้าคุณกำลังใช้ Internet Explorer เป็นเบราเซอร์ของคุณ คุณจะต้องคลิก **บันทึก** เพื่อเปิดจากตำแหน่งที่มีการดาวน์โหลดแฟ้มด้วยตนเอง หรือ คลิก **บันทึก และเปิด** เพื่อเปิดไฟล์ใน Microsoft Project Client ห้ามเปลี่ยนชื่อแฟ้ม เมื่อบันทึก

ก่อนที่จะทำการแก้ไขใดๆ ไปยังไฟล์โดยใช้ Microsoft Project Client คุณจำเป็นต้องตรวจสอบ คลิก **ตรวจสอบ** ในแท็บ **Microsoft Dynamics 365** นี่จะป้องกันไม่ให้ผู้ใช้คนอื่นแก้ไขโครงสร้างการแบ่งจากภายใน Finance and Operations ได้ในเวลาเดียวกัน ในการเผยแพร่โครงสร้างการแบ่งงานหลังจากเสร็จสิ้นการแก้ไขใดๆ คลิก **เช็คอิน** ในแท็บ **Microsoft Dynamics 365**

ถ้ามีการเพิ่มทีมโครงการกับโครงการไปยัง Finance and Operations เรียบร้อยแล้ว รายการทรัพยากรจะถูกเติมด้วยสมาชิกทีมงาน ถ้าทีมโครงการยังไม่ได้ถูกเพิ่มไปยังโครงการ คุณสามารถเลือกทรัพยากรและสร้างทีมงานภายใน Microsoft Project Client ได้โดยการคลิกที่ปุ่ม **ทรัพยากร** บนแท็บ **Microsoft Dynamics 365** ได้ 

ข้อมูลต่อไปนี้จะถูกซิงค์กลับไปยัง Finance and Operations โดยเป็นส่วนหนึ่งของกระบวนการเช็คอิน:

•   ชื่องาน

•   วันที่เริ่มต้น

•   วันที่เสร็จสิ้น

•   รายการก่อนหน้า

•   ชื่อทรัพยากร

•   ประเภท

•   ประเภททรัพยากร

•   ชั่วโมงทำงาน

•   บันทึก

•   ระดับความสำคัญ

> [!NOTE]
> ถ้าคุณเพิ่มคอลัมน์อื่นใดๆ ไปยังแฟ้ม Microsoft Project Client ของคุณ รายการเหล่านั้นจะไม่ถูกบันทึกในไฟล์ และจะไม่ถูกแสดงเมื่อมีการเปิดไฟล์อีกครั้ง

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>สร้างโครงสร้างการแบ่งงานสำหรับโครงการที่มีอยู่โดยใช้ Microsoft Project Client
ในการสร้างโครงสร้างการแบ่งงานใหม่โดยใช้ Microsoft Project Client ให้ดำเนินการตามขั้นตอนเหล่านี้:


1.  เปิด Microsoft Project Client

2.  ในแท็บ **Microsoft Dynamics 365** คลิก **เปิด**

3.  เลือก **นิติบุคคล** สำหรับโครงการ

4.  เลือก **โครงการ**

5.  คลิก **ตรวจสอบ** บนแท็บ **Microsoft Dynamics 365**

6.  เมื่อพร้อมที่จะเผยแพร่ไปยัง Finance and Operations คลิก **เช็คอิน** บนแท็บ **Microsoft Dynamics 365**

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>แทนที่โครงสร้างการแบ่งงานที่มีอยู่สำหรับโครงการที่มีอยู่โดยใช้ Microsoft Project Client
ในการสร้างโครงสร้างการแบ่งงานใหม่โดยใช้ Microsoft Project Client และแทนที่โครงสร้างการแบ่งงานที่มีอยู่สำหรับโครงการที่มีอยู่ ให้ทำตามขั้นตอนเหล่านี้:

1.  เปิด Microsoft Project Client

2.  สร้างกำหนดการใน Microsoft Project Client

3.  บนแท็บ **Microsoft Dynamics 365** คลิก **บันทึกการเปลี่ยนแปลง** > **แทนที่โครงการที่มีอยู่**

4.  เลือก **นิติบุคคล** สำหรับโครงการ

5.  เลือก **โครงการ**

6.  คลิก **ตกลง** 

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>สร้างโครงการใหม่จากภายใน Microsoft Project Client


1.  เปิด Microsoft Project Client

2.  สร้างกำหนดการใน Microsoft Project Client

3.  บนแท็บ **Microsoft Dynamics 365** คลิก **บันทึกการเปลี่ยนแปลง** > **บันทึกไปยังโครงการใหม่**

4.  เลือก **นิติบุคคล** สำหรับโครงการ

5.  ป้อน **รหัสโครงการ** ถ้าจำเป็น

6.  ป้อน **ชื่อโครงการ**

7.  เลือก **ชนิดโครงการ** **กลุ่มโครงการ** และ **รหัสสัญญาโครงการ** อีกทางหนึ่งคือ คุณสามารถสร้างสัญญาโครงการใหม่ได้ โดยการคลิก **สร้าง**

8.  เลือก **ปฏิทิน** ที่จะใช้สำหรับการจัดหาทรัพยากร

11. คลิก **ตกลง** 

