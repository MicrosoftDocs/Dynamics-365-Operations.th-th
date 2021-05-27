---
title: มีการพิมพ์ป้ายชื่อเพียงป้ายชื่อเดียวหลายหัวข้อบนใบรับสินค้าเดียว
description: มีการพิมพ์ป้ายชื่อเพียงป้ายชื่อเดียวหลายหัวข้อบนใบรับสินค้าเดียว
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026948"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="3d769-103">มีการพิมพ์ป้ายชื่อเพียงป้ายชื่อเดียวหลายหัวข้อบนใบรับสินค้าเดียว</span><span class="sxs-lookup"><span data-stu-id="3d769-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="3d769-104">หมายเลข KB: 4614667</span><span class="sxs-lookup"><span data-stu-id="3d769-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="3d769-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="3d769-105">Symptoms</span></span>

<span data-ttu-id="3d769-106">ส่วนหัวของงานหลายหัวข้อสร้างขึ้นเพื่อป้ายทะเบียนเป้าหมายเดียวกันโดยเป็นส่วนหนึ่งของเหตุการณ์การรับสินค้าตามแอปคลังสินค้าเดียว</span><span class="sxs-lookup"><span data-stu-id="3d769-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="3d769-107">แต่จะมีการพิมพ์ป้ายชื่อทะเบียนเพียงป้ายชื่อเดียวเมื่อได้รับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3d769-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="3d769-108">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="3d769-108">Resolution</span></span>

<span data-ttu-id="3d769-109">ระบบมีการทำงานตามที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="3d769-109">The system is behaving as designed.</span></span>

<span data-ttu-id="3d769-110">ในการออกแบบปัจจุบัน จะมีการสร้างป้ายชื่อทะเบียนเดียวเสมอ ไม่ว่าจํานวนของหัวข้องานและชุดรายการงานที่มีอยู่จะเป็นอย่างไรก็ตาม</span><span class="sxs-lookup"><span data-stu-id="3d769-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="3d769-111">ป้ายชื่อที่สร้างมีข้อมูลเพียงชุดเดียว</span><span class="sxs-lookup"><span data-stu-id="3d769-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="3d769-112">เมื่อต้องการแก้ไขปัญหานี้ ให้ตรวจสอบให้แน่ใจว่าการสร้างหัวข้อของงานได้รับการแม็ปกับป้ายทะเบียนเป้าหมายเพียงป้ายเดียวเสมอ</span><span class="sxs-lookup"><span data-stu-id="3d769-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
