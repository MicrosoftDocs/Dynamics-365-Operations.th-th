---
title: สถานีการจัดส่งไม่แสดงบันทึกผลิตภัณฑ์
description: สถานีการจัดส่งไม่แสดงบันทึกผลิตภัณฑ์
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSPack
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: bf64de3e67c1000dad9d5b37fffe622ae0e300b3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026946"
---
# <a name="packing-station-doesnt-show-product-notes"></a><span data-ttu-id="5bd5f-103">สถานีการจัดส่งไม่แสดงบันทึกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5bd5f-103">Packing station doesn't show product notes</span></span>

<span data-ttu-id="5bd5f-104">หมายเลข KB: 4614615</span><span class="sxs-lookup"><span data-stu-id="5bd5f-104">KB number: 4614615</span></span>

## <a name="symptoms"></a><span data-ttu-id="5bd5f-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="5bd5f-105">Symptoms</span></span>

<span data-ttu-id="5bd5f-106">บันทึกการจัดส่งไม่แสดงอยู่ในฟอร์มการจัดส่ง เมื่อคําแนะนําในการจัดส่งถูกเพิ่มเป็นเอกสารแนบกับผลิตภัณฑ์หลักหรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="5bd5f-106">Packing notes aren't shown in the packing form when the packing instructions are added as an attachment to a product master or a product variant.</span></span>

## <a name="resolution"></a><span data-ttu-id="5bd5f-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="5bd5f-107">Resolution</span></span>

<span data-ttu-id="5bd5f-108">ระบบมีการทำงานตามที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="5bd5f-108">The system is behaving as designed.</span></span>

<span data-ttu-id="5bd5f-109">ตรรกะปัจจุบันที่แสดงบันทึกการจัดส่งในฟอร์มการจัดส่งกําหนดให้ต้องเชื่อมโยงบันทึกกับการจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="5bd5f-109">The current logic for showing packing notes in the packing form requires that the notes be associated with the shipments.</span></span>
