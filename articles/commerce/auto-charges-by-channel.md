---
title: เปิดใช้งานและตั้งค่าคอนฟิกค่าธรรมเนียมอัตโนมัติตามช่องทาง
description: หัวข้อนี้จะอธิบายวิธีการเปิดใช้งานและตั้งค่าคอนฟิกค่าธรรมเนียมอัตโนมัติตามช่องทางใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 1be07c754e563298d82f6ca54f09ae3aa9118602
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175434"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="236ef-103">เปิดใช้งานและตั้งค่าคอนฟิกค่าธรรมเนียมอัตโนมัติตามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="236ef-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="236ef-104">หัวข้อนี้จะอธิบายวิธีการเปิดใช้งานและตั้งค่าคอนฟิกค่าธรรมเนียมที่คิดโดยอัตโนมัติ (ธรรมเนียมอัตโนมัติ) ตามช่องทางใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="236ef-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="236ef-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="236ef-105">Overview</span></span>

<span data-ttu-id="236ef-106">คุณอาจมีสถานการณ์จำลองที่ค่าธรรมเนียมการรีไซเคิลหรือค่าธรรมเนียมอื่นๆ ต้องใช้กับกลุ่มของผลิตภัณฑ์ที่ขายในร้านค้าทั้งหมดหรือบางร้านในรัฐเฉพาะ (ตัวอย่างเช่น แคลิฟอร์เนีย)</span><span class="sxs-lookup"><span data-stu-id="236ef-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="236ef-107">คุณลักษณะการทำงาน **เปิดใช้งานตัวกรองค่าธรรมเนียมอัตโนมัติตามช่องทาง** ใน Commerce ช่วยให้คุณสามารถระบุค่าธรรมเนียมอัตโนมัติตามช่องทาง (ตัวอย่างเช่น ช่องทางจริงเฉพาะ)</span><span class="sxs-lookup"><span data-stu-id="236ef-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="236ef-108">คุณลักษณะนี้พร้อมใช้งานใน Dynamics 365 Commerce รุ่น 10.0.10 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="236ef-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="236ef-109">เมื่อต้องการเปิดใช้งานและตั้งค่าคอนฟิกค่าธรรมเนียมอัตโนมัติตามช่องทาง คุณต้องทำงานต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="236ef-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="236ef-110">เปิดใช้งานคุณลักษณะ **เปิดใช้งานตัวกรองค่าธรรมเนียมโดยอัตโนมัติตามช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="236ef-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="236ef-111">ตั้งค่าคอนฟิกวัตถุประสงค์สำหรับลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="236ef-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="236ef-112">กำหนดค่าธรรมเนียมอัตโนมัติตามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="236ef-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="236ef-113">คุณลักษณะ **เปิดใช้งานตัวกรองค่าธรรมเนียมอัตโนมัติตามช่องทาง** ทำงานเมื่อมีการเปิดใช้งานคุณลักษณะค่าธรรมเนียมอัตโนมัติขั้นสูงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="236ef-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="236ef-114">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเปิดใช้งานคุณลักษณะค่าธรรมเนียมอัตโนมัติขั้นสูง ดูที่ [ค่าธรรมเนียมอัตโนมัติขั้นสูงช่องทาง Omni](omni-auto-charges.md)</span><span class="sxs-lookup"><span data-stu-id="236ef-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="236ef-115">เปิดใช้งานคุณลักษณะตัวกรองค่าธรรมเนียมโดยอัตโนมัติตามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="236ef-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="236ef-116">เมื่อต้องการเปิดใช้งานค่าธรรมเนียมอัตโนมัติตามช่องทางใน Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="236ef-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="236ef-117">ไปที่ **ผู้ดูแลระบบ \> พื้นที่ทำงาน \> การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="236ef-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="236ef-118">บนแท็บ **ไม่ได้เปิดใช้งาน** ในรายการ **ชื่อคุณลักษณะ** ให้ค้นหาและเลือก **เปิดใช้งานตัวกรองค่าธรรมเนียมอัตโนมัติตามช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="236ef-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="236ef-119">ที่มุมขวาล่าง ให้เลือก **เปิดใช้งานทันที**</span><span class="sxs-lookup"><span data-stu-id="236ef-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="236ef-120">หลังจากที่เปิดใช้งานคุณลักษณะแล้ว จะปรากฏในรายการบนแท็บ **ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="236ef-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="236ef-121">ไปยัง **การขายปลีกและการค้า \> การขายปลีกและไอทีเชิงพาณิชย์ \> กำหนดการการจัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="236ef-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="236ef-122">ในบานหน้าต่างด้านซ้าย ให้ค้นหาและเลือกงาน **1110** (**การตั้งค่าคอนฟิกส่วนกลาง**)</span><span class="sxs-lookup"><span data-stu-id="236ef-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="236ef-123">ในบานหน้าต่างการดำเนินการ ให้เลือก **เรียกใช้เดี๋ยวนี้** เพื่อเผยแพร่การเปลี่ยนแปลงการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="236ef-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="236ef-124">ถ้าคุณปิดใช้งาน **การเปิดใช้งานตัวกรองค่าธรรมเนียมอัตโนมัติตามช่องทาง** หลังจากที่คุณใช้งานแล้ว ฟิลด์ **ความสัมพันธ์ช่องทางการขายปลีก** ภายใต้ **ค่าธรรมเนียมอัตโนมัติ** จะไม่ปรากฏอีกต่อไป และคุณจะสูญเสียการตั้งค่าคอนฟิกที่มีอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="236ef-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="236ef-125">ถ้ามีการลบการตั้งค่าคอนฟิก **ความสัมพันธ์ช่องทางการขายปลีก** จะทำให้กฎค่าธรรมเนียมอัตโนมัติถูกทำซ้ำ ความพยายามในการปิดใช้งานคุณลักษณะจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="236ef-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="236ef-126">ก่อนที่คุณจะปิดคุณลักษณะ โปรดตรวจสอบให้แน่ใจว่าได้ตรวจสอบกฎค่าธรรมเนียมอัตโนมัติทั้งหมดและทำการเปลี่ยนแปลงใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="236ef-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="236ef-127">ตั้งค่าคอนฟิกวัตถุประสงค์สำหรับลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="236ef-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="236ef-128">วัตถุประสงค์ของลำดับชั้นขององค์กรใหม่ที่มีชื่อว่า **ค่าธรรมเนียมอัตโนมัติของการขายปลีก** มีการสร้างเพื่อจัดการลำดับชั้นสำหรับค่าธรรมเนียมอัตโนมัติตามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="236ef-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="236ef-129">เมื่อต้องการกำหนดลำดับชั้นเริ่มต้นให้กับวัตถุประสงค์ลำดับชั้นขององค์กรใน Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="236ef-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="236ef-130">ไปที่ **การจัดการองค์กร \> องค์กร \> วัตถุประสงค์สำหรับลำดับชั้นขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="236ef-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="236ef-131">ในบานหน้าต่างด้านซ้าย ให้เลือก **ค่าธรรมเนียมอัตโนมัติของการขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="236ef-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="236ef-132">ภายใต้ **ลำดับชั้นที่กำหนด** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="236ef-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="236ef-133">ในกล่องโต้ตอบ **ลำดับชั้นขององค์กร** ให้เลือกลำดับชั้นขององค์กร (ตัวอย่างเช่น **ร้านค้าปลีกตามภูมิภาค**) แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="236ef-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="236ef-134">ภายใต้ **ลำดับชั้นที่กำหนด** ให้เลือก **ตั้งเป็นค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="236ef-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="236ef-135">ไปยัง **การขายปลีกและการค้า \> การขายปลีกและไอทีเชิงพาณิชย์ \> กำหนดการการจัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="236ef-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="236ef-136">ในบานหน้าต่างด้านซ้าย ให้ค้นหาและเลือกงาน **1040** (**ผลิตภัณฑ์**)</span><span class="sxs-lookup"><span data-stu-id="236ef-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="236ef-137">บนบานหน้าต่างการดำเนินการ เลือก **รันเดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="236ef-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="236ef-138">ทำซ้ำสองขั้นตอนก่อนหน้านี้เพื่อรันงาน **1070** (**การตั้งค่าคอนฟิกช่องทาง**) และ **1110** (**การตั้งค่าคอนฟิกส่วนกลาง**)</span><span class="sxs-lookup"><span data-stu-id="236ef-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![การตั้งค่าคอนฟิกของวัตถุประสงค์ลำดับชั้นขององค์กรสำหรับค่าธรรมเนียมอัตโนมัติของการขายปลีก](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="236ef-140">กำหนดค่าธรรมเนียมอัตโนมัติตามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="236ef-140">Define auto charges by channel</span></span>

<span data-ttu-id="236ef-141">หลังจากที่คุณเปิดใช้คุณลักษณะ **การเปิดใช้งานค่าธรรมเนียมอัตโนมัติตามช่องทาง** และตั้งค่าคอนฟิกวัตถุประสงค์ลำดับชั้นขององค์กรที่มี **ค่าธรรมเนียมอัตโนมัติของการขายปลีก** จะมีการกำหนดค่าธรรมเนียมอัตโนมัติตามช่องทางในระดับส่วนหน้าของใบสั่งหรือระดับรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="236ef-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="236ef-142">เมื่อต้องการกำหนดค่าธรรมเนียมอัตโนมัติตามช่องทางใน Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="236ef-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="236ef-143">ไปยัง **บัญชีลูกหนี้ \> การตั้งค่าค่าธรรมเนียม \> ค่าธรรมเนียมอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="236ef-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="236ef-144">ในบานหน้าต่างด้านซ้าย ในฟิลด์ **ระดับ** ให้เลือก **ส่วนหัว** หรือ **รายการ** ทั้งนี้ขึ้นอยู่กับความต้องการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="236ef-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="236ef-145">ในฟิลด์ **รหัสช่องทางการขายปลีก** ให้เลือกรหัสช่องทางที่เหมาะสม (ตัวอย่างเช่น **ตาราง** หรือ **กลุ่ม**)</span><span class="sxs-lookup"><span data-stu-id="236ef-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="236ef-146">ถ้ามีการใช้การตั้งค่าเริ่มต้น **ทั้งหมด** จะมีการใช้กฎค่าธรรมเนียมกับช่องทางทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="236ef-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="236ef-147">ถ้าคุณเลือก **กลุ่ม** โปรดตรวจสอบให้แน่ใจว่ามีการสร้างกลุ่มค่าธรรมเนียมของช่องทางการขายปลีกที่ **Retail และ Commerce \> ตั้งค่าช่องทาง \> ค่าธรรมเนียม \> กลุ่มค่าธรรมเนียมช่องทางการขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="236ef-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="236ef-148">ถ้าคุณเลือก **ตาราง** คุณสามารถเลือกช่องทางเฉพาะ (ตัวอย่างเช่น **ซานฟรานซิสโก**) ในฟิลด์ **ความสัมพันธ์ช่องทางการขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="236ef-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="236ef-149">ไปยัง **การขายปลีกและการค้า \> การขายปลีกและไอทีเชิงพาณิชย์ \> กำหนดการการจัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="236ef-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="236ef-150">ในบานหน้าต่างด้านซ้าย ให้ค้นหาและเลือกงาน **1040** (**ผลิตภัณฑ์**)</span><span class="sxs-lookup"><span data-stu-id="236ef-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="236ef-151">บนบานหน้าต่างการดำเนินการ เลือก **รันเดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="236ef-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="236ef-152">ทำซ้ำสองขั้นตอนก่อนหน้านี้เพื่อรันงาน **1070** (**การตั้งค่าคอนฟิกช่องทาง**) และ **1110** (**การตั้งค่าคอนฟิกส่วนกลาง**)</span><span class="sxs-lookup"><span data-stu-id="236ef-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![ค่าธรรมเนียมอัตโนมัติที่กำหนดตามช่องทาง](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="236ef-154">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="236ef-154">Example scenario</span></span>

<span data-ttu-id="236ef-155">ตัวอย่างต่อไปนี้แสดงขั้นตอนที่จำเป็นในการตั้งค่าคอนฟิกผลิตภัณฑ์เพื่อให้มีการเรียกเก็บค่าธรรมเนียมการรีไซเคิลเมื่อมีการขายผลิตภัณฑ์ผ่านช่องทางจริงของซานฟรานซิสโก</span><span class="sxs-lookup"><span data-stu-id="236ef-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="236ef-156">ตัวอย่างเช่นนี้แสดงให้เห็นเมื่อมีค่าธรรมเนียมอัตโนมัติปรากฏขึ้นในแอปพลิเคชันการขายหน้าร้าน (POS) ของ Commerce</span><span class="sxs-lookup"><span data-stu-id="236ef-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="236ef-157">องค์กรกำหนดรหัสค่าธรรมเนียมที่มีชื่อว่า **รีไซเคิล** ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="236ef-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![รหัสค่าธรรมเนียมรไซเคิล](media/Auto-charges-charge-code.png)

<span data-ttu-id="236ef-159">มีการสร้างค่าธรรมเนียมอัตโนมัติที่ระดับรายการ</span><span class="sxs-lookup"><span data-stu-id="236ef-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="236ef-160">มีการตั้งค่าคอนฟิกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="236ef-160">It has the following configuration:</span></span>

- <span data-ttu-id="236ef-161">ฟิลด์ **รหัสบัญชี** ถูกตั้งค่าเป็น **ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="236ef-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="236ef-162">ฟิลด์ **รหัสรายการ** ถูกตั้งค่าเป็น **ตาราง**</span><span class="sxs-lookup"><span data-stu-id="236ef-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="236ef-163">ฟิลด์ **ความสัมพันธ์ของสินค้า** ถูกตั้งค่าเป็นรหัสผลิตภัณฑ์ **91001**</span><span class="sxs-lookup"><span data-stu-id="236ef-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="236ef-164">ฟิลด์ **รหัสของโหมดในการจัดส่ง** ถูกตั้งค่าเป็น **ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="236ef-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="236ef-165">ฟิลด์ **รหัสรช่องทางการขายปลีก** ถูกตั้งค่าเป็น **ตาราง**</span><span class="sxs-lookup"><span data-stu-id="236ef-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="236ef-166">ฟิลด์ **ความสัมพันธ์ของช่องทางการขายปลีก** ถูกตั้งค่าเป็นร้านค้า **ซานฟรานซิสโก**</span><span class="sxs-lookup"><span data-stu-id="236ef-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="236ef-167">มีการสร้างรายการค่าธรรมเนียมอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="236ef-167">An auto charges line is created.</span></span> <span data-ttu-id="236ef-168">มีการตั้งค่าคอนฟิกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="236ef-168">It has the following configuration:</span></span>

- <span data-ttu-id="236ef-169">ฟิลด์ **สกุลเงิน** ถูกการตั้งค่าเป็น **USD**</span><span class="sxs-lookup"><span data-stu-id="236ef-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="236ef-170">ฟิลด์ **รหัสค่าธรรมเนียม** ถูกตั้งค่าเป็น **รีไซเคิล**</span><span class="sxs-lookup"><span data-stu-id="236ef-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="236ef-171">ฟิลด์ **ประเภท** ถูกตั้งค่าเป็น **แก้ไขแล้ว**</span><span class="sxs-lookup"><span data-stu-id="236ef-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="236ef-172">ฟิลด์ **ค่าธรรมเนียม** จะถูกตั้งค่าเป็น **$6.25**</span><span class="sxs-lookup"><span data-stu-id="236ef-172">The **Charges** field is set to **$6.25**.</span></span>

![การตั้งค่าคอนฟิกค่าธรรมเนียมอัตโนมัติของระดับรายการและรายการค่าธรรมเนียมอัตโนมัติ](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="236ef-174">ในแอปพลิเคชัน POS ใบสั่งขายจะถูกสร้างขึ้นในช่องทางร้านค้า **ซานฟรานซิสโก**</span><span class="sxs-lookup"><span data-stu-id="236ef-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="236ef-175">รายการ **ค่าธรรมเนียม** แสดงค่าธรรมเนียมการรีไซเคิล **$6.25**</span><span class="sxs-lookup"><span data-stu-id="236ef-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="236ef-176">โดยการเลือก **ตัวเลือกธุรกรรม \> ค่าธรรมเนียม \> จัดการกับค่าธรรมเนียม** ในแอปพลิเคชัน POS คุณสามารถดูรหัสค่าธรรมเนียมและคำอธิบายสำหรับค่าธรรมเนียมการรีไซเคิลได้</span><span class="sxs-lookup"><span data-stu-id="236ef-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![ค่าธรรมเนียมการรีไซเคิลในแอปพลิเคชัน POS](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="236ef-178">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="236ef-178">Additional resources</span></span>

[<span data-ttu-id="236ef-179">ค่าธรรมเนียมอัตโนมัติขั้นสูงของช่องทาง Omni</span><span class="sxs-lookup"><span data-stu-id="236ef-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="236ef-180">แบ่งค่าธรรมเนียมส่วนหัวตามส่วนไปยังรายการขายที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="236ef-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)
