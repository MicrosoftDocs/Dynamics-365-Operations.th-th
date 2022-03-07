---
title: กำหนดเวอร์ชัน BOM
description: ในระหว่างการกระจายความต้องการ ถ้าสินค้ามีชนิดใบสั่งเริ่มต้นของการผลิต กลไกจัดการการวางแผนจะหารุ่น BOM ที่ถูกต้องตามไซต์
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370091eed4ee050031d5d135aa7b1d8d0fe82491
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570980"
---
# <a name="determine-the-bom-version"></a>กำหนดเวอร์ชัน BOM

[!include [banner](../includes/banner.md)]

ในระหว่างการกระจายความต้องการ ถ้าสินค้ามีชนิดใบสั่งเริ่มต้นของการผลิต กลไกจัดการการวางแผนจะหารุ่น BOM ที่ถูกต้องตามไซต์ 

มิติไซต์จะทราบเสมอ และระบุในธุรกรรมความต้องการ กระบวนการต่อไปนี้จะใช้เพื่อกำหนดรุ่น BOM ที่จะใช้:

-   ถ้ามีรุ่น BOMที่กำหนดสำหรับสินค้าที่ไซต์ความต้องการ BOM เฉพาะไซต์จะถูกใช้
-   ถ้าไม่มีรุ่น BOM เฉพาะไซต์ที่กำหนดสำหรับสินค้าที่ไซต์ความต้องการ BOM ทั่วไปจะถูกใช้ BOM ทั่วไปไม่ได้ระบุไซต์ และสามารถใช้ได้กับหลายไซต์ ถ้ามี BOM ทั่วไป ก็จะถูกใช้
-   ถ้าไม่มีรุ่น BOM ทั่วไปที่จะใช้ การกระจายความต้องการจะหยุดที่จุดนี้

BOM เวอร์ชันที่ถูกต้อง ไม่ว่าจะเป็นแบบเฉพาะไซต์หรือทั่วไป ต้องมีลักษณะตรงตามเงื่อนไขเกี่ยวกับวันที่และปริมาณที่กำหนด







[!INCLUDE[footer-include](../../includes/footer-banner.md)]