---
title: "กำหนดเวอร์ชัน BOM"
description: "ในระหว่างการกระจายความต้องการ ถ้าสินค้ามีชนิดใบสั่งเริ่มต้นของการผลิต กลไกจัดการการวางแผนจะหารุ่น BOM ที่ถูกต้องตามไซต์"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 134b9f7fd46b5326eb6f1f4fec4ed2bda8a8576a
ms.contentlocale: th-th
ms.lasthandoff: 04/25/2017


---

# <a name="determine-the-bom-version"></a>กำหนดเวอร์ชัน BOM

[!include[banner](../includes/banner.md)]


ในระหว่างการกระจายความต้องการ ถ้าสินค้ามีชนิดใบสั่งเริ่มต้นของการผลิต กลไกจัดการการวางแผนจะหารุ่น BOM ที่ถูกต้องตามไซต์ 

มิติไซต์จะทราบเสมอ และระบุในธุรกรรมความต้องการ กระบวนการต่อไปนี้จะใช้เพื่อกำหนดรุ่น BOM ที่จะใช้:

-   ถ้ามีรุ่น BOMที่กำหนดสำหรับสินค้าที่ไซต์ความต้องการ BOM เฉพาะไซต์จะถูกใช้
-   ถ้าไม่มีรุ่น BOM เฉพาะไซต์ที่กำหนดสำหรับสินค้าที่ไซต์ความต้องการ BOM ทั่วไปจะถูกใช้ BOM ทั่วไปไม่ได้ระบุไซต์ และสามารถใช้ได้กับหลายไซต์ ถ้ามี BOM ทั่วไป ก็จะถูกใช้
-   ถ้าไม่มีรุ่น BOM ทั่วไปที่จะใช้ การกระจายความต้องการจะหยุดที่จุดนี้

BOM เวอร์ชันที่ถูกต้อง ไม่ว่าจะเป็นแบบเฉพาะไซต์หรือทั่วไป ต้องมีลักษณะตรงตามเงื่อนไขเกี่ยวกับวันที่และปริมาณที่กำหนด






