---
title: มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Dynamics 365 Supply Chain Management 10.0.6 (พฤศจิกายน 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่ หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Supply Chain Management 10.0.6
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 77fdc3ae092fc8f214ae3ba68866244385e32b74
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263433"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="53f39-103">มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Dynamics 365 Supply Chain Management 10.0.6 (พฤศจิกายน 2019)</span><span class="sxs-lookup"><span data-stu-id="53f39-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53f39-104">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่ หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Microsoft Dynamics 365 Supply Chain Management 10.0.6</span><span class="sxs-lookup"><span data-stu-id="53f39-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="53f39-105">รุ่นนี้มีหมายเลขการสร้างเป็น 10.0.234</span><span class="sxs-lookup"><span data-stu-id="53f39-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="53f39-106">ในขณะที่วันที่พร้อมใช้งานทั่วไปคือในเดือนพฤศจิกายน คุณลักษณะใหม่จะพร้อมใช้งานสำหรับการนำออกใช้ล่วงหน้าในเดือนตุลาคม</span><span class="sxs-lookup"><span data-stu-id="53f39-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="53f39-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรุ่น10.0.6 ให้ดูที่ [ทรัพยากรเพิ่มเติม](whats-new-scm-10-0-6.md#additional-resources)</span><span class="sxs-lookup"><span data-stu-id="53f39-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="53f39-108">เอนทิตี้ข้อมูลของแบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์ V2</span><span class="sxs-lookup"><span data-stu-id="53f39-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="53f39-109">รุ่นที่สองสำหรับเอนทิตี้ข้อมูล "แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์" ถูกนำออกใช้แล้ว (ซึ่งเรียกว่า "แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์ V2")</span><span class="sxs-lookup"><span data-stu-id="53f39-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="53f39-110">นอกจากนี้ เท็มเพลตเริ่มต้น "418-แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์" ยังต้องเป็นเพื่อให้สามารถใช้เอนทิตี้ข้อมูล "แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์ V2" ใหม่ในเท็มเพลตกรอบงานนำเข้า/ส่งออกได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="53f39-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="53f39-111">เท็มเพลตจะไม่ได้รับการอัปเดตโดยอัตโนมัติ ดังนั้นคุณจะต้องโหลดเท็มเพลตจากค่าเริ่มต้นด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="53f39-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="53f39-112">เอนทิตี V2 ส่งออกแถวหนึ่งแถวเป็นไฟล์แยกต่างหากในเอกสารแนบ แทนที่จะเป็นอินไลน์ ซึ่งแก้ปัญหาขีดจำกัดขนาดของเอนทิตี V1</span><span class="sxs-lookup"><span data-stu-id="53f39-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="53f39-113">คุณต้องทำอะไรบ้างจึงจะสามารถทำการเปลี่ยนแปลงนี้ได้</span><span class="sxs-lookup"><span data-stu-id="53f39-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="53f39-114">เมื่อเอนทิตี้เอนทิตี V1 ถูกยกเลิกการใช้ คุณควรเริ่มต้นการย้ายจาก V1 เป็น V2</span><span class="sxs-lookup"><span data-stu-id="53f39-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="53f39-115">ถ้าคุณกำลังใช้เท็มเพลต "418-แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์" คุณสามารถคลิกปุ่ม "โหลดเท็มเพลตเริ่มต้น" และโหลดเท็มเพลต "418 – แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์" อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="53f39-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="53f39-116">ถ้าคุณต้องการรักษาความเข้ากันได้กับระบบที่มีอยู่ คุณสามารถดำเนินการต่อได้โดยใช้เท็มเพลตและเอนทิตี V1 ที่มีอยู่ จนกว่าคุณจะย้ายการรวมของคุณไปยังเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="53f39-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="53f39-117">การปรับปรุงการจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="53f39-117">Feature management enhancements</span></span>
<span data-ttu-id="53f39-118">ในขณะนี้การจัดการคุณลักษณะช่วยให้คุณสามารถเปิดใช้งานคุณลักษณะใหม่ทั้งหมดตามค่าเริ่มต้น ต้องการการยืนยันเพื่อเปิดใช้งานคุณลักษณะ และเปิดใช้งานคุณลักษณะทั้งหมดที่ยังไม่ได้เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="53f39-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="53f39-119">ฝ่ายที่รับผิดชอบข้อตกลงการซื้อ</span><span class="sxs-lookup"><span data-stu-id="53f39-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="53f39-120">ขณะนี้คุณมีความสามารถในการกำหนดฝ่ายที่รับผิดชอบหลักและรองในฟอร์มการจัดประเภทข้อตกลงการซื้อและข้อตกลงการซื้อที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="53f39-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="53f39-121">นี่จะแสดงสิทธิ์การเข้าถึงของผู้ใช้ที่เป็นผู้ดูแลข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="53f39-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="53f39-122">ลิงค์ RFQ ในรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="53f39-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="53f39-123">คุณสามารถเพิ่มลิงค์การอ้างอิงจากรายการใบสั่งซื้อกลับไปยังรายการ RFQ ที่สอดคล้องกันที่มีต้นกำเนิดมา ซึ่งช่วยให้ผู้ใช้สามารถได้รับเอกสารคำขอใบเสนอราคาที่สนับสนุนได้</span><span class="sxs-lookup"><span data-stu-id="53f39-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53f39-124">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="53f39-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="53f39-125">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="53f39-125">Bug fixes</span></span>
<span data-ttu-id="53f39-126">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแก้ไขบักที่รวมอยู่ในการอัปเดตแต่ละรายการที่เป็นส่วนหนึ่งของ 10.0.6 ให้ลงชื่อเข้าใช้ Lifecycle Services (LCS) และดู [บทความ KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7)</span><span class="sxs-lookup"><span data-stu-id="53f39-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="53f39-127">แพลตฟอร์ม update 30</span><span class="sxs-lookup"><span data-stu-id="53f39-127">Platform update 30</span></span>
<span data-ttu-id="53f39-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 รวมถึง Platform update 30</span><span class="sxs-lookup"><span data-stu-id="53f39-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="53f39-129">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับ Platform update 30 ให้ดูที่ [มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md)</span><span class="sxs-lookup"><span data-stu-id="53f39-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="53f39-130">Dynamics 365: 2019 แผนเวฟการนำออกใช้ 2</span><span class="sxs-lookup"><span data-stu-id="53f39-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="53f39-131">สงสัยเกี่ยวกับความสามารถที่กำลังจะเกิดขึ้นและที่เผยแพร่เมื่อเร็วๆ นี้ในแอปหรือแพลตฟอร์มทางธุรกิจใดๆ ของเราใช่ไหม</span><span class="sxs-lookup"><span data-stu-id="53f39-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="53f39-132">ตรวจสอบ [Dynamics 365: 2019 แผนเวฟการนำออกใช้ 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/)</span><span class="sxs-lookup"><span data-stu-id="53f39-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="53f39-133">เราได้บันทึกทุกรายละเอียดอย่างครอบคลุมตั้งแต่ต้นจนจบในเอกสารเดียวที่คุณสามารถใช้สำหรับการวางแผนได้</span><span class="sxs-lookup"><span data-stu-id="53f39-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="53f39-134">คุณลักษณะ Supply Chain Management ที่ถูกลบและที่ถูกยกเลิกการใช้</span><span class="sxs-lookup"><span data-stu-id="53f39-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="53f39-135">หัวข้อ [คุณลักษณะที่ถูกลบและที่ถูกยกเลิกการใช้ใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) จะอธิบายถึงคุณลักษณะที่ได้รับหรือถูกจัดกำหนดการให้ถูกลบหรือถูกยกเลิกการใช้สำหรับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="53f39-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="53f39-136">คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="53f39-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="53f39-137">คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต</span><span class="sxs-lookup"><span data-stu-id="53f39-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="53f39-138">ก่อนที่คุณลักษณะใดๆ จะถูกลบออกจากผลิตภัณฑ์ จะมีการประกาศการแจ้งเตือนการยกเลิกการใช้ในหัวข้อ [คุณลักษณะที่ถูกลบหรือที่ถูกเลิกใช้งานใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 เดือนก่อนการลบ</span><span class="sxs-lookup"><span data-stu-id="53f39-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="53f39-139">สำหรับการจำแนกการเปลี่ยนแปลงที่มีผลกระทบเฉพาะต่อเวลาการคอมไพล์ แต่เป็นไบนารีที่เข้ากันได้กับสภาพแวดล้อม sandbox และสภาพแวดล้อมการผลิต เวลาในการยกเลิกการใช้จะน้อยกว่า 12 เดือน</span><span class="sxs-lookup"><span data-stu-id="53f39-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="53f39-140">โดยทั่วไป รายการเหล่านี้คือการอัปเดตการทำงานที่จำเป็นต้องทำกับคอมไพเลอร์</span><span class="sxs-lookup"><span data-stu-id="53f39-140">Typically, these are functional updates that need to be made to the compiler.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]