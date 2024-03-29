---
title: รักษาชนิดบาร์โค้ด
description: กระบวนงานนี้แสดงวิธีการตั้งค่าข้อกำหนดบาร์โค้ดใหม่ ซึ่งสามารถนำไปใช้เป็นส่วนหนึ่งของรายงานรายการเบิกสินค้า
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b689d1fc85d59ac87efa1903fd7122ae5ff011da
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571124"
---
# <a name="maintain-bar-code-types"></a>รักษาชนิดบาร์โค้ด

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการตั้งค่าข้อกำหนดบาร์โค้ดใหม่ ซึ่งสามารถนำไปใช้เป็นส่วนหนึ่งของรายงานรายการเบิกสินค้า คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF หรือใช้ข้อมูลของคุณเอง ถ้าคุณกำลังใช้ USMF คุณสามารถใช้ตัวอย่างมูลค่าที่แสดงอยู่ งานเหล่านี้โดยทั่วไปจะถูกดำเนินการโดยผู้จัดการคลังสินค้า

1. ไปที่ **บาร์โค้ด**
1. เลือก **ใหม่**
1. ในฟิลด์ **การตั้งค่าบาร์โค้ด** ให้พิมพ์ค่าใดค่าหนึ่ง
1. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
1. ในฟิลด์ **ชนิดของบาร์โค้ด** ให้เลือกตัวเลือกหนึ่งตัวเลือก
    * ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก 'รหัส 39' ได้
1. ในฟิลด์ **รหัสตัวพราง** ให้ระบุรหัสตัวพรางบาร์โค้ด ใช้ตัวพรางบาร์โค้ดในการสร้างบาร์โค้ดและการระบุบาร์โค้ดที่ถูกสแกนไปยังระบบการขายหน้าร้าน (POS) ได้อย่างรวดเร็ว สำหรับรายละเอียด ให้ดูที่ [ตั้งค่าตัวพรางบาร์โค้ด](../../../commerce/set-up-bar-code-masks.md)
1. ในฟิลด์ **ขนาด** ให้ป้อนตัวเลข
1. ในฟิลด์ **ความยาวสูงสุด** ให้ป้อนตัวเลข
1. เลือก **บันทึก**
1. ปิดหน้า
1. ไปที่ **สินค้าคงคลังและพารามิเตอร์การจัดการคลังสินค้า**
1. ในฟิลด์ **การตั้งค่าบาร์โค้ด** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * เลือกการตั้งค่าบาร์โค้ดที่คุณสร้างขึ้นก่อนหน้า แต่ให้ระวังว่าบาร์โค้ดต้องตรงกับรูปแบบของตัวระบุเฉพาะสำหรับชนิดของเรกคอร์ดที่ใช้ในกระบวนการ ตัวอย่างเช่น สำหรับเส้นทางการเบิกสินค้า รูปแบบบาร์โค้ดควรตรงกับรูปแบบของการอ้างอิงเส้นทางการเบิกสินค้า ซึ่งโดยปกติจะเป็นลำดับหมายเลข  
1. เลือก **บันทึก**
1. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
