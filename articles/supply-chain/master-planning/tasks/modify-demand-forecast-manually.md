---
title: แก้ไขการคาดการณ์ความต้องการด้วยตนเอง
description: 'กระบวนงานนี้แสดงวิธีการแก้ไขการคาดการณ์สำหรับสินค้า '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca6b881bc094b68d1bbf8c7c20b65418e42b28e3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835892"
---
# <a name="modify-a-demand-forecast-manually"></a>แก้ไขการคาดการณ์ความต้องการด้วยตนเอง

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการแก้ไขการคาดการณ์สำหรับสินค้า  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF การบันทึกนี้มีไว้สำหรับผู้วางแผนการผลิต  


## <a name="modify-the-forecast-for-an-item"></a>แก้ไขการคาดการณ์สำหรับสินค้า
1. ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ 
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกสินค้าที่คุณต้องการแก้ไขการคาดการณ์  ตัวอย่างเช่น คุณสามารถเลือกสินค้า D0001  
3. ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน
4. คลิก การคาดการณ์ความต้องการ
5. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
    * ถ้าไม่มีรายการการคาดการณ์ สร้างรายการใหม่โดย การคลิกสร้างบนแถบแอพลิเคชัน  
6. ในฟิลด์ปริมาณการขาย ให้ป้อนตัวเลข 
    * ตัวเลขนี้จะแสดงถึงปริมาณที่คาดการณ์ของสินค้า   
7. คลิก บันทึก

## <a name="modify-the-forecast-in-excel"></a>แก้ไขการคาดการณ์ใน Excel
1. คลิกเปิดใน Microsoft Office
2. คลิกแก้ไขการคาดการณ์ความต้องการใน Excel 
    * ใน Excel คุณสามารถเพิ่ม ลบ และแก้ไขบรรทัดการคาดการณ์ความต้องการได้  ถ้าคุณไม่สามารถดูข้อมูลใน Excel ได้ คุณต้องลงชื่อเข้าใช้ Microsoft Dynamics 365 for Finance and Operations Enterprise edition ด้วยตัวเลือก "คงการลงชื่อเข้าใช้ของฉันไว้" ที่เปิดใช้งานและคุณต้องเชื่อแอปการเชื่อมต่อข้อมูล  

