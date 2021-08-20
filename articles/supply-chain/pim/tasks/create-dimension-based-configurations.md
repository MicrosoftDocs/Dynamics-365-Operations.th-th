---
title: สร้างการจัดโครงแบบตามมิติ
description: 'กระบวนงานนี้แสดงวิธีการกำหนดการปรับเปลี่ยนสำหรับผลิตภัณฑ์ตามมิติ '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b233f4a52652b359cd033c08544ca6f49470fc4d24d6cc33b79e32a372a259f7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757721"
---
# <a name="create-dimension-based-configurations"></a>สร้างการจัดโครงแบบตามมิติ

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการกำหนดการปรับเปลี่ยนสำหรับผลิตภัณฑ์ตามมิติ  นี่คือกระบวนงานสุดท้ายในชุดที่อธิบายถึงวิธีการสร้างชุดงานสำหรับการจัดโครงแบบตามมิติ การดำเนินการกระบวนงานนี้จะขึ้นอยู่กับข้อมูลที่สร้างขึ้นในการบันทึกเจ็ดรายการก่อนหน้านี้ บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF

## <a name="find-the-dimension-based-product-master"></a>หาผลิตภัณฑ์หลักตามมิติ

1. ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**
1. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
    * เลือกผลิตภัณฑ์หลักตามมิติ ที่คุณสร้างขึ้นในการบันทึกแรกในลำดับงานของการบันทึก 8 รายการนี้  

## <a name="create-configurations"></a>สร้างการตั้งค่าคอนฟิก

1. ในบานหน้าต่างการดำเนินการ **วิศวกรรม** เลือก **รักษาการตั้งค่าคอนฟิก**
1. เลือก **ตั้งค่าคอนฟิก**
1. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
1. ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * เลือกสินค้าใดๆของกลุ่มการปรับเปลี่ยนแรก  
1. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
1. ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * เลือกสินค้าใดๆจากกลุ่มการปรับเปลี่ยนที่สอง  
1. เลือก **ตกลง**
1. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
1. ในฟิลด์ **การตั้งค่าคอนฟิก** ให้พิมพ์ค่าใดค่าหนึ่ง
    * ป้อนชื่อของกลุ่มการปรับเปลี่ยนที่จะทำให้ง่ายต่อการระบุการปรับเปลี่ยน  
1. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
    * ป้อนคำอธิบายของการปรับเปลี่ยนเพื่ออธิบายส่วนประกอบ  
1. เลือก **ตกลง**



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]