---
title: แบบแผนการเช่าสินทรัพย์
description: หัวข้อนี้อธิบายแบบแผนสินทรัพย์ที่ให้เช่า
author: moaamer
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e6450438a6e8c594590df3cc4502895913f50d01
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842405"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="b9564-103">แบบแผนการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b9564-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="b9564-104">หัวข้อนี้อธิบายแบบแผนสินทรัพย์ที่ให้เช่า</span><span class="sxs-lookup"><span data-stu-id="b9564-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="b9564-105">แบบแผนการเช่าใช้ในการระบุวันที่เริ่มต้นของสมุดบัญชีการเช่า</span><span class="sxs-lookup"><span data-stu-id="b9564-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="b9564-106">หากแบบแผนการเช่าได้รับการตั้งค่าเป็น **ไม่มี** วันที่เริ่มต้นจะเหมือนกับวันที่เริ่มต้นของการเช่า (กล่าวคือ ค่าของฟิลด์ **วันที่เริ่มต้นการเช่า** )</span><span class="sxs-lookup"><span data-stu-id="b9564-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="b9564-107">หากแบบแผนการเช่าได้รับการตั้งค่าเป็น **เต็มเดือน** วันที่เริ่มต้นคือวันแรกของเดือนที่เป็นวันที่เริ่มต้นของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="b9564-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="b9564-108">วันที่เริ่มต้นจะระบุวันที่เริ่มต้นของรอบระยะเวลาที่ตัดบัญชีหนี้สินและการจัดกำหนดการการคิดค่าเสื่อมราคาสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b9564-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="b9564-109">ดอกเบี้ยจ่ายและค่าเสื่อมราคาจะลงรายการบัญชีในวันที่สิ้นสุดรอบระยะเวลาของกำหนดการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="b9564-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="b9564-110">การรับรู้เบื้องต้นและการปรับปรุงรายการสมุดรายวันมีการลงรายการบัญชีไว้ในวันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b9564-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="b9564-111">ลักษณะการทำงานของแบบแผนการเช่าจะต้องเปิดใช้งานผ่านการจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="b9564-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="b9564-112">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้ค้นหาและเลือกคุณลักษณะที่ชื่อคุณลักษณะ **แบบแผนการเช่าสำหรับการเช่าสินทรัพย์** แล้วเลือก **เปิดใช้งานตอนนี้**</span><span class="sxs-lookup"><span data-stu-id="b9564-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="b9564-113">มีการกำหนดแบบแผนการเช่าให้กับการตั้งค่าของสมุดบัญชีสินทรัพย์การเช่า</span><span class="sxs-lookup"><span data-stu-id="b9564-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="b9564-114">เมื่อต้องการดูหรือกําหนดแบบแผนการเช่า ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b9564-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="b9564-115">ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> สมุดบัญชีสัญญาเช่า**</span><span class="sxs-lookup"><span data-stu-id="b9564-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="b9564-116">ในฟิลด์ **แบบแผนการเช่า** ให้เลือกหนึ่งในค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b9564-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="b9564-117">ข้อตกลงการเช่า</span><span class="sxs-lookup"><span data-stu-id="b9564-117">Leasing convention</span></span> | <span data-ttu-id="b9564-118">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="b9564-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="b9564-119">None</span><span class="sxs-lookup"><span data-stu-id="b9564-119">None</span></span>               | <span data-ttu-id="b9564-120">การตัดบัญชีหนี้สินและกำหนดการคิดค่าเสื่อมราคาสินทรัพย์จะเริ่มต้นในวันที่เริ่มต้นของการเช่า เนื่องจากวันที่เริ่มต้นจะเท่ากับวันที่เริ่มต้นการเช่า</span><span class="sxs-lookup"><span data-stu-id="b9564-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="b9564-121">วันที่สิ้นสุดคือหนึ่งเดือนหลังจากนั้น</span><span class="sxs-lookup"><span data-stu-id="b9564-121">The end date is one month later.</span></span> <span data-ttu-id="b9564-122">แบบแผนการเช่านี้ไม่ได้รับประกันว่าจะมีการลงรายการบัญชีดอกเบี้ยในวันสุดท้ายของแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="b9564-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="b9564-123">เต็มเดือน</span><span class="sxs-lookup"><span data-stu-id="b9564-123">Full month</span></span>         | <span data-ttu-id="b9564-124">สำหรับสัญญาเช่าที่มีวันที่เริ่มต้นที่เกิดขึ้นเมื่อใดก็ได้ในระหว่างเดือน การตัดบัญชีหนี้สินและกำหนดการการคิดค่าเสื่อมราคาสินทรัพย์จะเริ่มต้นค่าใช้จ่ายค้างจ่ายในวันแรกของเดือนนั้น</span><span class="sxs-lookup"><span data-stu-id="b9564-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="b9564-125">แบบแผนการเช่านี้ช่วยให้มั่นใจว่าจะมีการตั้งค้างรับดอกเบี้ยในวันสุดท้ายของแต่ละเดือนตลอดทั้งเดือน</span><span class="sxs-lookup"><span data-stu-id="b9564-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="b9564-126">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b9564-126">Select **Save**.</span></span>

<span data-ttu-id="b9564-127">เมื่อมีการสร้างสัญญาเช่า วันที่เริ่มต้นของสมุดบัญชีแต่ละเล่มจะมีการป้อนข้อมูลโดยอัตโนมัติตามวันที่เริ่มต้นที่ป้อนไว้ให้กับสัญญาเช่าและแบบแผนการเช่าที่ระบุไว้ในสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9564-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]