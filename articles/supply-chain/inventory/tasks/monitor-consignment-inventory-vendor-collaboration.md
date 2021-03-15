---
title: ตรวจสอบสินค้าคงคลังที่มีการส่งมอบโดยใช้การทำงานร่วมกันกับผู้จัดจำหน่าย
description: 'กระบวนงานนี้แสดงวิธีการใช้การทำงานร่วมกันกับผู้จัดจำหน่ายเพื่อดูรายละเอียดเกี่ยวกับระดับสินค้าคงคลังของผลิตภัณฑ์ที่คุณได้ทำในการส่งมอบให้กับลูกค้า '
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f2e782bed4cd9f2f13e2ee45afffaef277279131
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020140"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>ตรวจสอบสินค้าคงคลังที่มีการส่งมอบโดยใช้การทำงานร่วมกันกับผู้จัดจำหน่าย

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการใช้การทำงานร่วมกันกับผู้จัดจำหน่ายเพื่อดูรายละเอียดเกี่ยวกับระดับสินค้าคงคลังของผลิตภัณฑ์ที่คุณได้ทำในการส่งมอบให้กับลูกค้า  คุณยังสามารถตรวจสอบปริมาณการใช้สินค้าคงคลังเมื่อลูกค้ากลายเป็นเจ้าของสินค้าคงคลังได้อีกด้วย คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มใน Dynamics 365 for Operations รุ่น 1611


## <a name="view-consumed-inventory"></a>ดูสินค้าคงคลังที่ใช้
1. ไปที่ การทำงานร่วมกันกับผู้จัดจำหน่าย > สินค้าคงคลังที่มีการส่งมอบ > ผลิตภัณฑ์ที่ได้รับจากสินค้าคงคลังที่มีการส่งมอบ
    * รายการจะแสดงรายการใบรับสินค้าที่สร้างขึ้นเมื่อความเป็นเจ้าของสินค้าคงคลังที่มีการส่งมอบเปลี่ยนจากผู้จัดจำหน่ายเป็นลูกค้า  คุณอาจต้องเลื่อนไปทางขวาเพื่อดูปริมาณและข้อมูลอื่น ๆ คุณสามารถใช้ข้อมูลในรายการนี้ในการสร้างใบแจ้งหนี้สำหรับลูกค้าของคุณ  นอกจากนี้ คุณยังสามารถส่งออกข้อมูลไปยัง Microsoft Excel ได้   
2. คลิก ดูรายการใบสั่งซื้อ
3. ขยายส่วน รายละเอียดของรายการ
    * รายการถูกทำเครื่องหมายเป็นการส่งมอบ และส่วนหัวแสดงให้เห็นว่าใบสั่งซื้อมีสถานะเป็นได้รับแล้ว  
4. ปิดหน้า

## <a name="view-on-hand-inventory"></a>ดูสินค้าคงคลังคงเหลือ
1. ไปที่ การทำงานร่วมกันกับผู้จัดจำหน่าย > สินค้าคงคลังที่มีการส่งมอบ > ปริมาณคงคลังคงเหลือ
    * หน้าปริมาณคงคลังคงเหลือแสดงสินค้าคงคลังที่คุณเป็นเจ้าของที่คลังสินค้าของลูกค้า คุณสามารถแสดงมิติเพิ่มเติม เช่น ไซต์และคลังสินค้าได้โดยการคลิกแท็บแสดงมิติ   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]