---
title: รักษากระบวนการผลิตสำหรับรุ่นผลิตภัณฑ์
description: 'การดำเนินกระบวนงานนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่ '
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88df8b867ac7f354417add0462e7999747333451
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577275"
---
# <a name="maintain-route-for-a-product-model"></a>รักษากระบวนการผลิตสำหรับรุ่นผลิตภัณฑ์

[!include [banner](../../includes/banner.md)]

การดำเนินกระบวนงานนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่  กระบวนงานนี้ใช้แบบจำลองลำโพงขั้นสูงในบริษัทสาธิต USMF เพื่อดำเนินกระบวนการ

## <a name="add-a-route-operation"></a>เพิ่มขั้นตอนของกระบวนการผลิต

1. ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> แบบจำลองการจัดโครงแบบผลิตภัณฑ์**
1. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกแบบจำลองลำโพงขั้นสูงสำหรับงานนี้  
1. ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก
1. ขยายส่วน **ดำเนินงานในกระบวนการผลิต**
1. เลือก **เพิ่ม**
1. ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง
1. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
1. เลือก **บันทึก**

## <a name="enter-route-operation-details"></a>ป้อนรายละเอียดขั้นตอนของกระบวนการผลิต

1. เลือก **รายละเอียดการดำเนินการในกระบวนการผลิต**
1. ในฟิลด์ **การดำเนินงาน** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
1. ใน **หมายเลขการดำเนินงาน** ป้อนหมายเลข
    * หมายเลขการดำเนินงานกำหนดลำดับในกระบวนการผลิต  
    * แต่ละคุณสมบัติในกระบวนการผลิตสามารถมีค่าคงที่หรือถูกแม็ปกับคุณลักษณะ  การแม็ปไปยังคุณลักษณะจะมีผลกับค่าที่ถูกตั้งค่าเป็นส่วนหนึ่งของการตั้งค่าคอนฟิก  
1. ในฟิลด์ **กลุ่มกระบวนการผลิต** ให้ป้อนหรือเลือกค่า
    * กลุ่มกระบวนการผลิตกำหนดลักษณะการทำงานที่จำเป็นสำหรับการคิดต้นทุน ปริมาณการใช้วัสดุ และการตั้งค่า  
1. เลือกแท็บ **การตั้งค่า**
1. เลือกแท็บ **เวลา**
1. ในฟิลด์ **ปริมาณกระบวนการ** ให้ป้อนตัวเลข
    * กำหนดจำนวนที่จะถูกประมวลผลในระหว่างการดำเนินงานหนึ่ง  
1. ในฟิลด์ **ชั่วโมง/เวลา** ให้ป้อนหมายเลข
    * ป้อนอัตราส่วนเวลา  
1. เลือกกล่องกาเครื่องหมาย **การตั้งค่า**
1. ในฟิลด์ **เวลาที่ใช้ในการผลิต** ให้ป้อนหมายเลข
    * กำหนดเวลาการประมวลผลสำหรับปริมาณที่คุณระบุ  
1. เลือกแท็บ **ความต้องการทรัพยากร**
1. เลือก **เพิ่ม**
1. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
1. ในฟิลด์ **ชนิดความต้องการ** ให้เลือกตัวเลือกหนึ่งตัวเลือก
    * ตัดสินใจว่าคุณต้องการระบุทรัพยากรที่เฉพาะเจาะจงหรือความสามารถที่ต้องมีอยู่หรือไม่  
1. ในฟิลด์ **ความต้องการ** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
1. เลือก **ตกลง**



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]