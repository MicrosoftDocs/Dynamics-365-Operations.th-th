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
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026940"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>คลังสินค้าในสมุดรายวันรายการเบิกสินค้าไม่มีการอัปเดตบนบรรทัด BOM

หมายเลข KB: 4614848

## <a name="symptoms"></a>อาการ

คลังสินค้าในสมุดรายวันรายการเบิกสินค้าไม่มีการอัปเดตบนบรรทัดสูตรการผลิต (BOM)

## <a name="resolution"></a>ความละเอียด

ระบบมีการทำงานตามที่ออกแบบ ถ้าบรรทัดสมุดรายวันรายการเบิกสินค้าถูกสร้างซึ่งมีการอ้างอิง (ผ่านรหัสล็อต) ไปยังบรรทัด BOM การผลิต คลังสินค้าในบรรทัด BOM การผลิตจะไม่มีการอัปเดต ถ้ามิติคลังสินค้าในบรรทัดสมุดรายวันรายการเบิกสินค้าการผลิตมีการเปลี่ยนแปลงในภายหลัง
