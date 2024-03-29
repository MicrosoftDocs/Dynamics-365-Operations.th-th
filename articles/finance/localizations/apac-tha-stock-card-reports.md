---
title: รายงานบัตรสินค้าคงคลังสำหรับประเทศไทย
description: บทความนี้ให้ข้อมูลเกี่ยวกับรายงานบัตรสินค้าคงคลังสำหรับนิติบุคคลในประเทศไทย
author: AdamTrukawka
ms.date: 03/21/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Thailand
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 265184
ms.assetid: 1ce8c70b-c6af-4171-98d2-2aa8e9563c5b
ms.search.form: TaxWithholdGroup, TaxWithholdTable, TaxWithholdTrans
ms.openlocfilehash: 0ac5f5e889fe47795000a4ed8a90a1ea83929be9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291654"
---
# <a name="stock-card-report-for-thailand"></a>รายงานบัตรสินค้าคงคลังสำหรับประเทศไทย

[!include [banner](../includes/banner.md)]

บทความนี้ให้ข้อมูลเกี่ยวกับรายงานบัตรสินค้าคงคลังสำหรับนิติบุคคลในประเทศไทย รายงานบัตรสินค้าคงคลังประกอบด้วยรายละเอียดเกี่ยวกับความเคลื่อนไหวของสินค้าคงคลัง ปริมาณ และต้นทุนสำหรับแต่ละสินค้าและคลังสินค้า และจะต้องถูกสร้างขึ้นเมื่อรัฐบาลร้องขอ รายงานบัตรสินค้าคงคลังจะถูกสร้างขึ้นก่อนหรือหลังกระบวนการปิดบัญชีสินค้าคงคลัง 

คุณสามารถสร้างรายงานบัตรสินค้าคงคลังต่อไปนี้:

-   **บัตรสินค้าคงคลังตามจริง** – ดูข้อมูลที่เกี่ยวข้องกับไซต์เดียวหรือไซต์ทั้งหมดต่อสถานที่เก็บและคลังสินค้า หลังจากมีการลงรายการบัญชีบันทึกการจัดส่ง
-   **บัตรสินค้าคงคลังทางการเงิน** – ดูข้อมูลที่เกี่ยวข้องกับไซต์เดียวหรือไซต์ทั้งหมดต่อสถานที่เก็บและคลังสินค้า หลังจากมีการลงรายการบัญชีใบแจ้งหนี้
-   **สรุปบัตรสินค้าคงคลัง** – ดูรายละเอียดสินค้าหรือคลังสินค้าตามกลุ่มสินค้า ไซต์ คลังสินค้า และต้นทุน

## <a name="set-up-the-generation-of-stock-card-reports"></a>ตั้งค่าการสร้างรายงานบัตรสินค้าคงคลัง
ทำงานต่อไปนี้ให้เสร็จสมบูรณ์ก่อนที่คุณจะสร้างรายงานบัตรสินค้าคงคลัง:

-   สร้างรายการที่มีข้อมูลที่จำเป็น **หมายเหตุ:** กำหนดสำนักงานสาขาย่อยที่ยื่นให้กับไซต์
-   สร้างสำนักงานสาขาย่อยที่ยื่น
-   ตั้งค่าสำนักงานสาขาย่อยที่ยื่นสำหรับนิติบุคคล
-   ตั้งค่าสำนักงานสาขาย่อยที่ยื่นสำหรับผู้จัดจำหน่ายหรือลูกค้า
-   กำหนดสำนักงานสาขาย่อยที่ยื่นให้กับไซต์
-   สร้างและลงรายการบัญชีธุรกรรมการซื้อ การขาย และการโอนย้ายสินค้าคงคลังที่จำเป็น

## <a name="recalculate-inventory-and-generate-the-financial-stock-card-report"></a>คำนวณสินค้าคงคลังอีกครั้ง และสร้างรายงานบัตรสินค้าคงคลังทางการเงิน
ใช้หน้า **การปิดและการปรับปรุง** ในการคำนวณสินค้าคงคลังอีกครั้งหลังจากมีการรันกระบวนการปิดบัญชีสินค้าคงคลัง และสร้างรายงานบัตรสินค้าคงคลังทางการเงิน

## <a name="generate-the-stock-card-report"></a>สร้างรายงานบัตรสินค้าคงคลัง
คุณสามารถจัดกลุ่มสินค้าต่างๆ ตามไซต์ คลังสินค้า สถานที่เก็บ หมายเลขสินค้า หรือกลุ่มสินค้า และสร้างรายงานบัตรสินค้าคงคลัง ใช้รายงาน **บัตรสินค้าคงคลัง – ตามจริง** ในการสร้างรายงานบัตรสินค้าคงคลังตามจริง ใช้รายงาน **บัตรสินค้าคงคลัง – ทางการเงิน** ในการสร้างรายงานบัตรสินค้าคงคลังทางการเงิน คุณสามารถสร้างรายงานบัตรสินค้าคงคลังโดยละเอียดหรือโดยสรุป


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
