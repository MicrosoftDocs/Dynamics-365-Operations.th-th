---
title: "ตั้งค่าคอนฟิก การจัดการค่าใช้จ่าย"
description: "บทความนี้อธิบายถึงการพิจารณาและตัดสินใจที่คุณต้องทำในระหว่างกระบวนการวางแผน ก่อนที่คุณจะตั้งค่าคอนฟิกการจัดการค่าใช้จ่ายใน Microsoft Dynamics 365 for Finance and Operations"
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aa7c7bfaf4301904e1b7ae242efaf8b660fb076a
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="configure-expense-management"></a><span data-ttu-id="0e87b-103">ตั้งค่าคอนฟิก การจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0e87b-103">Configure expense management</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="0e87b-104">หัวข้อนี้อธิบายถึงการพิจารณาและตัดสินใจที่คุณต้องทำในระหว่างกระบวนการวางแผน ก่อนที่คุณจะตั้งค่าคอนฟิกการจัดการค่าใช้จ่ายใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0e87b-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="0e87b-105">ในการจัดการค่าใช้จ่าย คุณสามารถจัดเก็บข้อมูลเกี่ยวกับวิธีการชำระเงิน ใบเบิกค่าเดินทาง รายงานค่าใช้จ่าย และนโยบายต่างๆ</span><span class="sxs-lookup"><span data-stu-id="0e87b-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="0e87b-106">เนื่องจากหลายการตัดสินใจที่คุณเลือกเมื่อคุณวางแผนการตั้งค่าคอนฟิกของคุณสำหรับการจัดการค่าใช้จ่าย ตามลำดับชั้นขององค์กรของคุณและโครงสร้างทางการเงิน คุณต้องอ้างอิงเอกสารการวางแผนสำหรับพื้นที่เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="0e87b-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="0e87b-107">ค่าใช้จ่ายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="0e87b-107">Intercompany expenses</span></span>

<span data-ttu-id="0e87b-108">เมื่อคุณเปิดใช้งานค่าใช้จ่ายระหว่างบริษัท คุณอนุญาตนิติบุคคลและพนักงานให้ทำให้เกิดค่าใช้จ่ายในนามของนิติบุคคลอื่น และเรียกเก็บการชำระเงินจากนิติบุคคลของการจ้างงานภายในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="0e87b-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="0e87b-109">ตัวอย่างเช่น พนักงานในนิติบุคคล A ทำโครงการสำหรับนิติบุคคล B เสร็จสิ้น และโครงการมีค่าเดินทางที่เกี่ยวข้องกับค่าใช้จ่ายเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="0e87b-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="0e87b-110">ถ้าเปิดใช้งานค่าใช้จ่ายระหว่างบริษัท พนักงานสามารถสร้างรายงานค่าใช้จ่ายที่จะลงรายการบัญชีค่าใช้จ่ายไปยังนิติบุคคล B และค่าใช้จ่ายจะต้องถูกชำระโดยนิติบุคคล A ถ้าองค์กรของคุณไม่มีหลายนิติบุคคล คุณไม่จำเป็นต้องเปิดใช้งานค่าใช้จ่ายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="0e87b-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="0e87b-111">**การตัดสินใจ:** คุณต้องการเปิดใช้งานค่าใช้จ่ายระหว่างบริษัทหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="0e87b-112">การจัดทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="0e87b-112">Financial management</span></span>

<span data-ttu-id="0e87b-113">การจัดการค่าใช้จ่ายมีการรวมเข้ากับการจัดทางการเงินขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="0e87b-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="0e87b-114">การตั้งค่าคอนฟิกของคุณจำนวนมากสำหรับการจัดการค่าใช้จ่ายจะขึ้นอยู่กับการตัดสินใจที่คุณได้ทำไว้เกี่ยวกับการเงินขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="0e87b-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="0e87b-115">ส่วนต่อไปนี้อธิบายถึงพื้นที่ต่าง ๆ ที่ต้องใช้การวางแผนและการตัดสินใจที่ขึ้นอยู่กับการตัดสินใจทางการเงินขององค์กรของคุณและคำแนะนำจากทีมงานผู้นำของคุณ</span><span class="sxs-lookup"><span data-stu-id="0e87b-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="0e87b-116">ค่าเบี้ยเลี้ยงต่อวัน</span><span class="sxs-lookup"><span data-stu-id="0e87b-116">Per diems</span></span>

<span data-ttu-id="0e87b-117">คุณต้องกำหนดค่าเบี้ยเลี้ยงต่อวันของพนักงานที่องค์กรของคุณมอบให้</span><span class="sxs-lookup"><span data-stu-id="0e87b-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="0e87b-118">เนื่องจากโดยทั่วไปใช้ค่าเบี้ยเลี้ยงต่อวันจะครอบคลุมค่าใช้จ่าย เช่นอาหาร ค่าที่พัก ค่าใช้จ่ายเบ็ดเตล็ดอื่น คุณสามารถสร้างกฎสำหรับค่าเบี้ยเลี้ยงต่อวันที่องค์กรของคุณเสนอให้</span><span class="sxs-lookup"><span data-stu-id="0e87b-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="0e87b-119">อัตราค่าเบี้ยเลี้ยงต่อวันสามารถขึ้นอยู่กับเวลาของปี สถานที่เดินทาง หรือทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="0e87b-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="0e87b-120">เมื่อคุณกำหนดกฎค่าเบี้ยเลี้ยงต่อวัน คุณสามารถระบุได้ว่าจะมีการหักเปอร์เซ็นต์ของอัตราค่าเบี้ยเลี้ยงต่อวันหากผู้ปฏิบัติงานได้รับประทานอาหารหรือได้รับบริการที่ไม่ต้องเสียค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0e87b-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="0e87b-121">คุณยังสามารถกำหนดระดับอัตราค่าเบี้ยเลี้ยงต่อวันเพื่อตั้งค่าจำนวนต่ำสุดและสูงสุดของชั่วโมงที่สามารถใช้อัตราค่าเบี้ยเลี้ยงต่อวันในการเดินทางของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="0e87b-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="0e87b-122">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="0e87b-122">**Decisions:**</span></span>

- <span data-ttu-id="0e87b-123">กฎค่าเบี้ยเลี้ยงต่อวันเริ่มต้นสำหรับวันแรกและวันสุดท้าย:</span><span class="sxs-lookup"><span data-stu-id="0e87b-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="0e87b-124">อะไรคือจำนวนชั่วโมงต่ำสุดที่พนักงานสามารถอ้างสิทธิ์สำหรับวันและยังคงได้รับยอดเงินประจำวันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="0e87b-125">มีการลดในยอดเงินที่เสนอไว้สำหรับค่าอาหารสำหรับวันแรกและวันสุดท้ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="0e87b-126">ถ้าไม่มีการลด เปอร์เซ็นต์ของการลดคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="0e87b-127">มีการลดในยอดเงินที่เสนอไว้สำหรับโรงแรมสำหรับวันแรกและวันสุดท้ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="0e87b-128">ถ้าไม่มีการลด เปอร์เซ็นต์ของการลดคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="0e87b-129">มีการลดในยอดเงินที่เสนอไว้สำหรับค่าใช้จ่ายอื่นๆที่เกิดขึ้นในวันแรกและวันสุดท้ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="0e87b-130">ถ้าไม่มีการลด เปอร์เซ็นต์ของการลดคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="0e87b-131">การสร้างกฎค่าเบี้ยเลี้ยงต่อวันเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="0e87b-131">Default per diem rules:</span></span>

    - <span data-ttu-id="0e87b-132">มีเปอร์เซ็นต์การปรับลดในค่าเบี้ยเลี้ยงต่อวันสำหรับแต่ละมื้ออาหาร ตัวอย่างเช่น ค่าอาหารฟรีหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="0e87b-133">ถ้าไม่มีการลด เปอร์เซ็นต์ของการลดสำหรับแต่ละมื้อคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="0e87b-134">มีการคำนวณการลดมื้ออาหารต่อวัน ต่อการเดินทาง หรือตามจำนวนมื้ออาหารต่อวันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="0e87b-135">ยอดเงินค่าเบี้ยเลี้ยงต่อวันควรปัดเศษตามวิธีการปกติหรือปัดเศษขึ้น</span><span class="sxs-lookup"><span data-stu-id="0e87b-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="0e87b-136">การคำนวณค่าเบี้ยเลี้ยงต่อวันยึดตามรอบระยะเวลา 24 ชั่วโมงหรือหนึ่งวันปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="0e87b-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="0e87b-137">กฎค่าเบี้ยเลี้ยงต่อวันที่ขึ้นอยู่กับสถานที่:</span><span class="sxs-lookup"><span data-stu-id="0e87b-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="0e87b-138">อัตราค่าเบี้ยเลี้ยงต่อวันแตกต่างกันขึ้นอยู่กับสถานที่ใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="0e87b-139">สถานที่ใดถูกรวมบ้าง</span><span class="sxs-lookup"><span data-stu-id="0e87b-139">What locations are included?</span></span>
    - <span data-ttu-id="0e87b-140">ถ้าอัตราค่าเบี้ยเลี้ยงต่อวันแตกต่างกันตามสถานที่ สำหรับสถานที่แต่ละแห่ง จำนวนเปอร์เซ็นต์ใดที่ระบุไว้สำหรับชนิดของค่าใช้จ่ายต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0e87b-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="0e87b-141">มื้ออาหาร</span><span class="sxs-lookup"><span data-stu-id="0e87b-141">Meals</span></span>
        - <span data-ttu-id="0e87b-142">โรงแรม</span><span class="sxs-lookup"><span data-stu-id="0e87b-142">Hotel</span></span>
        - <span data-ttu-id="0e87b-143">ค่าใช้จ่ายอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="0e87b-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="0e87b-144">สมุดรายวันการจัดการค่าใช้จ่ายและบัญชี</span><span class="sxs-lookup"><span data-stu-id="0e87b-144">Expense management journals and accounts</span></span>

<span data-ttu-id="0e87b-145">การจัดการค่าใช้จ่ายต้องการให้คุณใช้สมุดรายวันและบัญชีหลายเล่ม</span><span class="sxs-lookup"><span data-stu-id="0e87b-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="0e87b-146">คุณต้องตัดสินใจ ตัวอย่างเช่น ว่าจะใช้บัญชีเดียวกันสำหรับเงินทดรองจ่ายและข้อโต้แย้งเกี่ยวกับบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="0e87b-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="0e87b-147">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="0e87b-147">**Decisions:**</span></span>

- <span data-ttu-id="0e87b-148">สมุดรายวันบัญชีแยกประเภทใดที่จะลงรายการบัญชีรายงานค่าใช้จ่ายที่ได้รับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="0e87b-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="0e87b-149">บัญชีใดที่จะใช้สำหรับเงินทดรองจ่าย</span><span class="sxs-lookup"><span data-stu-id="0e87b-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="0e87b-150">ควรจะมีการลงรายการบัญชีเงินทดรองจ่ายทันทีหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="0e87b-151">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0e87b-151">Payment methods</span></span>

<span data-ttu-id="0e87b-152">เมื่อคุณอนุญาตให้พนักงานทำให้เกิดค่าใช้จ่ายในนามของธุรกิจของคุณ คุณต้องกำหนดวิธีการชำระเงินที่พนักงานได้รับอนุญาตให้ใช้</span><span class="sxs-lookup"><span data-stu-id="0e87b-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="0e87b-153">ตัวอย่างเช่น คุณอาจอนุญาตให้พนักงานใช้เงินสดหรือบัตรเครดิตของบริษัท</span><span class="sxs-lookup"><span data-stu-id="0e87b-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="0e87b-154">คุณอาจยังอนุญาตให้พนักงานใช้บัตรเครดิตส่วนบุคคล จากนั้นจ่ายคืนพนักงาน</span><span class="sxs-lookup"><span data-stu-id="0e87b-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="0e87b-155">คุณต้องทำการตัดสินใจต่าง ๆ ต่อไปนี้สำหรับแต่ละวิธีการชำระเงินที่คุณอนุญาต</span><span class="sxs-lookup"><span data-stu-id="0e87b-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="0e87b-156">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="0e87b-156">**Decisions:**</span></span>

- <span data-ttu-id="0e87b-157">วิธีการชำระเงินใดที่อนุญาต</span><span class="sxs-lookup"><span data-stu-id="0e87b-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="0e87b-158">ใครเป็นเจ้าของค่าใช้จ่ายวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0e87b-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="0e87b-159">มีชนิดบัญชีตรงข้ามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-159">Is there an offset account type?</span></span> <span data-ttu-id="0e87b-160">ถ้ามีบัญชีตรงข้าม บัญชีนั้นคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="0e87b-161">ถ้ามีบัญชีตรงข้าม บัญนั้นชีคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="0e87b-162">ถ้าวิธีการชำระเงินเป็นบัตรเครดิต วิธีการชำระเงินควรใช้เฉพาะกับธุรกรรมที่นำเข้าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="0e87b-163">ประเภทค่าใช้จ่ายและประเภทที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="0e87b-163">Expense categories and shared categories</span></span>

<span data-ttu-id="0e87b-164">เมื่อพนักงานสร้างรายงานค่าใช้จ่าย แต่ละค่าใช้จ่ายที่พวกเขาบันทึกจะต้องเชื่อมโยงกับประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0e87b-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="0e87b-165">ประเภทค่าใช้จ่ายจะสืบทอดมาจากประเภทที่ใช้ร่วมกันซึ่งสามารถใช้ร่วมกันระหว่างนิติบุคคลภายในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="0e87b-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="0e87b-166">ประเภทเหล่านี้ยังสามารถใช้ร่วมกันในการจัดการโครงการและการบัญชี ขึ้นอยู่กับวิธีการกำหนดโดยองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="0e87b-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="0e87b-167">กำหนดว่าประเภทที่ใช้ในการจัดการค่าใช้จ่ายจะถูกใช้ในการจัดการค่าใช้จ่ายเท่านั้นหรือควรถูกใช้ร่วมกันระหว่างการจัดการโครงการและการจัดการบัญชีและค่าใช้จ่ายโดยขึ้นอยู่กับคำนิยามขององค์กรของคุณและคำแนะนำจากทีมงาน</span><span class="sxs-lookup"><span data-stu-id="0e87b-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="0e87b-168">โปรดทราบว่าประเภทเหล่านี้สามารถใช้ร่วมกันระหว่างโครงการและค่าใช้จ่ายหรือโครงการและการผลิต แต่ไม่ได้ระหว่างค่าใช้จ่ายและการผลิต</span><span class="sxs-lookup"><span data-stu-id="0e87b-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="0e87b-169">คุณต้องทำการตัดสินใจต่าง ๆ ต่อไปนี้สำหรับแต่ละประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0e87b-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="0e87b-170">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="0e87b-170">**Decisions:**</span></span>

- <span data-ttu-id="0e87b-171">ประเภทของค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-171">What is the expense category?</span></span> <span data-ttu-id="0e87b-172">ตัวอย่างเช่น ประเภทสำหรับเที่ยวบิน โรงแรม หรือระยะไมล์</span><span class="sxs-lookup"><span data-stu-id="0e87b-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="0e87b-173">ประเภทของค่าใช้จ่ายสามารถใช้ในการจัดการและการบัญชีโครงการได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="0e87b-174">ชนิดของค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-174">What is the expense type?</span></span>
- <span data-ttu-id="0e87b-175">วิธีการชำระเงินเริ่มต้นสำหรับประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="0e87b-176">ต้องมีการแสดงรายการค่าใช้จ่ายในประเภทค่าใช้จ่ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="0e87b-177">บัญชีเริ่มต้นหลักสำหรับประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="0e87b-178">กลุ่มภาษีขายตามประเภทสินค้าเริ่มต้นสำหรับประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="0e87b-179">มีการอนุญาตให้ใช้วิธีการชำระเงินเพิ่มเติมสำหรับประเภทค่าใช้จ่ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="0e87b-180">ถ้าสามารถใช้วิธีการชำระเงินเพิ่มเติมได้ จะมีอะไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="0e87b-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="0e87b-181">มีประเภทย่อยภายในประเภทค่าใช้จ่ายนี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="0e87b-182">ถ้ามีประเภทย่อย คุณต้องทำการตัดสินใจต่าง ๆ ต่อไปนี้เช่นกัน:</span><span class="sxs-lookup"><span data-stu-id="0e87b-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="0e87b-183">มีประเภทย่อยใดที่ถูกแยกออกจากการขอคืนภาษีหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="0e87b-184">กลุ่มภาษีขายตามประเภทสินค้าของประเภทย่อยคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="0e87b-185">ถ้ามีใช้ประเภทค่าใช้จ่ายในการจัดการและการบัญชีโครงการ ให้ตอบคำถามที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="0e87b-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="0e87b-186">มิฉะนั้น เลื่อนไปยังส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="0e87b-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="0e87b-187">บัญชีต้นทุนใดจะใช้สำหรับค่าใช้จ่ายต่อไปนี้?</span><span class="sxs-lookup"><span data-stu-id="0e87b-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="0e87b-188">ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0e87b-188">Cost</span></span>
    - <span data-ttu-id="0e87b-189">การปันส่วนค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="0e87b-189">Payroll allocation</span></span>
    - <span data-ttu-id="0e87b-190">WIP - ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0e87b-190">WIP-cost value</span></span>
    - <span data-ttu-id="0e87b-191">ต้นทุน - สินค้า</span><span class="sxs-lookup"><span data-stu-id="0e87b-191">Cost-item</span></span>
    - <span data-ttu-id="0e87b-192">WIP - ต้นทุน - สินค้า</span><span class="sxs-lookup"><span data-stu-id="0e87b-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="0e87b-193">ขาดทุนสะสม</span><span class="sxs-lookup"><span data-stu-id="0e87b-193">Accrued loss</span></span>
    - <span data-ttu-id="0e87b-194">WIP - ขาดทุนสะสม</span><span class="sxs-lookup"><span data-stu-id="0e87b-194">WIP-accrued loss</span></span>

- <span data-ttu-id="0e87b-195">บัญชีรายได้ใดจะใช้สำหรับต่อไปนี้?</span><span class="sxs-lookup"><span data-stu-id="0e87b-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="0e87b-196">รายได้ที่ออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0e87b-196">Invoiced revenue</span></span>
    - <span data-ttu-id="0e87b-197">รายได้ค้างรับ - ยอดขาย</span><span class="sxs-lookup"><span data-stu-id="0e87b-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="0e87b-198">WIP - มูลค่าการขาย</span><span class="sxs-lookup"><span data-stu-id="0e87b-198">WIP-sales value</span></span>
    - <span data-ttu-id="0e87b-199">รายได้ค้างรับ - การผลิต</span><span class="sxs-lookup"><span data-stu-id="0e87b-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="0e87b-200">WIP - การผลิต</span><span class="sxs-lookup"><span data-stu-id="0e87b-200">WIP-production</span></span>
    - <span data-ttu-id="0e87b-201">รายได้ค้างรับ - กำไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="0e87b-202">WIP - กำไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-202">WIP-profit</span></span>
    - <span data-ttu-id="0e87b-203">รายได้ค้างรับ - การบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="0e87b-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="0e87b-204">WIP - การบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="0e87b-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="0e87b-205">ภาษี</span><span class="sxs-lookup"><span data-stu-id="0e87b-205">Taxes</span></span>

<span data-ttu-id="0e87b-206">สำหรับค่าใช้จ่ายที่เกี่ยวข้องกับภาษี คุณต้องกำหนดสิ่งที่จะรวมหรือเปิดใช้งานในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0e87b-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="0e87b-207">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="0e87b-207">**Decisions:**</span></span>

- <span data-ttu-id="0e87b-208">ภาษีขายจะรวมอยู่ในจำนวนค่าใช้จ่ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="0e87b-209">การขอคืนภาษีควรจะเปิดใช้งานในค่าใช้จ่ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e87b-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="0e87b-210">เมื่อคุณกำลังวางแผนบัญชีแยกประเภท ถ้าคุณตัดสินใจที่จะใช้ภาษีขายของสหรัฐอเมริกา และใช้กฎภาษี คุณไม่สามารถเปิดใช้งานการขอคืนภาษีค่าใช้จ่ายได้</span><span class="sxs-lookup"><span data-stu-id="0e87b-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="0e87b-211">(เมื่อต้องการใช้ภาษีขายของสหรัฐอเมริกา และใช้กฎภาษี ให้ตั้งค่าตัวเลือก **ใช้กฎภาษีสำหรับภาษีขาย** เป็น **ใช่**)</span><span class="sxs-lookup"><span data-stu-id="0e87b-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="0e87b-212">นโยบาย</span><span class="sxs-lookup"><span data-stu-id="0e87b-212">Policies</span></span>

<span data-ttu-id="0e87b-213">คุณสามารถช่วยให้องค์กรของคุณประหยัดเวลาและเงินเมื่อพนักงานทำให้เกิดค่าใช้จ่ายในนามได้โดยการสร้างนโยบายรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0e87b-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="0e87b-214">นโยบายช่วยให้แน่ใจว่าพนักงานยังอยู่ในงบประมาณ ให้ข้อมูลที่จำเป็นทั้งหมด และใช้จ่ายเงินตามความจำเป็นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0e87b-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="0e87b-215">คุณต้องทำการตัดสินใจต่าง ๆ ต่อไปนี้สำหรับแต่ละนโยบายรายงานค่าใช้จ่ายและแต่ละนโยบายการอนุมัติรายงานค่าใช้จ่ายที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="0e87b-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="0e87b-216">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="0e87b-216">**Decisions:**</span></span>

- <span data-ttu-id="0e87b-217">ชื่อของนโยบายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-217">What is the name of the policy?</span></span>
- <span data-ttu-id="0e87b-218">นโยบายค่าใช้จ่ายสำหรับอะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-218">What is the expense policy for?</span></span>
- <span data-ttu-id="0e87b-219">ถ้าคุณเคยตัดสินใจที่จะเปิดใช้งานค่าใช้จ่ายระหว่างบริษัท บริษัทใดในองค์กรของคุณที่จะใช้นโยบายนี้</span><span class="sxs-lookup"><span data-stu-id="0e87b-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="0e87b-220">เมื่อใดนโยบายจะมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="0e87b-220">When does the policy become effective?</span></span>
- <span data-ttu-id="0e87b-221">เมื่อใดโยบายจะหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="0e87b-221">When does the policy expire?</span></span>
- <span data-ttu-id="0e87b-222">กฎนโยบายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-222">What is the policy rule?</span></span>
- <span data-ttu-id="0e87b-223">ผลลัพธ์ของกฎนโยบายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="0e87b-223">What is the outcome of the policy rule?</span></span>

