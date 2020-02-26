---
title: ตัวเลือกสำหรับการป้องกันไม่ให้มีส่วนลดสำหรับผลิตภัณฑ์ Retail
description: มีเหตุผลต่าง ๆ ว่าเพราะเหตุใดผู้ค้าปลีกอาจต้องการป้องกันไม่ให้ได้รับส่วนลด จากโปรโมชัน หรือ ระหว่างการขายที่ POS
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 822bd39bca3a95f073bacea90a8ee58eada50ae2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024246"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a>ตัวเลือกสำหรับการป้องกันไม่ให้มีส่วนลดสำหรับผลิตภัณฑ์ Retail

[!include [banner](includes/banner.md)]

มีเหตุผลต่าง ๆ ว่าเพราะเหตุใดผู้ค้าปลีกอาจต้องการป้องกันไม่ให้ได้รับส่วนลด จากโปรโมชัน หรือ ระหว่างการขายที่ POS

ตัวเลือกต่อไปนี้ซึ่งสามารถพบได้ในแท็บ **การค้า** ของผลิตภัณฑ์ที่วางจำหน่าย จะช่วยให้สามารถกำหนดค่าผลิตภัณฑ์เพื่อป้องกันส่วนลดทั้งหมดหรือส่วนลดด้วยตนเอง คุณสามารถระบุการตั้งค่าได้ที่ระดับประเภทจากลำดับชั้นประเภทการขายปลีก

- **ป้องกันส่วนลดทั้งหมด** – เลือกตัวเลือกนี้เพื่อป้องกันไม่ให้มีการนำส่วนลดทุกประเภททั้งหมดไปใช้กับผลิตภัณฑ์นี้ ซึ่งรวมถึงโปรโมชันต่าง ๆ เช่น การซื้อคละกัน ส่วนลดตามปริมาณและส่วนลดจำกัด รวมทั้งส่วนลดต่อรายการสินค้าที่กำหนดเองและส่วนลดของธุรกรรมที่ใช้ในระหว่างการขายโดยผู้ใช้ POS
- **ป้องกันส่วนลดที่กำหนดเอง** – เลือกตัวเลือกนี้เพื่อป้องกันเฉพาะส่วนลดต่อรายการสินค้าที่กำหนดเอง หรือส่วนลดของธุรกรรมที่ใช้ในระหว่างการขายโดยผู้ใช้ POS ผลิตภัณฑ์ที่มีการเลือกตัวเลือกนี้จะยังคงมีสิทธิ์สำหรับการส่งเสริมการขาย เช่น ส่วนลดสำหรับการซื้อคละกัน และส่วนลดตามปริมาณและส่วนลดจำกัด

> [!NOTE]
> การตั้งค่าเหล่านี้ไม่จำกัดการดำเนินการแทนที่ราคา เนื่องจากจะเป็นการกำหนดราคาพื้นฐานและไม่ถือว่าเป็นส่วนลด

[![ฟิลด์ป้องกันไม่ให้มีส่วนลด](./media/prevent-discounts.png)](./media/prevent-discounts.png)
