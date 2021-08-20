---
title: คลังสินค้าในสมุดรายวันรายการเบิกสินค้าไม่มีการอัปเดตบนบรรทัด BOM
description: คลังสินค้าในสมุดรายวันรายการเบิกสินค้าไม่มีการอัปเดตบนบรรทัดสูตรการผลิต (BOM)
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 970930bbdd30b57a8374de7810bb3ece8cb19a7010b5ef19d90bfc39d09f172b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740562"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>คลังสินค้าในสมุดรายวันรายการเบิกสินค้าไม่มีการอัปเดตบนบรรทัด BOM

หมายเลข KB: 4614848

## <a name="symptoms"></a>อาการ

คลังสินค้าในสมุดรายวันรายการเบิกสินค้าไม่มีการอัปเดตบนบรรทัดสูตรการผลิต (BOM)

## <a name="resolution"></a>ความละเอียด

ระบบมีการทำงานตามที่ออกแบบ ถ้าบรรทัดสมุดรายวันรายการเบิกสินค้าถูกสร้างซึ่งมีการอ้างอิง (ผ่านรหัสล็อต) ไปยังบรรทัด BOM การผลิต คลังสินค้าในบรรทัด BOM การผลิตจะไม่มีการอัปเดต ถ้ามิติคลังสินค้าในบรรทัดสมุดรายวันรายการเบิกสินค้าการผลิตมีการเปลี่ยนแปลงในภายหลัง
