---
title: ตั้งค่ารหัสการโอนการครอบครอง
description: คุณสามารถตั้งค่ารหัสการโอนการครอบครอง เพื่อระบุวิธีการประมวลผลสินค้าที่ถูกส่งคืนโดยลูกค้าได้
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnDispositionCode
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96fb8bd2ce7fed6962563773ad63a7a48943e1ca
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566517"
---
# <a name="set-up-disposition-codes"></a>ตั้งค่ารหัสการโอนการครอบครอง 

[!include [banner](../includes/banner.md)]


คุณสามารถตั้งค่ารหัสการโอนการครอบครอง เพื่อระบุวิธีการประมวลผลสินค้าที่ถูกส่งคืนโดยลูกค้าได้ ตัวอย่างเช่น สร้างรหัสการโอนการครอบครองที่ชื่อว่า **ซ่อมแซมและส่งคืน** เพื่อบ่งชี้ว่า สินค้าที่ส่งคืนจะถูกซ่อมแซม แล้วถูกส่งคืนให้แก่ลูกค้า สำหรับตัวอย่างเพิ่มเติมเกี่ยวกับรหัสการโอนการครอบครองที่ถูกใช้โดยทั่วไปสำหรับสินค้าที่ถูกส่งคืนโดยลูกค้า โปรดดู [Specify how to dispose of returned items](specify-how-to-dispose-of-returned-items.md).

นอกจากนี้ คุณยังสามารถตั้งค่ารหัสเหตุผลเพื่อช่วยอธิบายว่า เพราะเหตุใดจึงมีการส่งคืนสินค้า สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรหัสเหตุผล ให้ดูที่ [ตั้งค่ารหัสเหตุผลในการส่งคืน](set-up-return-reason-code.md)

1.  คลิก **การขายและการตลาด** \> **ตั้งค่า** \> **ใบสั่งขาย** \> **การส่งคืนสินค้า** \> **รหัสการโอนการครอบครอง**

2.  คลิก **สร้าง** หรือกด CTRL+N เพื่อสร้างรหัสการโอนการครอบครองใหม่

3.  ป้อนชื่อที่เป็นคำอธิบายที่ไม่ซ้ำ เลือกการดำเนินการ และป้อนคำอธิบายสำหรับรหัสการโอนการครอบครอง

4.  ถ้าคุณต้องการเชื่อมโยงค่าธรรมเนียมของลูกค้าใดๆ เข้ากับรหัสการโอนการครอบครองนี้ ให้คลิกปุ่ม **ค่าธรรมเนียม** เพื่อเปิดแบบฟอร์ม **ตั้งค่าค่าธรรมเนียม**

5.  ถ้าคุณต้องการกำหนดรหัสภายนอกเพื่อจับคู่กับรหัสการโอนการครอบครองของบริษัทของคุณเอง ให้คลิกปุ่ม **รหัสภายนอก** เพื่อเปิดแบบฟอร์ม **รหัสภายนอก**

## <a name="see-also"></a>ดูเพิ่มเติมที่

[รหัสการโอนการครอบครองและรหัสเหตุผลการส่งคืน](disposition-and-return-reason-codes.md)

[รหัสการจัดการ (แบบฟอร์ม)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))

[ค่าธรรมเนียมอัตโนมัติ (แบบฟอร์ม)](https://technet.microsoft.com/en-us/library/aa582856\(v=ax.60\))

[รหัสภายนอก (แบบฟอร์ม)](https://technet.microsoft.com/en-us/library/aa583814\(v=ax.60\))

  


