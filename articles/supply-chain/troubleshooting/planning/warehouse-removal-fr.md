---
title: คุณไม่สามารถลบมิติการคาดการณ์ความต้องการคลังสินค้าออกจากบรรทัดการคาดการ
description: คุณไม่สามารถลบมิติการคาดการณ์ความต้องการคลังสินค้าออกจากบรรทัดการคาดการ
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026952"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="3a3ce-103">คุณไม่สามารถลบมิติการคาดการณ์ความต้องการคลังสินค้าออกจากบรรทัดการคาดการ</span><span class="sxs-lookup"><span data-stu-id="3a3ce-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="3a3ce-104">หมายเลข KB: 4614408</span><span class="sxs-lookup"><span data-stu-id="3a3ce-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="3a3ce-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="3a3ce-105">Symptoms</span></span>

<span data-ttu-id="3a3ce-106">ปัญหานี้จะเกิดขึ้นเมื่อมิติ **คลังสินค้า** ไม่ได้ได้รับการมอบหมายบนแท็บ **มิติการคาดการณ์** บนหน้า **พารามิเตอร์การคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="3a3ce-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="3a3ce-107">อย่างไรก็ตาม คอลัมน์ **คลังสินค้า** จะแสดง บนหน้า **การคาดการณ์ความต้องการ** (**การวางแผนหลัก \> การคาดการณ์ \> เอนทิตีการคาดการณ์ด้วยตนเอง \> รายการการคาดการณ์ความต้องการ**)</span><span class="sxs-lookup"><span data-stu-id="3a3ce-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="3a3ce-108">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="3a3ce-108">Resolution</span></span>

<span data-ttu-id="3a3ce-109">การตั้งค่าบนแท็บ **มิติการคาดการณ์** บนหน้า **พารามิเตอร์การคาดการณ์ความต้องการ** จะไม่ส่งผลต่อหน้า **การคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="3a3ce-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="3a3ce-110">โดยจะควบคุมการคาดการณ์พื้นฐานที่สร้างขึ้นและแสดงในการคาดการณ์ความต้องการที่ปรับปรุงแล้ว</span><span class="sxs-lookup"><span data-stu-id="3a3ce-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="3a3ce-111">อย่างไรก็ตาม มิติเหล่านั้นไม่ได้ควบคุมมิติที่ต้องใช้ในการคาดการณ์ความต้องการ "จริง"</span><span class="sxs-lookup"><span data-stu-id="3a3ce-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="3a3ce-112">โดยการสร้างเรกคอร์ดที่แสดงอยู่บนหน้า **การคาดการณ์ความต้องการที่ปรับปรุงแล้ว** คุณสามารถแปลงเรกคอร์ดเหล่านั้นเป็นรายการการคาดการณ์ "จริง" ของแบบจำลองการคาดการณ์ได้</span><span class="sxs-lookup"><span data-stu-id="3a3ce-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="3a3ce-113">จากนั้นสามารถใช้แบบจำลองนั้นกับการวางแผนหลักได้</span><span class="sxs-lookup"><span data-stu-id="3a3ce-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="3a3ce-114">บนหน้า **การคาดการณ์ความต้องการ** มิติของการคาดการณ์ "จริง" ที่แสดงบนบรรทัดการคาดการณ์ความต้องการเป็นส่วนหนึ่งของมิติสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="3a3ce-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="3a3ce-115">(ลักษณะการทำงานนี้จะคล้ายกับลักษณะการทำงานของบรรทัดใบสั่งขาย) ถ้าระบบของคุณไม่มีการตั้งค่าให้ใช้ **คลังสินค้า** เป็นมิติสินค้าคงคลังบังคับ คุณสามารถเลือกเลือกตั้งหน้าเพื่อซ่อนคอลัมน์ได้</span><span class="sxs-lookup"><span data-stu-id="3a3ce-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
