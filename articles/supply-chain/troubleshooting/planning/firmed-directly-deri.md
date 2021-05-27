---
title: ใบสั่งที่ยืนยันที่ได้รับมาโดยตรงจะถูกประมวลผลโดยลำดับงานในระหว่างการตรวจทาน
description: ใบสั่งที่ยืนยันที่ได้รับมาโดยตรงจะถูกประมวลผลโดยลำดับงานที่มีสถานะระหว่างการตรวจทาน
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026957"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="46896-103">ใบสั่งที่ยืนยันที่ได้รับมาโดยตรงจะถูกประมวลผลโดยลำดับงานในระหว่างการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="46896-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="46896-104">หมายเลข KB: 4612450</span><span class="sxs-lookup"><span data-stu-id="46896-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="46896-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="46896-105">Symptoms</span></span>

<span data-ttu-id="46896-106">ใบสั่งที่ยืนยันที่ได้รับมาโดยตรงจะถูกประมวลผลโดยลำดับงานที่มีสถานะ *ระหว่างการตรวจทาน*</span><span class="sxs-lookup"><span data-stu-id="46896-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="46896-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="46896-107">Resolution</span></span>

<span data-ttu-id="46896-108">เมื่อการติดตามการเปลี่ยนแปลงกรณีเปิดใช้งาน สถานะ *ระหว่างการตรวจทาน* จะกำหนดให้ใบสั่งที่ได้รับมาซึ่งยืนยันแล้ว (ใบสั่งซื้อของผู้รับเหมารายย่อย)</span><span class="sxs-lookup"><span data-stu-id="46896-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="46896-109">ดังนั้นถ้าใบสั่งซื้อได้รับมา (ใบสั่งซื้อของผู้รับเหมารายย่อย) ใบสั่งซื้อนั้นจะถูกส่งไปยังลำดับงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="46896-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="46896-110">ถ้าใบสั่งซื้อเป็นแผนการใบสั่งซื้อที่ยืนยันแล้ว ใบสั่งซื้อจะได้รับการอนุมัติโดยอัตโนมัติเพื่อให้แน่ใจว่ากลไกจัดการวางแผนจะไม่สร้างแผนการใบสั่งใหม่ในขณะที่ใบสั่งซื้อยังคงอยู่ในสถานะ *ร่าง*</span><span class="sxs-lookup"><span data-stu-id="46896-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
