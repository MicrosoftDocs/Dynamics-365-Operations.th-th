---
title: สินค้าไม่สามารถมี BOM หรือสูตร
description: เมื่อคุณพยายามยืนยันใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดระหว่างการตรวจสอบความถูกต้องของสินค้า ระบุว่าสินค้าไม่สามารถมีสูตรการผลิต (BOM) หรือสูตร
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1e946adc3a04db60bf15ac7bb44163085e1c19802872964877d3929b1f79bf7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730117"
---
# <a name="item-cant-have-a-bom-or-formula"></a>สินค้าไม่สามารถมี BOM หรือสูตร

รหัสข้อผิดพลาด: PRO2614

## <a name="symptoms"></a>อาการ

เมื่อคุณพยายามยืนยันใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดระหว่างการตรวจสอบความถูกต้องของสินค้าต่อไปนี้:

> สินค้าไม่สามารถมี BOM หรือสูตร

## <a name="resolution"></a>การแก้ปัญหา

สินค้าที่มีสูตรการผลิต (BOM) หรือสูตรต้องเป็นชนิด *การวางแผนสินค้า* *BOM* หรือ *สูตร* เมื่อต้องการเปลี่ยนชนิดของสินค้า ให้ทำตามขั้นตอนเหล่านี้:

1. ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**
1. เปิดผลิตภัณฑ์ที่เกี่ยวข้อง
1. บนแท็บด่วน **วิศวกรรม** ตั้งค่าฟิลด์ **ชนิดผลิตภัณฑ์** เป็น *การวางแผนสินค้า* *BOM* หรือ *สูตร*
