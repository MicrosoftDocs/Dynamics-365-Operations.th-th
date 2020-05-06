---
title: เริ่มต้นใช้งานบริการการบัญชีต้นทุน
description: หัวข้อนี้แสดงรายละเอียดของใบอนุญาตและคำแนะนำการติดตั้งสำหรับบริการการบัญชีต้นทุน
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276968"
---
# <a name="get-started-with-the-cost-accounting-service"></a><span data-ttu-id="2c23e-103">เริ่มต้นใช้งานบริการการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2c23e-103">Get started with the cost accounting service</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="2c23e-104">ฟังก์ชันการทำงานที่อธิบายในหัวข้อนี้พร้อมใช้งานเป็นส่วนหนึ่งของการเผยแพร่รุ่นพรีวิวแบบส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="2c23e-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="2c23e-105">เนื้อหาของหัวข้อนี้และฟังก์ชันที่อธิบายอาจมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="2c23e-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="2c23e-106">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการนำออกใช้การแสดงตัวอย่าง ให้ดูที่ [FAQ เกี่ยวกับการอัปเดตบริการแบบหนึ่งเวอร์ชัน](../../fin-ops-core/fin-ops/get-started/one-version.md)</span><span class="sxs-lookup"><span data-stu-id="2c23e-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="2c23e-107">บริการการบัญชีต้นทุนช่วยให้คุณสามารถทำการบัญชีสินค้าคงคลังหลายรายการในบัญชีแยกประเภทการบัญชีต้นทุนสินค้าที่คุณตั้งค่าไว้</span><span class="sxs-lookup"><span data-stu-id="2c23e-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="2c23e-108">คุณเชื่อมโยงบัญชีแยกประเภทการบัญชีต้นทุนแต่ละบัญชีกับ *แบบแผน*</span><span class="sxs-lookup"><span data-stu-id="2c23e-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="2c23e-109">แบบแผนเป็นชุดของนโยบายการบัญชีชนิดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c23e-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="2c23e-110">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2c23e-110">Cost object</span></span>
- <span data-ttu-id="2c23e-111">ป้อนข้อมูลเกณฑ์การวัด</span><span class="sxs-lookup"><span data-stu-id="2c23e-111">Input measurement basis</span></span>
- <span data-ttu-id="2c23e-112">สมมติฐานกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2c23e-112">Cost flow assumption</span></span>
- <span data-ttu-id="2c23e-113">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2c23e-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="2c23e-114">แม้แต่หลังจากที่คุณได้เปิดใช้งานบริการการบัญชีต้นทุนแล้ว คุณยังสามารถทำการบัญชีสินค้าคงคลังใน Microsoft Dynamics 365 Supply Chain Management ได้ตามปกติ</span><span class="sxs-lookup"><span data-stu-id="2c23e-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="2c23e-115">บริการการบัญชีต้นทุนเป็น add-in</span><span class="sxs-lookup"><span data-stu-id="2c23e-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="2c23e-116">เมื่อต้องการทำให้คุณลักษณะพร้อมใช้งาน คุณต้องติดตั้งจาก Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="2c23e-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="2c23e-117">ดังนั้น คุณจึงสามารถเลือกที่จะประเมินในสภาพแวดล้อมการทดสอบ ก่อนที่คุณจะเปิดใช้งานสำหรับสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="2c23e-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="2c23e-118">ขณะนี้บริการการบัญชีต้นทุนไม่สนับสนุนคุณลักษณะการจัดการต้นทุนทั้งหมดที่ถูกสร้างลงใน Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2c23e-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="2c23e-119">ดังนั้น จึงเป็นเรื่องสำคัญอย่างยิ่งที่คุณจะต้องประเมินว่าชุดของคุณลักษณะที่พร้อมใช้งานในขณะนี้จะตรงกับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="2c23e-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="licensing"></a><span data-ttu-id="2c23e-120">การให้ลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="2c23e-120">Licensing</span></span>

<span data-ttu-id="2c23e-121">บริการการบัญชีต้นทุนจะได้รับอนุญาตพร้อมกับคุณลักษณะมาตรฐานของการบัญชีสินค้าคงคลังที่พร้อมใช้งานสำหรับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2c23e-121">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="2c23e-122">คุณไม่จำเป็นต้องซื้อสิทธิ์การใช้งานเพิ่มเติมเพื่อใช้บริการการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2c23e-122">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><span data-ttu-id="2c23e-123">ติดตั้ง Add-in</span><span class="sxs-lookup"><span data-stu-id="2c23e-123">Install the add-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c23e-124">เมื่อต้องการใช้บริการการบัญชีต้นทุน คุณต้องมีสภาพแวดล้อมที่มีความพร้อมใช้งานสูงซึ่ง LCS เปิดใช้งาน (ไม่ใช่สภาพแวดล้อม OneBox) และคุณต้องรัน Dynamics 365 Supply Chain Management รุ่น 10.0.11 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="2c23e-124">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="2c23e-125">เมื่อต้องการใช้บริการการบัญชีต้นทุน ให้ติดตั้ง add-in ของบริการการบัญชีต้นทุนสำหรับ Supply Chain Management ตามที่อธิบายไว้ในกระบวนงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2c23e-125">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="2c23e-126">ลงชื่อเข้าใช้ LCS</span><span class="sxs-lookup"><span data-stu-id="2c23e-126">Sign in to LCS.</span></span>

1. <span data-ttu-id="2c23e-127">ไปที่ **การจัดการคุณลักษณะการแสดงตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="2c23e-127">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="2c23e-128">เลือกเครื่องหมายบวก (**+**)</span><span class="sxs-lookup"><span data-stu-id="2c23e-128">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="2c23e-129">ในฟิลด์ **รหัส** ให้ป้อนคีย์เบต้า add-in ของคุณสำหรับบริการการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2c23e-129">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="2c23e-130">(คุณควรได้รับคีย์ของคุณทางอีเมล)</span><span class="sxs-lookup"><span data-stu-id="2c23e-130">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="2c23e-131">เลือก **ยกเลิกการบล็อก**</span><span class="sxs-lookup"><span data-stu-id="2c23e-131">Select **Unblock**.</span></span>

1. <span data-ttu-id="2c23e-132">เปิดสภาพแวดล้อม LCS ที่คุณต้องการเพิ่มบริการ</span><span class="sxs-lookup"><span data-stu-id="2c23e-132">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="2c23e-133">ไปที่ **รายละเอียดแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="2c23e-133">Go to **Full details**.</span></span>

1. <span data-ttu-id="2c23e-134">เลื่อนลงไปที่แท็บด่วน **Add-in ของสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="2c23e-134">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="2c23e-135">เลือก **การติดตั้ง Add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="2c23e-135">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="2c23e-136">เลือก **บริการการบัญชีต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="2c23e-136">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="2c23e-137">ปฏิบัติตามคำแนะนำการติดตั้ง และยอมรับข้อกำหนดและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="2c23e-137">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="2c23e-138">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="2c23e-138">Select **Install**.</span></span>

1. <span data-ttu-id="2c23e-139">บน FastTab **Add-in ของสภาพแวดล้อม** คุณควรเห็นว่ามีการติดตั้งบริการการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2c23e-139">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="2c23e-140">หลังจากสองสามนาที สถานะควรเปลี่ยนจาก **กำลังติดตั้ง** เป็น **ติดตั้งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="2c23e-140">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="2c23e-141">(คุณอาจต้องรีเฟรชหน้าเพื่อดูการเปลี่ยนแปลงนี้) ณ จุดนั้น บริการการบัญชีต้นทุนจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2c23e-141">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="2c23e-142">ตั้งค่าการรวม</span><span class="sxs-lookup"><span data-stu-id="2c23e-142">Set up the integration</span></span>

<span data-ttu-id="2c23e-143">เมื่อต้องการตั้งค่าการรวมระหว่างบริการการบัญชีต้นทุนและ Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="2c23e-143">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="2c23e-144">ไปที่ **การจัดการระบบ > การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="2c23e-144">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="2c23e-145">เลือก **ตรวจหาการอัพเดต**</span><span class="sxs-lookup"><span data-stu-id="2c23e-145">Select **Check for updates**.</span></span>

1. <span data-ttu-id="2c23e-146">เปิดแท็บ **ทั้งหมด** และค้นหาคุณลักษณะที่มีชื่อว่า *บริการการบัญชีต้นทุน*</span><span class="sxs-lookup"><span data-stu-id="2c23e-146">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="2c23e-147">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="2c23e-147">Select **Enable now**.</span></span>

1. <span data-ttu-id="2c23e-148">ไปที่ **การจัดการต้นทุน > บริการการบัญชีต้นทุน > การตั้งค่า > พารามิเตอร์บริการการบัญชีต้นทุน > พารามิเตอร์การรวม**</span><span class="sxs-lookup"><span data-stu-id="2c23e-148">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="2c23e-149">ในฟิลด์ **รหัสแอพลิเคชัน** ให้ป้อนรหัสต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c23e-149">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="2c23e-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="2c23e-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="2c23e-151">ในฟิลด์ **ปลายทางของบริการข้อมูล** ให้ป้อน URL ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c23e-151">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="2c23e-152">ในฟิลด์ **ปลายทางของบริการการบัญชีต้นทุน** ให้ป้อน URL ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c23e-152">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="2c23e-153">ขณะนี้บริการการบัญชีต้นทุนพร้อมใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="2c23e-153">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="2c23e-154">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="2c23e-154">Related resources</span></span>

[<span data-ttu-id="2c23e-155">โฮมเพจบริการการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2c23e-155">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
