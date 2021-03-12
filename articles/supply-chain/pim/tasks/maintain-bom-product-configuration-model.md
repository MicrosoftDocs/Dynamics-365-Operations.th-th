---
title: รักษา BOM สำหรับแบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'การดำเนินขั้นตอนนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่ '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 267ac5447d36f63094fdb57c0d450e4d79cf138b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966866"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>รักษา BOM สำหรับแบบจำลองการจัดโครงแบบผลิตภัณฑ์

[!include [banner](../../includes/banner.md)]

การดำเนินขั้นตอนนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่  แบบจำลองลำโพงขีดขั้นสูงในบริษัทสาธิต USMF จะใช้เพื่อสร้างกระบวนงานนี้


## <a name="add-a-bom-line"></a>เพิมรายการ BOM
1. คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย
2. คลิก แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์
3. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกลำโพงขั้นสูงสำหรับกระบวนงานนี้  
4. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
5. ขยายส่วนรายการ BOM
6. คลิก เพิ่ม
7. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
8. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า
9. คลิก บันทึก

## <a name="add-bom-line-details"></a>เพิ่มรายละเอียดรายการ BOM
1. คลิกรายละเอียดรายการ BOM
2. ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า
    * ตัวอย่างเช่น คุณสามารถเลือกสินค้า M0055  
    * สำหรับแต่ละคุณสมบัติของรายการ BOM คุณสามารถเลือกได้ว่าจะเป็นค่าคงที่หรือมีการแม็ปไปที่คุณลักษณะ  
3. เลือกการตั้งค่ากล่องกาเครื่องหมาย
4. เลือก ใช่ ในฟิลด์การคำนวณ
    * การตั้งค่าคุณสมบัติการคำนวณเป็น ใช่ ช่วยให้มั่นใจว่ารายการ BOM จะถูกรวมอยู่ในการคำนวณต้นทุน  
5. คลิกแท็บ การตั้งค่า
6. เลือกการตั้งค่ากล่องกาเครื่องหมาย
7. ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข
    * ฟิลด์ปริมาณกำหนดจำนวนของสินค้าที่จะรวมอยู่ใน BOM  นี่อาจเป็นตัวเลือกที่ชัดเจนสำหรับการแม็ปคุณลักษณะ  
8. คลิกแท็บมิติ
    * ตรวจสอบถ้ามีมิติของผลิตภัณฑ์ใดๆมีการใช้งานอยู่ และดังนั้น ต้องมีค่าหรือคุณลักษณะที่กำหนดให้  
9. คลิก ตกลง

