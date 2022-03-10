---
title: รักษา BOM สำหรับแบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'การดำเนินขั้นตอนนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่ '
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd78b06f10d0c9b1df57dacdd824b06ebe414b3b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577299"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>รักษา BOM สำหรับแบบจำลองการจัดโครงแบบผลิตภัณฑ์

[!include [banner](../../includes/banner.md)]

การดำเนินขั้นตอนนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่  แบบจำลองลำโพงขีดขั้นสูงในบริษัทสาธิต USMF จะใช้เพื่อสร้างกระบวนงานนี้

## <a name="add-a-bom-line"></a>เพิมรายการ BOM

1. ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> แบบจำลองการจัดโครงแบบผลิตภัณฑ์**
1. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกลำโพงขั้นสูงสำหรับกระบวนงานนี้  
1. ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก
1. ขยายส่วน **รายการ BOM**
1. เลือก **เพิ่ม**
1. ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง
1. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
1. เลือก **บันทึก**

## <a name="add-bom-line-details"></a>เพิ่มรายละเอียดรายการ BOM

1. เลือก **รายละเอียดรายการ BOM**
2. ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * ตัวอย่างเช่น คุณสามารถเลือกสินค้า M0055  
    * สำหรับแต่ละคุณสมบัติของรายการ BOM คุณสามารถเลือกได้ว่าจะเป็นค่าคงที่หรือมีการแม็ปไปที่คุณลักษณะ  
3. เลือกกล่องกาเครื่องหมาย **การตั้งค่า**
4. เลือก *ใช่* ในฟิลด์ **การคำนวณ**
    * การตั้งค่าคุณสมบัติ **การคำนวณ** เป็น *ใช่* ช่วยให้มั่นใจว่ารายการ BOM จะถูกรวมอยู่ในการคำนวณต้นทุน  
5. เลือกแท็บ **การตั้งค่า**
6. เลือกกล่องกาเครื่องหมาย **การตั้งค่า**
7. ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข
    * ฟิลด์ปริมาณกำหนดจำนวนของสินค้าที่จะรวมอยู่ใน BOM  นี่อาจเป็นตัวเลือกที่ชัดเจนสำหรับการแม็ปคุณลักษณะ  
8. เลือกแท็บ **มิติ**
    * ตรวจสอบถ้ามีมิติของผลิตภัณฑ์ใดๆมีการใช้งานอยู่ และดังนั้น ต้องมีค่าหรือคุณลักษณะที่กำหนดให้  
9. เลือก **ตกลง**


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]