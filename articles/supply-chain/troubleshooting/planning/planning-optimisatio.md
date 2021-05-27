---
title: มีการสร้างแผนการใบสั่งซื้อเมื่อมีการซื้อภายในจำนวนวันที่ติดลบ
description: ถ้ารหัสความครอบคลุมเป็น ต่ำสุด/สูงสุด การเพิ่มประสิทธิภาพการวางแผนจะสร้างแผนการใบสั่งซื้อเมื่อมีการซื้ออยู่ภายในจำนวนวันที่ติดลบ
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026955"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="2cc55-103">มีการสร้างแผนการใบสั่งซื้อเมื่อมีการซื้อภายในจำนวนวันที่ติดลบ</span><span class="sxs-lookup"><span data-stu-id="2cc55-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="2cc55-104">หมายเลข KB: 4614298</span><span class="sxs-lookup"><span data-stu-id="2cc55-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="2cc55-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="2cc55-105">Symptoms</span></span>

<span data-ttu-id="2cc55-106">ถ้ารหัสความครอบคลุมเป็น *ต่ำสุด/สูงสุด* การเพิ่มประสิทธิภาพการวางแผนจะสร้างแผนการใบสั่งซื้อเมื่อมีการซื้ออยู่ภายในจำนวนวันที่ติดลบ</span><span class="sxs-lookup"><span data-stu-id="2cc55-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="2cc55-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="2cc55-107">Resolution</span></span>

<span data-ttu-id="2cc55-108">การเพิ่มประสิทธิภาพการวางแผนไม่สนับสนุนจำนวนวันที่ติดลบ</span><span class="sxs-lookup"><span data-stu-id="2cc55-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="2cc55-109">อย่างไรก็ตาม การตรวจสอบให้แน่ใจเสมอว่าแผนการใบสั่งจะไม่มีการจัดตารางการผลิตภายในระยะเวลารอคอยสินค้าที่สัมพันธ์กับวันที่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2cc55-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="2cc55-110">ตัวอย่างเช่น ระยะเวลารอคอยสินค้าจากการซื้อคือ 10 วัน และคาดว่าใบสั่งซื้อจะมาถึงแปดวันนับจากวันนี้</span><span class="sxs-lookup"><span data-stu-id="2cc55-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="2cc55-111">ในกรณีนี้ ใบสั่งซื้อจะใช้เป็นการจัดหาวัสดุเพื่อความต้องการที่เป็นห้าวันนับจากวันนี้</span><span class="sxs-lookup"><span data-stu-id="2cc55-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="2cc55-112">จึงขอแนะนำว่าคุณควรปรับปรุงระยะเวลารอคอยสินค้าเพื่อครอบคลุมสถานการณ์ทั้งหมด (หรือเกือบทั้งหมด) ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2cc55-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
