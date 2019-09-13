---
title: แก้ไขการคาดการณ์ความต้องการด้วยตนเอง
description: 'กระบวนงานนี้แสดงวิธีการแก้ไขการคาดการณ์สำหรับสินค้า '
author: ShylaThompson
manager: AnnBe
ms.date: 08/12/2019
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
ms.openlocfilehash: 1ec1edb861619bae2ae3c211720b55e170b83ec9
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916633"
---
# <a name="modify-a-demand-forecast-manually"></a>แก้ไขการคาดการณ์ความต้องการด้วยตนเอง

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการแก้ไขการคาดการณ์สำหรับสินค้า  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF การบันทึกนี้มีไว้สำหรับผู้วางแผนการผลิต  


## <a name="modify-the-forecast-for-an-item"></a>แก้ไขการคาดการณ์สำหรับสินค้า
1. ใน **บานหน้าต่างนำทาง** ไปยัง **โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้**
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ เลือกสินค้าที่คุณต้องการแก้ไขการคาดการณ์  ตัวอย่างเช่น คุณสามารถเลือกสินค้า D0001  
3. ใน **บานหน้าต่างการดำเนินการ** คลิก **วางแผน**
4. คลิก **การคาดการณ์ความต้องการ**
5. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก ถ้าไม่มีรายการการคาดการณ์ สร้างรายการใหม่โดยคลิกสร้างบนแถบแอป  
6. ในฟิลด์ **ปริมาณการขาย** ให้ป้อนตัวเลข ตัวเลขนี้จะแสดงถึงปริมาณที่คาดการณ์ของสินค้า   
7. คลิก บันทึก

## <a name="modify-the-forecast-in-excel"></a>แก้ไขการคาดการณ์ใน Excel
1. คลิก **เปิด** ใน Microsoft Office
2. คลิก **แก้ไขการคาดการณ์ความต้องการ** ใน Excel ใน Excel คุณสามารถเพิ่ม ลบ และแก้ไขบรรทัดการคาดการณ์ความต้องการได้  ถ้าคุณไม่สามารถดูข้อมูลใน Excel ได้ คุณต้องลงชื่อเข้าใช้ Microsoft Dynamics 365 for Finance and Operations Enterprise edition ด้วยตัวเลือก "คงการลงชื่อเข้าใช้ของฉันไว้" ที่เปิดใช้งานและคุณต้องเชื่อแอปการเชื่อมต่อข้อมูล  

