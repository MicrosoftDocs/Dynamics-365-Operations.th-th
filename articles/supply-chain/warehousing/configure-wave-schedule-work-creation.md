---
title: จัดกำหนดการการสร้างงานในระหว่างเวฟ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าและใช้วิธีการประมวลผลเวฟการสร้างงานตามกำหนดการ
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078312"
---
# <a name="schedule-work-creation-during-wave"></a>จัดกำหนดการการสร้างงานในระหว่างเวฟ

[!include [banner](../includes/banner.md)]

ใช้คุณลักษณะ *การสร้างงานตามกำหนดการ* เนื่องจากเป็นส่วนหนึ่งของกระบวนการเวฟของคุณที่จะช่วยเพิ่มปริมาณที่สามารถประมวลผลเวฟได้ โดยการให้ระบบสร้างงานโดยใช้การประมวลผลแบบขนาน

เมื่อมีการเปิดใช้งานฟังก์ชัน งานที่วางแผนไว้จะถูกสร้างขึ้นโดยอัตโนมัติ ซึ่งระบบจะประมวลผลเพื่อสร้างงานจริงในที่สุด หากจํานวนของรายการจํานวนงานในศูนย์การผลิตของเวฟถึงขีดจำกัดที่กำหนดไว้ล่วงหน้า ระบบจะสร้างงานจริงอย่างรวดเร็วขึ้นโดยใช้การประมวลผลแบบขนานแบบอะซิงโครนัส

## <a name="enable-the-schedule-work-creation-feature"></a>เปิดใช้งานคุณลักษณะการสร้างงานตามกำหนดการ

### <a name="enable-the-feature-in-feature-management"></a>เปิดใช้งานคุณลักษณะในการจัดการคุณลักษณะ

ก่อนที่คุณจะสามารถใช้คุณลักษณะ *การสร้างงานตามกำหนดการ* คุณต้องเปิดใช้งานในระบบของคุณ ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:

- **โมดูล:** *การจัดการคลังสินค้า*
- **ชื่อคุณลักษณะ:** *การสร้างงานตามกำหนดการ*

> [!NOTE]
> ต้องเปิดใช้งานคุณลักษณะ *การบล็อคงานทั่วทั้งองค์กร* ก่อนที่คุณจะสามารถเปิดใช้งาน *การสร้างงานตามกำหนดการ*

### <a name="manually-enable-batch-processing-of-waves"></a>เปิดใช้งานการประมวลผลชุดงานของเวฟด้วยตนเอง

หากต้องการใช้ประโยชน์จากวิธีการแบบอะซิงโครนัสแบบขนานเพื่อสร้างงานของคลังสินค้า กระบวนการเวฟของคุณจะต้องรันอยู่ในชุดงาน เพื่อตั้งค่ารายการนี้:

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> พารามิเตอร์การจัดการคลังสินค้า**

1. บนแท็บ **ทั่วไป** ตั้งค่า **ประมวลผลเวฟในชุดงาน** เป็น *ใช่* หรือคุณยังสามารถเลือก **กลุ่มชุดงานการประมวลผลเวฟ** ที่จัดสรรไว้ เพื่อป้องกันไม่ให้การประมวลผลคิวชุดงานของคุณรันพร้อมกันกับกระบวนการอื่นๆ

1. ตั้งค่า **เวลารอการล็อค (ms)** ที่ใช้เมื่อระบบประมวลผลเวฟหลายเวฟในเวลาเดียวกัน สำหรับกระบวนการเวฟที่ใหญ่ที่สุด เราขอแนะนำค่า *60000*

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>เปิดใช้งานวิธีการขั้นตอนเวฟใหม่ด้วยตนเองจากเท็มเพลตเวฟที่มีอยู่

เริ่มต้นโดยการสร้างวิธีการขั้นตอนของเวฟใหม่และเปิดใช้งานวิธีการดังกล่าวเพื่อการประมวลผลงานแบบอะซิงโครนัสแบบขนาน

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> วิธีการประมวลผลเวฟ**

1. เลือก  **สร้างวิธีการใหม่** และโปรดทราบว่า *WHSScheduleWorkCreationWaveStepMethod* ถูกเพิ่มเข้าในรายการของวิธีการกระบวนการเวฟที่คุณสามารถใช้ในเท็มเพลตเวฟการจัดส่งของคุณแล้ว

1. เลือกเรกคอร์ดที่มี **ชื่อวิธีการ** *WHSScheduleWorkCreationWaveStepMethod* และเลือก **การตั้งค่าคอนฟิกงาน**

1. เพื่อเพิ่มแถวใหม่ไปยังกริด เลือก **สร้าง** ในบานหน้าต่างการดำเนินการ และใช้การตั้งค่าต่อไปนี้:

    - **คลังสินค้า** - เลือกคลังสินค้าที่คุณจะใช้จัดกำหนดการการประมวลผลการสร้างงาน

    - **จํานวนงานของชุดงานสูงสุด** - ระบุจํานวนงานของชุดงานสูงสุด ในกรณีส่วนใหญ่ ค่านี้ควรอยู่ในช่วงตั้งแต่ 8-16 อย่างไรก็ตาม ขอแนะนำว่าคุณควรลองใช้การตั้งค่าที่เหมาะสมตามสถานการณ์ของคุณ

    - **กลุ่มชุดงานการประมวลผลเวฟ** - เลือกกลุ่มชุดงานการประมวลผลเวฟที่จัดสรรไว้ เพื่อให้การประมวลผลคิวชุดงานของคุณมีประสิทธิภาพสูงสุด

ขณะนี้คุณพร้อมที่จะอัพเดตเท็มเพลตเวฟที่มีอยู่ (หรือสร้างเท็มเพลตใหม่) เพื่อใช้วิธีการประมวลผลเวฟ *การสร้างงานตามกำหนดการ*

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**

1. เลือก **แก้ไข** บนบานหน้าต่างการดำเนินการ

1. ในบานหน้าต่างรายการ ให้เลือกเท็มเพลตเวฟที่คุณต้องการอัพเดต (หากคุณทดสอบโดยใช้ข้อมูลสาธิต คุณสามารถใช้ *24 ค่าเริ่มต้นการจัดส่ง*)

1. ขยาย FastTab **วิธีการ** และเลือกแถวที่มี **ชื่อ** *การสร้างงานตามกำหนดการ* ในกริด **วิธีการที่เหลือ**

1. เลือกลูกศรที่ชี้ไปที่คอลัมน์ **วิธีการที่เลือก** เพื่อย้ายแถวที่เลือกไปที่คอลัมน์นั้น (คุณสามารถมีวิธีการเลือกได้เพียงหนึ่งวิธีเท่านั้นในแต่ละครั้งที่ใช้ *WHSScheduleWorkCreationWaveStepMethod* หรือ *createWork* ดังนั้น แถวที่มีอยู่ที่มี **ชื่อวิธีการ** *createWork* จะถูกย้ายไปยังกริด **วิธีการที่เหลือ** โดยอัตโนมัติ)

## <a name="set-wave-task-processing-threshold-data"></a>ตั้งค่าข้อมูลขีดจำกัดการประมวลผลงานเวฟ

ระบบจะสร้างข้อมูลขีดจำกัดการประมวลผลงานเวฟเริ่มต้นในครั้งแรกที่กระบวนการเวฟรัน โดยใช้การประมวลผลตามงานใดๆ ข้อมูลจะถูกใช้ในการควบคุมเวลาที่การประมวลผลเวฟจะรันแบบอะซิงโครนัสและยึดตามงาน ซึ่งช่วยให้สามารถประมวลผลและสร้างงานพร้อมกันได้

ในครั้งแรก ข้อมูลเริ่มต้นจะใช้ค่าขีดจำกัดเป็น 15 สำหรับจํานวนรายการโหลดต่ำสุด (MINIMUMWAVELOADLINES) นี่หมายความว่าเมื่อระบบประมวลผลเวฟที่มีรายการโหลดมากกว่า 15 รายการ ระบบจะใช้การประมวลผลงานแบบอะซิงโครนัส คุณสามารถแทรก/อัพเดตข้อมูลนี้ด้วยตนเองในตาราง **WHSWaveTaskProcessingThresholdParameters** ในสภาพแวดล้อมการทดสอบของคุณ แต่ถ้าคุณต้องเปลี่ยนการตั้งค่านี้ในสภาพแวดล้อมการผลิต คุณต้องติดต่อ Microsoft Support เพื่อร้องขอการอัพเดต

## <a name="work-with-the-feature"></a>ทำงานกับคุณลักษณะ

เมื่อเปิดใช้งานฟังก์ชัน *การสร้างงานตามกำหนดการ* การประมวลผลเวฟจะสร้างงานที่วางแผนไว้ ซึ่งจะใช้โดยกระบวนการสร้างงานใหม่ในที่สุด ในระหว่างการสร้างงาน งานจะถูกบล็อคโดยใช้คุณลักษณะ *การบล็อคงานทั่วทั้งองค์กร*

แผนผังลำดับงานต่อไปนี้จะแสดงวิธีการสร้างงานที่วางแผนไว้ในระหว่างการประมวลผลเวฟ

![จัดกำหนดการสร้างงาน](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>งานที่วางแผนไว้

หน้า **รายละเอียดของงานที่วางแผนไว้** (**การจัดการคลังสินค้า \> งาน \> รายละเอียดงานของงานที่วางแผนไว้**) แสดงข้อมูลเกี่ยวกับงานที่วางแผนไว้ ซึ่งมีการสร้างขึ้นในตอนเริ่มต้นในระหว่างการประมวลผลเวฟ ค่า **สถานะกระบวนการ** ต่อไปนี้พร้อมใช้งาน:

- **จัดคิวแล้ว** - งานที่วางแผนไว้รอที่จะถูกใช้ในการสร้างงาน
- **เสร็จสมบูรณ์** - งานที่วางแผนไว้ถูกใช้ในการสร้างงาน
- **ล้มเหลว** – การประมวลผลเวฟล้มเหลว โปรดทราบว่างานที่วางแผนไว้สามารถอยู่ในสถานะ **ล้มเหลว** ที่มีหรือไม่มีงานจริงที่เกี่ยวข้อง เมื่อกระบวนการสร้างงานจริงล้มเหลว งานจริงจะยังคงอยู่ในสถานะ *ยกเลิกแล้ว*

### <a name="batch-job-for-the-work-creation-process"></a>ชุดงานสำหรับกระบวนการสร้างงาน

เมื่อต้องการดูงานในชุดงานของเวฟการประมวลผล ให้เลือก **งานในชุดงาน** บนบานหน้าต่างการดำเนินการในหน้า **เวฟทั้งหมด**

จากที่นี่ คุณสามารถดูรายละเอียดงานของชุดงานทั้งหมดสำหรับรหัสงานในชุดงานแต่ละรหัสได้
