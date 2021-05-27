---
title: เมื่อปริมาณตามน้ําหนักจริงถูกแบ่ง ระบบจะใช้ปริมาณต่ำสุดแทนปริมาณที่ระบุ
description: เมื่อปริมาณตามน้ําหนักจริงถูกแบ่งออกเป็นชุด ฟิลด์ปริมาณการเบิกสินค้าจะใช้ปริมาณต่ำสุดที่ตั้งค่าไว้ของสินค้า ไม่ใช่ปริมาณที่ระบุ
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026958"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="1222f-103">เมื่อปริมาณตามน้ําหนักจริงถูกแบ่ง ระบบจะใช้ปริมาณต่ำสุดแทนปริมาณที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1222f-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="1222f-104">หมายเลข KB: 4612073</span><span class="sxs-lookup"><span data-stu-id="1222f-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="1222f-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="1222f-105">Symptoms</span></span>

<span data-ttu-id="1222f-106">เมื่อปริมาณตามน้ําหนักจริงถูกแบ่งออกเป็นชุด ฟิลด์ **ปริมาณการเบิกสินค้า** จะใช้ปริมาณต่ำสุดที่ตั้งค่าไว้ของสินค้า ไม่ใช่ปริมาณที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1222f-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="1222f-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="1222f-107">Resolution</span></span>

<span data-ttu-id="1222f-108">ระบบมีการทำงานตามที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="1222f-108">The system is behaving as designed.</span></span> <span data-ttu-id="1222f-109">ระบบใช้การตั้งค่าปริมาณต่ำสุดของสินค้าแต่ละรายการในการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="1222f-109">The system uses each item's minimum quantity setup for picking.</span></span>
