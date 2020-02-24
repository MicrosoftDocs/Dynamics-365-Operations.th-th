---
title: การประมวลผลใบเสร็จค่าใช้จ่าย
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการประมวลผลการรู้จำอักขระด้วยแสง (OCR) สำหรับใบเสร็จรับเงิน คุณลักษณะนี้ได้รับการออกแบบมาเพื่อปรับปรุงประสบการณ์การใช้งานของผู้ใช้ เมื่อมีการสร้างรายงานค่าใช้จ่ายใน Microsoft Dynamics 365 Finance
author: stevensporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ead9039de63e2cf4f3a7faddd1702b9614d7f99
ms.sourcegitcommit: 6aceca43c53c4dde46954c0b6b855d488eb44ed2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027914"
---
# <a name="public-preview-expense-receipt-processing"></a><span data-ttu-id="e321c-104">การแสดงตัวอย่างสาธารณะ: การประมวลผลใบเสร็จค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="e321c-104">Public Preview: Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


<span data-ttu-id="e321c-105">มีการปรับปรุงรายการค่าใช้จ่ายโดยใช้การแนะนำในการประมวลผลการรู้จำอักขระด้วยแสง (OCR) สำหรับใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="e321c-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="e321c-106">คุณลักษณะนี้ได้รับการออกแบบมาเพื่อปรับปรุงประสบการณ์การใช้งานของผู้ใช้ เมื่อมีการสร้างรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="e321c-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="e321c-107">คุณลักษณะสำคัญ</span><span class="sxs-lookup"><span data-stu-id="e321c-107">Key features</span></span>

- <span data-ttu-id="e321c-108">ชื่อร้านค้า วันที่ และยอดเงินรวม จะถูกแยกจากใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="e321c-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="e321c-109">คุณลักษณะพยายามจับคู่ใบเสร็จรับเงินที่ยังไม่ได้แนบกับธุรกรรมค่าใช้จ่ายที่ยังไม่ได้แนบ</span><span class="sxs-lookup"><span data-stu-id="e321c-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="e321c-110">ผู้ใช้สามารถสร้างธุรกรรมค่าใช้จ่ายที่ป้อนด้วยตนเองจากใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="e321c-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="e321c-111">ตัวอย่างการใช้</span><span class="sxs-lookup"><span data-stu-id="e321c-111">Usage examples</span></span>

- <span data-ttu-id="e321c-112">**แนบใบเสร็จรับเงินที่มีธุรกรรมบัตรเครดิตโดยอัตโนมัติ เมื่อสร้างรายงานค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="e321c-112">**Automatically attach receipts that include credit card transactions when an expense report is created.**</span></span>

    1. <span data-ttu-id="e321c-113">เปิดพื้นที่ทำงาน **การจัดการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="e321c-113">Open the **Expense management** workspace.</span></span>
    2. <span data-ttu-id="e321c-114">บนแท็บ **ใบเสร็จรับเงิน** ให้ตรวจสอบว่ามีใบเสร็จรับเงินที่ยังไม่ได้แนบอยู่</span><span class="sxs-lookup"><span data-stu-id="e321c-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="e321c-115">นอกจากนี้ คุณยังสามารถอัพโหลดใบเสร็จรับเงินในแท็บ **ใบเสร็จรับเงิน**</span><span class="sxs-lookup"><span data-stu-id="e321c-115">You can also upload receipts on the **Receipts** tab.</span></span>
    3. <span data-ttu-id="e321c-116">บนแท็บ **ค่าใช้จ่าย** ให้ตรวจสอบว่ามีค่าใช้จ่ายอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="e321c-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="e321c-117">โดยทั่วไป ผู้ดูแลระบบค่าใช้จ่ายจะนำเข้าค่าใช้จ่ายเหล่านี้จากผู้ให้บริการบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="e321c-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
    4. <span data-ttu-id="e321c-118">เลือก **รายงานค่าใช้จ่ายใหม่**</span><span class="sxs-lookup"><span data-stu-id="e321c-118">Select **New expense report**.</span></span> <span data-ttu-id="e321c-119">โปรดสังเกตว่าคุณสามารถรวมค่าใช้จ่ายและใบเสร็จรับเงินในขณะนี้ได้เช่นกัน เมื่อคุณสร้างรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="e321c-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="e321c-120">ถ้าคุณเพิ่มทั้งค่าใช้จ่ายและใบเสร็จรับเงิน การจับคู่อัตโนมัติของใบเสร็จรับเงินกับค่าใช้จ่ายจะถูกทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="e321c-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

- <span data-ttu-id="e321c-121">**สร้างค่าใช้จ่าย หรือจับคู่ค่าใช้จ่ายจากใบเสร็จรับเงิน**</span><span class="sxs-lookup"><span data-stu-id="e321c-121">**Create an expense, or match an expense from a receipt.**</span></span>

    1. <span data-ttu-id="e321c-122">ในรายงานค่าใช้จ่าย บนแท็บ **ใบเสร็จรับเงิน** ให้แนบใบเสร็จรับเงินโดยเลือก **เพิ่มใบเสร็จรับเงิน**</span><span class="sxs-lookup"><span data-stu-id="e321c-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
    2. <span data-ttu-id="e321c-123">ภายใต้รูปที่อัพโหลดของใบเสร็จรับเงิน ให้สังเกตตัวเลือก **สร้าง** และ **จับคู่**</span><span class="sxs-lookup"><span data-stu-id="e321c-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

        - <span data-ttu-id="e321c-124">เลือก **สร้าง** เพื่อสร้างธุรกรรมค่าใช้จ่ายที่ป้อนด้วยตนเอง และกรอกค่าที่ถูกแยกจากใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="e321c-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
        - <span data-ttu-id="e321c-125">ถ้าคุณเลือก **จับคู่** ระบบจะพยายามจับคู่ค่าใช้จ่ายที่มีอยู่กับใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="e321c-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="e321c-126">การติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="e321c-126">Installation</span></span>

<span data-ttu-id="e321c-127">คุณลักษณะนี้จะทำงานร่วมกับคุณลักษณะ **รายงานค่าใช้จ่ายที่คิดใหม่** เพื่อช่วยให้ประสบการณ์ค่าใช้จ่ายง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="e321c-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span>

<span data-ttu-id="e321c-128">เมื่อต้องการใช้ความสามารถในการใช้ค่าใช้จ่ายขั้นสูงเหล่านี้ ให้ติดตั้ง Add-in บริการการจัดการค่าใช้จ่ายสำหรับ Microsoft Dynamics 365 Finance และเปิดใช้งานคุณลักษณะในอินสแตนซ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e321c-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="e321c-129">คุณสามารถเข้าถึง add-in จากโครงการของคุณใน Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e321c-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="e321c-130">ลงชื่อเข้าใช้ LCS และเปิดสภาพแวดล้อมที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="e321c-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="e321c-131">ไปที่ **รายละเอียดแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="e321c-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="e321c-132">เลือก **เก็บรักษา** หรือเลื่อนลงไปที่แท็บด่วน **Add-in ของสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="e321c-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="e321c-133">เลือก **การติดตั้ง Add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="e321c-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="e321c-134">เลือก **บริการจัดการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="e321c-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="e321c-135">ปฏิบัติตามคำแนะนำการติดตั้ง และยอมรับข้อกำหนดและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="e321c-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="e321c-136">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="e321c-136">Select **Install**.</span></span>

<span data-ttu-id="e321c-137">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** เปิดใช้งานคุณลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e321c-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="e321c-138">คิดรูปแบบรายงานค่าใช้จ่ายใหม่แล้ว</span><span class="sxs-lookup"><span data-stu-id="e321c-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="e321c-139">จับคู่อัตโนมัติและสร้างค่าใช้จ่ายจากใบเสร็จ</span><span class="sxs-lookup"><span data-stu-id="e321c-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="e321c-140">เมื่อคุณเปิดใช้งานคุณลักษณะเหล่านี้ การดำเนินการต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="e321c-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="e321c-141">พื้นที่ทำงาน **การจัดการค่าใช้จ่าย** ที่มีอยู่จะถูกแทนที่ด้วยพื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="e321c-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="e321c-142">มีการเพิ่มรายการเมนูใหม่สำหรับการมองเห็นฟิลด์ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="e321c-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="e321c-143">คุณยังสามารถเปิดหน้า **รายงานค่าใช้จ่าย** ก่อนหน้านี้ โดยไปที่ **การจัดการค่าใช้จ่าย > ค่าใช้จ่ายของฉัน > รายงานค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="e321c-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="e321c-144">ลำดับงานและการอนุมัติใดๆ ยังคงนำคุณไปยังหน้ารายงานค่าใช้จ่ายที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="e321c-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="e321c-145">ใบเสร็จรับเงินจะถูกประมวลผลโดยผ่านทาง Microsoft Azure Cognitive Services และข้อมูลเมตาจะถูกแยกและเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="e321c-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="e321c-146">มีการเพิ่มตัวเลือกซึ่งช่วยให้คุณสามารถสร้างรายงานค่าใช้จ่ายที่มีใบเสร็จรับเงินที่จับคู่ที่ยังไม่ได้ถูกแนบ</span><span class="sxs-lookup"><span data-stu-id="e321c-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="e321c-147">ตัวเลือกที่บวกเพิ่มเข้าในรายงานค่าใช้จ่ายจะช่วยให้คุณสามารถสร้างรายการค่าใช้จ่ายจากใบเสร็จรับเงิน หรือพยายามจับคู่ใบเสร็จรับเงินที่มีอยู่กับรายการค่าใช้จ่ายที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="e321c-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="e321c-148">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะที่คิดรูปแบบรายงานค่าใช้จ่ายใหม่แล้ว ดู [คิดรูปแบบรายงานค่าใช้จ่ายใหม่แล้ว](ExpenseWorkspaceNew.md)</span><span class="sxs-lookup"><span data-stu-id="e321c-148">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="e321c-149">คำถามที่ถามบ่อย</span><span class="sxs-lookup"><span data-stu-id="e321c-149">Frequently asked questions</span></span>

<span data-ttu-id="e321c-150">**Microsoft ใช้ข้อมูลของฉันสำหรับแบบจำลองหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="e321c-150">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="e321c-151">ไม่ Microsoft ได้สร้าง Machine Learning ทั่วไปสำหรับบริการการประมวลผลใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="e321c-151">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="e321c-152">แบบจำลองนี้ไม่ได้ขึ้นอยู่กับใบเสร็จรับเงินที่คุณอัพโหลด</span><span class="sxs-lookup"><span data-stu-id="e321c-152">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="e321c-153">**คุณลักษณะนี้พร้อมใช้งานและมีการประมวลผลที่ใด**</span><span class="sxs-lookup"><span data-stu-id="e321c-153">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="e321c-154">ในปัจจุบัน ประเทศสหรัฐอเมริกาได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="e321c-154">Currently, the United States is supported.</span></span>

<span data-ttu-id="e321c-155">**ใบเสร็จรับเงินของฉันอยู่ที่ไหน**</span><span class="sxs-lookup"><span data-stu-id="e321c-155">**Where do my receipts go?**</span></span>

<span data-ttu-id="e321c-156">การเงินจะติดต่อ Cognitive Services เพื่อแยกข้อมูลฟิลด์</span><span class="sxs-lookup"><span data-stu-id="e321c-156">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="e321c-157">Cognitive Services จะรักษาสำเนาของใบเสร็จรับเงินของคุณให้นานถึง 24 ชั่วโมง ในขณะที่การประมวลผลเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="e321c-157">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="e321c-158">หลังจากเสร็จสิ้นการประมวลผลแล้ว Cognitive Services จะลบใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="e321c-158">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="e321c-159">ใบเสร็จรับเงินยังคงจัดเก็บอยู่ในการเงิน</span><span class="sxs-lookup"><span data-stu-id="e321c-159">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="e321c-160">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เปิดใช้งานความเข้าใจในใบเสร็จรับเงินด้วยความสามารถใหม่ของ Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)</span><span class="sxs-lookup"><span data-stu-id="e321c-160">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
