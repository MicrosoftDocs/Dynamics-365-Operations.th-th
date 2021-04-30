---
title: เชื่อมโยงสินทรัพย์ถาวรกับสัญญาเช่า
description: หัวข้อนี้จะอธิบายวิธีการเชื่อมโยงสินทรัพย์ถาวรที่มีอยู่กับสัญญาเช่าใหม่
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 02a17b8c995e8aa97384d8b855afb688324017d6
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881359"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="e375f-103">เชื่อมโยงสินทรัพย์ถาวรกับสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="e375f-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e375f-104">หัวข้อนี้จะอธิบายวิธีการเชื่อมโยงสินทรัพย์ถาวรที่มีอยู่กับสัญญาเช่าใหม่</span><span class="sxs-lookup"><span data-stu-id="e375f-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="e375f-105">เมื่อคุณเชื่อมโยงสินทรัพย์ถาวรกับสัญญาเช่า มูลค่าของสิทธิ์การใช้สินทรัพย์ (ROU) ที่การรับรู้เริ่มต้น จะเป็นต้นทุนการซื้อสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="e375f-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="e375f-106">ก่อนที่คุณจะสามารถเชื่อมโยงสินทรัพย์ถาวรกับสัญญาเช่า คุณต้องสร้างเรกคอร์ดสำหรับสินทรัพย์ถาวรในสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="e375f-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="e375f-107">หลังจากนั้น บนหน้า **สรุปสัญญาเช่า** คุณต้องสร้างสัญญาเช่าและลิงค์สินทรัพย์กับสัญญาเช่านั้น</span><span class="sxs-lookup"><span data-stu-id="e375f-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="e375f-108">เพิ่มสัญญาเช่าโดยทำตามขั้นตอนใน [เพิ่มหรือคัดลอกสัญญาเช่า](add-lease.md)</span><span class="sxs-lookup"><span data-stu-id="e375f-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="e375f-109">บนหน้า **เพิ่มสัญญาเช่า** ในฟิลด์ **หมายเลขสินทรัพย์ถาวร** ให้เลือกสินทรัพย์ที่ยังไม่ได้ซื้อมา</span><span class="sxs-lookup"><span data-stu-id="e375f-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="e375f-110">เลือก **สมุดบัญชี** และยืนยันกำหนดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e375f-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="e375f-111">เลือก **การรับรู้เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="e375f-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="e375f-112">เลือก **สมุดรายวันการเช่าสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="e375f-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="e375f-113">รายการสมุดรายวันการรับรู้เริ่มต้นสำหรับสัญญาเช่า จะเดบิตสินทรัพย์ถาวรสำหรับยอดเงินที่โดยปกติจะถูกเดบิตไปที่บัญชีสิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e375f-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="e375f-114">ขณะนี้คุณสามารถดูชนิดธุรกรรมและสมุดบัญชีสำหรับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="e375f-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="e375f-115">เลือก  **รายละเอียดของสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="e375f-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="e375f-116">เลือก **รายการ** เพื่อดูรายการแต่ละบรรทัดสำหรับรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e375f-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="e375f-117">เลือกบรรทัดสมุดรายวันที่มีสินทรัพย์ แล้วจากนั้น เลือกแท็บ **สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="e375f-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="e375f-118">แท็บ **สินทรัพย์ถาวร** จะแสดงชนิดของธุรกรรมและสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="e375f-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="e375f-119">โดยค่าเริ่มต้น จะมีการตั้งค่าฟิลด์ **ชนิดธุรกรรม** เป็น **การซื้อสินทรัพย์** และฟิลด์ **สมุดบัญชี** ถูกกำหนดเป็นสมุดบัญชีปัจจุบันสำหรับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="e375f-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="e375f-120">หลังจากที่คุณลงรายการบัญชีสมุดรายวันการรับรู้เริ่มต้น ธุรกรรมจะปรากฏเป็นธุรกรรมการซื้อสินทรัพย์สำหรับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="e375f-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="e375f-121">ถ้าต้องการดูตารางธุรกรรม ให้ไปที่ **สินทรัพย์ถาวร \> สินทรัพย์ถาวร \> สินทรัพย์ถาวร** เลือกสินทรัพย์ที่เหมาะสม และจากนั้น เลือก **การประเมินค่า**</span><span class="sxs-lookup"><span data-stu-id="e375f-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="e375f-122">คุณควรเห็นว่าสมุดรายวันการรับรู้เริ่มต้นได้สร้างธุรกรรมการซื้อสินทรัพย์สำหรับสินทรัพย์ถาวรที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="e375f-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="e375f-123">ขณะนี้สามารถคิดค่าเสื่อมราคาสินทรัพย์ถาวรได้โดยใช้ฟังก์ชันการคิดค่าเสื่อมราคามาตรฐานในสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="e375f-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="e375f-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับค่าเสื่อมราคา ดูที่ [วิธีการคิดค่าเสื่อมราคาและแบบแผนการคิดค่าเสื่อมราคา](../fixed-assets/depreciation-methods-conventions.md)</span><span class="sxs-lookup"><span data-stu-id="e375f-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="e375f-125">ถ้าคุณเชื่อมโยงสินทรัพย์ถาวรกับสัญญาเช่า ปุ่ม **ค่าเสื่อมราคาสินทรัพย์** และ **การด้อยค่าของสินทรัพย์ของสัญญาเช่า** ถูกปิดใช้งานในการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e375f-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="e375f-126">คุณสามารถดูธุรกรรมค่าเสื่อมราคาของสินทรัพย์และการด้อยค่าของสินทรัพย์ของสัญญาเช่าจากสินทรัพย์ถาวรได้</span><span class="sxs-lookup"><span data-stu-id="e375f-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="e375f-127">ปุ่ม **ธุรกรรมสินทรัพย์** ซึ่งเปิดฟอร์มการสอบถาม จะถูกปิดใช้งานด้วย</span><span class="sxs-lookup"><span data-stu-id="e375f-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="e375f-128">นอกจากนี้ คุณยังสามารถเปิดฟอร์มการสอบถาม **ธุรกรรมสินทรัพย์** ในสินทรัพย์ถาวรได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="e375f-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
