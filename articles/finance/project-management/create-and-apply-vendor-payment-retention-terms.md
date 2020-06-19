---
title: สร้างและใช้เงื่อนไขเงินวางประกันสำหรับการชำระเงินให้แก่ผู้จัดจำหน่าย
description: หัวข้อนี้จะนำเสนอข้อมูลเกี่ยวกับวิธีการตั้งค่า และดูแลรักษาเงื่อนไขเงินวางประกันสำหรับการชำระเงินให้แก่ผู้จัดจำหน่าย
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410273"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="b034d-103">สร้างและใช้เงื่อนไขเงินวางประกันสำหรับการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b034d-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="b034d-104">การตั้งค่าเงื่อนไขเงินวางประกันสำหรับการชำระเงินให้แก่ผู้จัดจำหน่ายสำหรับโครงการจะมีประโยชน์ เมื่อองค์กรของคุณต้องการประกันส่วนหนึ่งของเงินที่ชำระให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b034d-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="b034d-105">ตัวอย่างเช่น เมื่อคุณต้องการระงับการชำระเงินให้แก่ผู้จัดจำหน่าย จนกว่าผลิตภัณฑ์ที่จัดส่งมาจะตรงตามความคาดหวังของคุณ</span><span class="sxs-lookup"><span data-stu-id="b034d-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="b034d-106">สามารถระบุเงื่อนไขเงินวางประกันสำหรับการชำระเงินให้แก่ผู้จัดจำหน่าย เมื่อคุณเจรจากับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b034d-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="b034d-107">สร้างเงื่อนไขเงินประกันผลงานสำหรับการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b034d-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="b034d-108">คุณสามารถป้อนเปอร์เซ็นต์การชำระเงินให้แก่ผู้จัดจำหน่ายที่จะเก็บไว้ และเปอร์เซ็นต์ของยอดเงินที่เก็บไว้ก่อนหน้านี้ที่จะนำออก</span><span class="sxs-lookup"><span data-stu-id="b034d-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="b034d-109">ทั้งนี้ยอดเงินจะสะสมบนใบแจ้งหนี้ของผู้จัดจำหน่ายโดยอัตโนมัติ จนกว่าสัญญาไปถึงสถานะของความสมบูรณ์ที่ระบุ </span><span class="sxs-lookup"><span data-stu-id="b034d-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="b034d-110">หลังจากที่คุณตั้งค่าเงื่อนไขเงินวางประกันแล้ว คุณสามารถนำเงื่อนไขนี้ไปใช้กับโครงการใดสำหรับผู้จัดจำหน่ายนั้นก็ได้</span><span class="sxs-lookup"><span data-stu-id="b034d-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="b034d-111">ใช้ขั้นตอนต่อไปนี้เพื่อตั้งค่าและดูแลรักษาเงื่อนไขเงินวางประกันสำหรับการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b034d-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="b034d-112">ไปที่ **การจัดการและการบัญชีโครงการ** > **การวางเงินประกัน** > **เงื่อนไขเงินวางประกันสำหรับการชำระเงินให้แก่ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="b034d-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="b034d-113">เลือก **สร้าง** เมื่อต้องการเพิ่มเงื่อนไขเงินวางประกันของผู้จัดจำหน่ายใหม่</span><span class="sxs-lookup"><span data-stu-id="b034d-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="b034d-114">ค่า **รหัสกฎ** สำหรับเงื่อนไขใหม่จะถูกป้อนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b034d-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="b034d-115">ป้อนคำอธิบายโดยย่อในฟิลด์ **คำอธิบาย** และบนแท็บด่วน **เงื่อนไข** ให้เลือก **เพิ่มบรรทัด** เพื่อป้อนค่าของเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b034d-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="b034d-116">**เปอร์เซ็นต์ของหน่วยที่จัดส่ง** ป้อนเปอร์เซ็นต์ความสมบูรณ์ของเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="b034d-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="b034d-117">ยอดเงินจะถูกเก็บไว้บนใบแจ้งหนี้ของผู้จัดจำหน่ายโดยอัตโนมัติ จนกว่าขั้นความสมบูรณ์ของโครงการจะเท่ากับเปอร์เซ็นต์ที่คุณระบุ</span><span class="sxs-lookup"><span data-stu-id="b034d-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="b034d-118">ตัวอย่างเช่น ถ้าคุณป้อน 50.00 ยอดเงินจะเก็บไว้จนกว่าโครงการจะเสร็จสมบูรณ์ 50 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="b034d-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="b034d-119">**เปอร์เซ็นต์ที่จะเก็บไว้** ป้อนเปอร์เซ็นต์ยอดเงินใบแจ้งหนี้ของผู้จัดจำหน่ายที่จะเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="b034d-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="b034d-120">ตัวอย่างเช่น ถ้าคุณได้ป้อน 10.00 ดังนั้น 10 เปอร์เซ็นต์ของยอดเงินในใบแจ้งหนี้ของผู้จัดจำหน่ายจะถูกเก็บไว้จนกว่าโครงการจะถึงเปอร์เซ็นต์ของความสมบูรณ์ที่ตั้งค่าใน **ฟิลด์เปอร์เซ็นต์ของหน่วยที่จัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="b034d-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="b034d-121">ในฟิลด์ **เปอร์เซ็นต์ที่จะนำออกใช้** เลือก **เพิ่มบรรทัด** เพื่อป้อนเปอร์เซ็นต์ของยอดเงินที่เก็บไว้ก่อนหน้านี้ ที่จะนำออกใช้ในระดับความสมบูรณ์ของโครงการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b034d-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="b034d-122">ถ้าคุณมีเหตุการณ์สำคัญสำหรับระดับความสมบูรณ์ของโครงการต่าง ๆ มากกว่าหนึ่งเหตุการณ์ ให้ป้อนรายการเงื่อนไขเงินวางประกันของผู้จัดจำหน่ายแยกต่างหากสำหรับแต่ละกฎเงินวางประกัน</span><span class="sxs-lookup"><span data-stu-id="b034d-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="b034d-123">โดยแต่ละรายการสามารถระบุเปอร์เซ็นต์ที่เก็บไว้แตกต่างกัน และเปอร์เซ็นต์ที่นำออกใช้ที่แตกต่างกันสำหรับความสมบูรณ์ของโครงการที่กำหนดแต่ละระดับ</span><span class="sxs-lookup"><span data-stu-id="b034d-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="b034d-124">หลังจากที่คุณเงื่อนไขเงินวางประกันสำหรับการชำระเงินให้แก่ผู้จัดจำหน่ายแลเว คุณสามารถนำเงื่อนไขนี้ไปใช้กับโครงการได้</span><span class="sxs-lookup"><span data-stu-id="b034d-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="b034d-125">นำเงื่อนไขเงินวางประกันสำหรับการชำระเงินให้แก่ผู้จัดจำหน่ายไปใช้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="b034d-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="b034d-126">ไปที่ **การจัดการและการบัญชีโครงการ** > **โครงการ** > **โครงการทั้งหมด** และเปิดโครงการจากหน้ารายการโครงการ</span><span class="sxs-lookup"><span data-stu-id="b034d-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="b034d-127">ใน FastTab **ข้อตกลงของผู้จัดจำหน่าย** ให้เลือก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="b034d-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="b034d-128">ในฟิลด์ **รหัสบัญชี** ให้เลือกตัวเลือกใดตัวเลือกหนึ่งดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b034d-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="b034d-129">**ตาราง**: – เงื่อนไขเงินวางประกันของผู้จัดจำหน่ายใช้กับผู้จัดจำหน่ายเดียว</span><span class="sxs-lookup"><span data-stu-id="b034d-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="b034d-130">**กลุ่ม**: – เงื่อนไขเงินวางประกันของผู้จัดจำหน่ายใช้กับผู้จัดจำหน่ายทั้งหมดในกลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b034d-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="b034d-131">**ทั้งหมด**: – เงื่อนไขเงินวางประกันของผู้จัดจำหน่ายใช้กับผู้จัดจำหน่ายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b034d-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="b034d-132">ในฟิลด์ **ผู้จัดจำหน่าย/กลุ่มผู้จัดจำหน่าย** ให้เลือกผู้จัดจำหน่ายหรือกลุ่มผู้จัดจำหน่ายที่ต้องใช้เงื่อนไขเงินวางประกันของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b034d-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="b034d-133">ถ้าคุณเลือก **ทั้งหมด** ในขั้นตอนก่อนหน้านี้ ฟิลด์นี้จะไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b034d-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="b034d-134">ในฟิลด์ **เงื่อนไขเงินวางประกัน** ให้เลือกเงื่อนไขเงินวางประกันที่คุณสร้างไว้ในกระบวนงานก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="b034d-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="b034d-135">ถ้าโครงการมีการตั้งค่าเงื่อนไขจ่ายเมื่อได้รับชำระเงิน (PWP) สำหรับผู้จัดจำหน่ายด้วย ให้ป้อนเปอร์เซ็นต์ขีดจำกัดสำหรับโครงการในฟิลด์ **เปอร์เซ็นต์ขีดจำกัด PWP**</span><span class="sxs-lookup"><span data-stu-id="b034d-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="b034d-136">นอกจากนี้เงื่อนไขเงินวางประกันของผู้จัดจำหน่ายจะแสดงบนใบสั่งซื้อที่คุณสร้างสำหรับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b034d-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
