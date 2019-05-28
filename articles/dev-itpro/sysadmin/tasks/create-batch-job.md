---
title: การสร้างชุดงาน
description: 'ชุดงานคือกลุ่มของงานที่ส่งไปยังอินสแตนซ์เซิร์ฟเวอร์แอพลิเคชันออบเจ็กต์ (AOS) สำหรับการประมวลผลโดยอัตโนมัติ '
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562892"
---
# <a name="create-a-batch-job"></a>การสร้างชุดงาน

[!include [task guide banner](../../includes/task-guide-banner.md)]

ชุดงานคือกลุ่มของงานที่ส่งไปยังอินสแตนซ์เซิร์ฟเวอร์แอพลิเคชันออบเจ็กต์ (AOS) สำหรับการประมวลผลโดยอัตโนมัติ  ชุดงานจะรันโดยใช้ข้อมูลประจำตัวของผู้ใช้ที่สร้างงานนั้น  ใช้กระบวนงานต่อไปนี้ในการสร้างชุดงาน  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF


## <a name="create-the-batch-job"></a>สร้างชุดงาน
1. ไปที่ การดูแลระบบ > การสอบถาม > ชุดงาน
2. คลิก สร้าง
3. ในฟิลด์คำอธิบายงาน ให้พิมพ์ค่า
4. ในฟิลด์วันที่/เวลาเริ่มต้นตามกำหนดการ ให้ป้อนวันที่และเวลา
5. คลิก บันทึก

## <a name="create-a-recurrence"></a>สร้างการเกิดซ้ำ
1. ในบานหน้าต่างการดำเนินการ คลิกชุดงาน
2. การเกิดซ้ำ 
    * ใช้ตัวเลือกเหล่านี้เพื่อป้อนช่วงและรูปแบบสำหรับการเกิดซ้ำ  
3. คลิก ตกลง

## <a name="add-alerts"></a>เพิ่มข้อความแจ้งเตือน
1. ในบานหน้าต่างการดำเนินการ คลิกชุดงาน
2. คลิกที่ข้อความแจ้งเตือน
    * ระบุว่าคุณต้องการได้รับข้อความแจ้งเตือนเมื่อชุดงานสิ้นสุด มีข้อผิดพลาด หรือถูกยกเลิกหรือไม่  จากนั้นระบุว่าคุณต้องการให้แสดงข้อความแจ้งเตือนเป็นข้อความป็อปอัพหรือไม่   
3. คลิก ตกลง

