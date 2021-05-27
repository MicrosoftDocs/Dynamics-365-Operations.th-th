---
title: หมายเลขชุดงานจะถูกล้างข้อมูลเมื่อเลือกรหัสล็อตใหม่
description: เมื่อคุณทบทวนบรรทัดสมุดรายวันรายการเบิกสินค้า ค่าในฟิลด์หมายเลขชุดงานจะถูกล้างข้อมูลถ้าคุณเลือกค่าใหม่ในฟิลด์รหัสล็อต
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026934"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a><span data-ttu-id="49fc9-103">หมายเลขชุดงานจะถูกล้างข้อมูลเมื่อเลือกรหัสล็อตใหม่</span><span class="sxs-lookup"><span data-stu-id="49fc9-103">Batch number is cleared when a new lot ID is selected</span></span>

<span data-ttu-id="49fc9-104">หมายเลข KB: 4613107</span><span class="sxs-lookup"><span data-stu-id="49fc9-104">KB number: 4613107</span></span>

## <a name="symptoms"></a><span data-ttu-id="49fc9-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="49fc9-105">Symptoms</span></span>

<span data-ttu-id="49fc9-106">เมื่อคุณทบทวนบรรทัดสมุดรายวันรายการเบิกสินค้า ค่าในฟิลด์ **หมายเลขชุดงาน** จะถูกล้างข้อมูลถ้าคุณเลือกค่าใหม่ในฟิลด์ **รหัสล็อต**</span><span class="sxs-lookup"><span data-stu-id="49fc9-106">When you're reviewing a picking list journal line, the value in the **Batch number** field is cleared if you select a new value in the **Lot ID** field.</span></span>

## <a name="resolution"></a><span data-ttu-id="49fc9-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="49fc9-107">Resolution</span></span>

<span data-ttu-id="49fc9-108">ระบบมีการทำงานตามที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="49fc9-108">The system is behaving as designed.</span></span> <span data-ttu-id="49fc9-109">ถ้าคุณเปลี่ยนรหัสล็อต คุณจะเปลี่ยนบริบทสินค้า</span><span class="sxs-lookup"><span data-stu-id="49fc9-109">If you change the lot ID, you change the item context.</span></span> <span data-ttu-id="49fc9-110">ดังนั้นหมายเลขชุดงานจะถูกรีเซ็ต</span><span class="sxs-lookup"><span data-stu-id="49fc9-110">Therefore, the batch number is reset.</span></span>

<span data-ttu-id="49fc9-111">เมื่อต้องการเชื่อมโยงหมายเลขชุดงานกับรหัสล็อต คุณต้องตั้งค่ารหัสล็อตก่อน</span><span class="sxs-lookup"><span data-stu-id="49fc9-111">To associate the batch number with a lot ID, you must set the lot ID first.</span></span>
