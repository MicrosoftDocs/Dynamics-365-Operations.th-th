---
title: ตั้งค่าความปลอดภัยสำหรับเนื้อหา Power BI ของการวิเคราะห์การบัญชีต้นทุน
description: หัวข้อนี้อธิบายวิธีการที่คุณสามารถเผยแพร่ความปลอดภัยระดับการเข้าถึงในการบัญชีต้นทุนไปยังความปลอดภัยระดับแถวใน Microsoft Power BI ฟังก์ชันนี้ช่วยรับประกันว่าผู้ใช้เห็นเฉพาะข้อมูล Power BI ที่พวกเขาได้รับอนุญาตให้เข้าถึง
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b0f7dffd85dc1c7a58a3e1f55eaa26ecbf6e8360
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185186"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="50bd3-104">ตั้งค่าความปลอดภัยสำหรับเนื้อหา Power BI ของการวิเคราะห์การบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="50bd3-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50bd3-105">หัวข้อนี้อธิบายวิธีการที่คุณสามารถเผยแพร่ความปลอดภัยระดับการเข้าถึงในการบัญชีต้นทุนไปยังความปลอดภัยระดับแถวใน Microsoft Power BI</span><span class="sxs-lookup"><span data-stu-id="50bd3-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="50bd3-106">ฟังก์ชันนี้ช่วยรับประกันว่าผู้ใช้เห็นเฉพาะข้อมูล Power BI ที่พวกเขาได้รับอนุญาตให้เข้าถึง</span><span class="sxs-lookup"><span data-stu-id="50bd3-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="50bd3-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="50bd3-107">Overview</span></span>

<span data-ttu-id="50bd3-108">เนื้อหา Microsoft Power BI ของ **การวิเคราะห์การบัญชีต้นทุน** ใช้ความปลอดภัยระดับแถวของ Power BI เพื่อจำกัดการเข้าถึงของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="50bd3-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="50bd3-109">ความปลอดภัยขึ้นอยู่กับลำดับชั้นขององค์กรระดับการเข้าถึงที่ถูกตั้งค่าในพารามิเตอร์การบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="50bd3-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="50bd3-110">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน** ดู [เนื้อหา Power BI ของการวิเคราะห์การบัญชีต้นทุน](cost-accounting-analysis-content-pack.md)</span><span class="sxs-lookup"><span data-stu-id="50bd3-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="50bd3-111">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="50bd3-111">Setup</span></span>
<span data-ttu-id="50bd3-112">เพื่อเผยแพร่ความปลอดภัยระดับการเข้าถึงไปยัง Power BI เจ้าของเนื้อหา Power BI ต้องทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="50bd3-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="50bd3-113">ผู้ใช้ที่เผยแพร่เนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน** กลายเป็นเจ้าของโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="50bd3-113">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="50bd3-114">เฉพาะเจ้าของสามารถตั้งค่าความปลอดภัยใน Power BI</span><span class="sxs-lookup"><span data-stu-id="50bd3-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="50bd3-115">นอกจากนี้ จนกว่าเจ้าของจะเพิ่มผู้ใช้อื่นใน PowerBI.com ไม่มีใครนอกจากเจ้าของที่สามารถมองเห็นข้อมูลใดๆ ในเนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="50bd3-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="50bd3-116">เผยแพร่ไฟล์ข้อกำหนดไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="50bd3-116">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="50bd3-117">ลงชื่อเข้าใช้ไปยัง PowerBI.com</span><span class="sxs-lookup"><span data-stu-id="50bd3-117">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="50bd3-118">ค้นหาชุดข้อมูลสำหรับเนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="50bd3-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="50bd3-119">เปิดหน้าความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="50bd3-119">Open the security page.</span></span>

    ![กำลังเปิดหน้าความปลอดภัย](./media/CA-picture-1.png)

5. <span data-ttu-id="50bd3-121">บทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** ถูกสร้างไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="50bd3-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="50bd3-122">เพิ่มสมาชิกอื่น ๆ ที่เป็นส่วนหนึ่งของลำดับชั้นขององค์กรระดับการเข้าถึงของการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="50bd3-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![การเพิ่มสมาชิก](./media/CA-picture-2.png)

<span data-ttu-id="50bd3-124">ผู้ใช้ที่ถูกเพิ่มไปยังบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** จะเห็นเฉพาะข้อมูลที่พวกเขาได้รับอนุญาตให้ดู ตามข้อกำหนดในลำดับชั้นขององค์กรระดับการเข้าถึงของการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="50bd3-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="50bd3-125">ความปลอดภัยระดับแถวนำไปใช้กับไทล์และรายงานที่ถูกฝังจาก Power BI</span><span class="sxs-lookup"><span data-stu-id="50bd3-125">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="50bd3-126">การอัพเดตความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="50bd3-126">Updating security</span></span>
<span data-ttu-id="50bd3-127">ถ้ามีการทำการปรับปรุงไปยังความปลอดภัยระดับการเข้าถึงในการบัญชีต้นทุน และคุณต้องการ Power BI เพื่อสะท้อนการปรับปรุงเหล่านั้น คุณต้องปรับปรุงร้านค้าเอนทิตีสำหรับเนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="50bd3-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="50bd3-128">หลังจากที่คุณอัพเดตที่จัดเก็บเอนทิตีแล้ว คุณต้องอัพเดตวัตถุบน PowerBI.com</span><span class="sxs-lookup"><span data-stu-id="50bd3-128">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="50bd3-129">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการอัพเดตร้านค้าเอนทิตี ดูที่ [อัพเดตร้านค้าเอนทิตี](power-bi-integration-entity-store.md#update-entity-store)</span><span class="sxs-lookup"><span data-stu-id="50bd3-129">For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="50bd3-130">เจ้าของเนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน** ยังต้องทำการปรับปรุงร้านค้าเอนทิตี ถ้ามีการให้การเข้าถึงแก่ผู้ใช้ใหม่ไปยังลำดับชั้นเชิงองค์กร</span><span class="sxs-lookup"><span data-stu-id="50bd3-130">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="50bd3-131">นอกจากนี้ เจ้าของต้องเพิ่มผู้ใช้ใหม่ไปยังบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** บน PowerBI.com เพื่อให้ความปลอดภัยระดับแถวนั้นถูกนำไปใช้กับพวกเขา</span><span class="sxs-lookup"><span data-stu-id="50bd3-131">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="50bd3-132">การปิดใช้งานความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="50bd3-132">Disabling security</span></span>
<span data-ttu-id="50bd3-133">เราสมมติว่าองค์กรของคุณต้องการจำกัดการเข้าถึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="50bd3-133">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="50bd3-134">ถ้า ด้วยเหตุผลบางอย่าง พารามิเตอร์ความปลอดภัยถูกปิดใช้งาน เมื่อคุณรันการบัญชีต้นทุน เจ้าของต้องเพิ่มผู้ใช้บทบาท **นักบัญชีต้นทุน** ใน Power BI แทน</span><span class="sxs-lookup"><span data-stu-id="50bd3-134">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="50bd3-135">ถ้าคุณเปลี่ยนความปลอดภัยจากสถานะที่เปิดใช้งานไปเป็นสถานะที่ปิดใช้งาน คุณควรลบผู้ใช้ออกจากบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="50bd3-135">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="50bd3-136">และในทางกลับกัน ถ้าคุณเปิดใช้งานความปลอดภัยอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="50bd3-136">And vice versa if you re-enable security.</span></span> <span data-ttu-id="50bd3-137">ผู้ใช้อาจเป็นสมาชิกของทั้งสองบทบาท</span><span class="sxs-lookup"><span data-stu-id="50bd3-137">Users can belong to both roles.</span></span> <span data-ttu-id="50bd3-138">การเข้าถึงร่วมกันคือการรวมทั้งสองบทบาท</span><span class="sxs-lookup"><span data-stu-id="50bd3-138">Joint access is the union of both roles.</span></span> <span data-ttu-id="50bd3-139">ในกรณีของเนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน** ผู้ใช้ที่มีการเข้าถึงการเข้าร่วมมีการเข้าถึงข้อมูลที่ไม่จำกัด</span><span class="sxs-lookup"><span data-stu-id="50bd3-139">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="50bd3-140">ถ้าเป้าหมายของคุณคือการจำกัดการเข้าถึง จะต้องกำหนดผู้ใช้ไปยังบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="50bd3-140">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="50bd3-141">การอัพเดตความปลอดภัยระดับแถวเหล่านี้จะมีผลทันที</span><span class="sxs-lookup"><span data-stu-id="50bd3-141">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="50bd3-142">ผู้ใช้ที่ได้รับผลกระทบควรรีเฟรชเบราว์เซอร์ของตน</span><span class="sxs-lookup"><span data-stu-id="50bd3-142">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="50bd3-143">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="50bd3-143">Additional resources</span></span>
<span data-ttu-id="50bd3-144">เพื่อเรียนรู้เพิ่มเติมเกี่ยวกับความปลอดภัยระดับแถวของ Power BI ดู [จัดการความปลอดภัยในแบบจำลองของคุณใน Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model)</span><span class="sxs-lookup"><span data-stu-id="50bd3-144">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>
