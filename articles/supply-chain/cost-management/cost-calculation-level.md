---
title: ระดับการคำนวณต้นทุน
description: บทความนี้อธิบายระดับของรายการวัสดุและส่วนประกอบ (BOM) ที่มีการตั้งชื่อว่าระดับการคำนวณต้นทุน ระดับ BOM นี้ไม่รวมใบสั่งผลิตและใบสั่งชุดในการคำนวณ
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: e63a868696e36c1d4f5d19ea87bdf4d682c39f8c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334969"
---
# <a name="cost-calculation-level"></a>ระดับการคำนวณต้นทุน

[!include [banner](../includes/banner.md)]

ระดับของรายการวัสดุและส่วนประกอบ (BOM) ที่ตั้งชื่อเป็น **ระดับการคำนวณต้นทุน** ไม่รวมใบสั่งผลิตและใบสั่งชุดงานในการคำนวณ ระบบจะใช้ระดับนี้ เมื่อเรียกใช้การคำนวณต้นทุนในเวอร์ชันการคิดต้นทุน ในกระบวนการ เช่น การคำนวณใหม่ และการปิดบัญชีสินค้าคงคลัง ระบบจะใช้ BOM ระดับ **ระดับการคิดต้นทุน** แทน

## <a name="turn-the-cost-calculation-level-feature-on-or-off"></a>เปิดหรือปิดคุณลักษณะระดับการคำนวณต้นทุน

การใช้คุณลักษณะนี้ ต้องเปิดคุณลักษณะนี้ในระบบของคุณก่อน เริ่มจาก Supply Chain Management รุ่น 10.0.29 คุณลักษณะนี้จะเปิดไว้ ตามค่าเริ่มต้น ผู้ดูแลระบบสามารถเปิดหรือปิดฟังก์ชันนี้ได้โดยค้นหาคุณลักษณะ *ระดับการคำนวณต้นทุน* ในพื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

## <a name="example-scenario"></a>ตัวอย่างสถานการณ์จำลอง

สถานการณ์จำลองอย่างง่ายต่อไปนี้แสดงความแตกต่างระหว่าง BOM ระดับ **ระดับการคำนวณต้นทุน** และ BOM ระดับ **ระดับการคิดต้นทุน**

คุณมีผลิตภัณฑ์สามผลิตภัณฑ์ได้แก่ A B และ C ผลิตภัณฑ์ C เป็นส่วนประกอบของผลิตภัณฑ์ B และผลิตภัณฑ์ B เป็นส่วนประกอบของผลิตภัณฑ์ A

- **ระดับการคิดต้นทุน** กำหนดระดับ BOM ต่อไปนี้:

    - **ผลิตภัณฑ์ A:** 0
    - **ผลิตภัณฑ์ B:** 1
    - **ผลิตภัณฑ์ C:** 2

- **ระดับการคำนวณต้นทุน** กำหนดระดับ BOM ต่อไปนี้:

    - **ผลิตภัณฑ์ A:** 0
    - **ผลิตภัณฑ์ B:** 1
    - **ผลิตภัณฑ์ C:** 2

ใบสั่งผลิตสำหรับผลิตภัณฑ์ C จะถูกสร้าง และมีการเพิ่มผลิตภัณฑ์ A ที่ BOM ใบสั่งผลิต หลังจากที่มีการประเมินใบสั่งแล้ว ระดับ BOM จะมีการอัพเดตในลักษณะต่อไปนี้:

- **ระดับการคิดต้นทุน** กำหนดระดับ BOM ต่อไปนี้:

    - **ผลิตภัณฑ์ B:** 1
    - **ผลิตภัณฑ์ C:** 2
    - **ผลิตภัณฑ์ A:** 3

- **ระดับการคำนวณต้นทุน** กำหนดระดับ BOM ต่อไปนี้:

    - **ผลิตภัณฑ์ A:** 0
    - **ผลิตภัณฑ์ B:** 1
    - **ผลิตภัณฑ์ C:** 2

ลักษณะการทำงานนี้ช่วยให้มั่นใจว่าการเปลี่ยนแปลงใน BOM ของใบสั่งผลิตจะไม่มีผลกระทบต่อการคำนวณต้นทุน


[!INCLUDE[footer-include](../../includes/footer-banner.md)]