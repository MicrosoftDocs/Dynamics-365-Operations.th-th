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
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a><span data-ttu-id="f26f0-103">คลังสินค้าในสมุดรายวันรายการเบิกสินค้าไม่มีการอัปเดตบนบรรทัด BOM</span><span class="sxs-lookup"><span data-stu-id="f26f0-103">The warehouse in the picking list journal isn't updated on a BOM line</span></span>

<span data-ttu-id="f26f0-104">หมายเลข KB: 4614848</span><span class="sxs-lookup"><span data-stu-id="f26f0-104">KB number: 4614848</span></span>

## <a name="symptoms"></a><span data-ttu-id="f26f0-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="f26f0-105">Symptoms</span></span>

<span data-ttu-id="f26f0-106">คลังสินค้าในสมุดรายวันรายการเบิกสินค้าไม่มีการอัปเดตบนบรรทัดสูตรการผลิต (BOM)</span><span class="sxs-lookup"><span data-stu-id="f26f0-106">The warehouse in the picking list journal isn't updated on a bill of materials (BOM) line.</span></span>

## <a name="resolution"></a><span data-ttu-id="f26f0-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="f26f0-107">Resolution</span></span>

<span data-ttu-id="f26f0-108">ระบบมีการทำงานตามที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f26f0-108">The system is behaving as designed.</span></span> <span data-ttu-id="f26f0-109">ถ้าบรรทัดสมุดรายวันรายการเบิกสินค้าถูกสร้างซึ่งมีการอ้างอิง (ผ่านรหัสล็อต) ไปยังบรรทัด BOM การผลิต คลังสินค้าในบรรทัด BOM การผลิตจะไม่มีการอัปเดต ถ้ามิติคลังสินค้าในบรรทัดสมุดรายวันรายการเบิกสินค้าการผลิตมีการเปลี่ยนแปลงในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="f26f0-109">If a picking list journal line is created that has a reference (via the lot ID) to a production BOM line, the warehouse on the production BOM line won't be updated if the warehouse dimension on the production picking list journal line is changed later.</span></span>
