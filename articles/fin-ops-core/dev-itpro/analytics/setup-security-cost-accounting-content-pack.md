---
title: ตั้งค่าความปลอดภัยสำหรับเนื้อหา Power BI ของการวิเคราะห์การบัญชีต้นทุน
description: หัวข้อนี้อธิบายวิธีการที่คุณสามารถเผยแพร่ความปลอดภัยระดับการเข้าถึงในการบัญชีต้นทุนไปยังความปลอดภัยระดับแถวใน Microsoft Power BI
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d54ced21de112288c2f98c0bc895ca0d49c217e3
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093366"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="931cc-103">ตั้งค่าความปลอดภัยสำหรับเนื้อหาของ Power BI เกี่ยวกับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="931cc-103">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="931cc-104">หัวข้อนี้อธิบายวิธีการที่คุณสามารถเผยแพร่ความปลอดภัยระดับการเข้าถึงในการบัญชีต้นทุนไปยังความปลอดภัยระดับแถวใน Microsoft Power BI</span><span class="sxs-lookup"><span data-stu-id="931cc-104">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="931cc-105">ฟังก์ชันนี้ช่วยรับประกันว่าผู้ใช้เห็นเฉพาะข้อมูล Power BI ที่พวกเขาได้รับอนุญาตให้เข้าถึง</span><span class="sxs-lookup"><span data-stu-id="931cc-105">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="931cc-106">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="931cc-106">Overview</span></span>

<span data-ttu-id="931cc-107">เนื้อหา Microsoft Power BI ของ **การวิเคราะห์การบัญชีต้นทุน** ใช้ความปลอดภัยระดับแถวของ Power BI เพื่อจำกัดการเข้าถึงของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="931cc-107">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="931cc-108">ความปลอดภัยขึ้นอยู่กับลำดับชั้นขององค์กรระดับการเข้าถึงที่ถูกตั้งค่าในพารามิเตอร์การบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="931cc-108">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="931cc-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน** ดู [เนื้อหา Power BI ของการวิเคราะห์การบัญชีต้นทุน](cost-accounting-analysis-content-pack.md)</span><span class="sxs-lookup"><span data-stu-id="931cc-109">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="931cc-110">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="931cc-110">Setup</span></span>
<span data-ttu-id="931cc-111">เพื่อเผยแพร่ความปลอดภัยระดับการเข้าถึงไปยัง Power BI เจ้าของเนื้อหา Power BI ต้องทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="931cc-111">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="931cc-112">ผู้ใช้ที่เผยแพร่เนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน** กลายเป็นเจ้าของโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="931cc-112">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="931cc-113">เฉพาะเจ้าของสามารถตั้งค่าความปลอดภัยใน Power BI</span><span class="sxs-lookup"><span data-stu-id="931cc-113">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="931cc-114">นอกจากนี้ จนกว่าเจ้าของจะเพิ่มผู้ใช้อื่นใน PowerBI.com ไม่มีใครนอกจากเจ้าของที่สามารถมองเห็นข้อมูลใดๆ ในเนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="931cc-114">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="931cc-115">เผยแพร่ไฟล์ข้อกำหนดไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="931cc-115">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="931cc-116">ลงชื่อเข้าใช้ไปยัง PowerBI.com</span><span class="sxs-lookup"><span data-stu-id="931cc-116">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="931cc-117">ค้นหาชุดข้อมูลสำหรับเนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="931cc-117">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="931cc-118">เปิดหน้าความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="931cc-118">Open the security page.</span></span>

    ![กำลังเปิดหน้าความปลอดภัย](./media/CA-picture-1.png)

5. <span data-ttu-id="931cc-120">บทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** ถูกสร้างไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="931cc-120">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="931cc-121">เพิ่มสมาชิกอื่น ๆ ที่เป็นส่วนหนึ่งของลำดับชั้นขององค์กรระดับการเข้าถึงของการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="931cc-121">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![การเพิ่มสมาชิก](./media/CA-picture-2.png)

<span data-ttu-id="931cc-123">ผู้ใช้ที่ถูกเพิ่มไปยังบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** จะเห็นเฉพาะข้อมูลที่พวกเขาได้รับอนุญาตให้ดู ตามข้อกำหนดในลำดับชั้นขององค์กรระดับการเข้าถึงของการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="931cc-123">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="931cc-124">ความปลอดภัยระดับแถวนำไปใช้กับไทล์และรายงานที่ถูกฝังจาก Power BI</span><span class="sxs-lookup"><span data-stu-id="931cc-124">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="931cc-125">การอัพเดตความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="931cc-125">Updating security</span></span>
<span data-ttu-id="931cc-126">ถ้ามีการทำการปรับปรุงไปยังความปลอดภัยระดับการเข้าถึงในการบัญชีต้นทุน และคุณต้องการ Power BI เพื่อสะท้อนการปรับปรุงเหล่านั้น คุณต้องปรับปรุงร้านค้าเอนทิตีสำหรับเนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="931cc-126">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="931cc-127">หลังจากที่คุณอัพเดตที่จัดเก็บเอนทิตีแล้ว คุณต้องอัพเดตวัตถุบน PowerBI.com</span><span class="sxs-lookup"><span data-stu-id="931cc-127">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="931cc-128">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการอัพเดตร้านค้าเอนทิตี ดูที่ [การรวม Power BI กับร้านค้าเอนทิตี](power-bi-integration-entity-store.md#update-entity-store)</span><span class="sxs-lookup"><span data-stu-id="931cc-128">For more information about how to do an entity store update, see [Power BI integration with Entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="931cc-129">เจ้าของเนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน** ยังต้องทำการปรับปรุงร้านค้าเอนทิตี ถ้ามีการให้การเข้าถึงแก่ผู้ใช้ใหม่ไปยังลำดับชั้นเชิงองค์กร</span><span class="sxs-lookup"><span data-stu-id="931cc-129">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="931cc-130">นอกจากนี้ เจ้าของต้องเพิ่มผู้ใช้ใหม่ไปยังบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** บน PowerBI.com เพื่อให้ความปลอดภัยระดับแถวนั้นถูกนำไปใช้กับพวกเขา</span><span class="sxs-lookup"><span data-stu-id="931cc-130">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="931cc-131">การปิดใช้งานความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="931cc-131">Disabling security</span></span>
<span data-ttu-id="931cc-132">เราสมมติว่าองค์กรของคุณต้องการจำกัดการเข้าถึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="931cc-132">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="931cc-133">ถ้า ด้วยเหตุผลบางอย่าง พารามิเตอร์ความปลอดภัยถูกปิดใช้งาน เมื่อคุณรันการบัญชีต้นทุน เจ้าของต้องเพิ่มผู้ใช้บทบาท **นักบัญชีต้นทุน** ใน Power BI แทน</span><span class="sxs-lookup"><span data-stu-id="931cc-133">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="931cc-134">ถ้าคุณเปลี่ยนความปลอดภัยจากสถานะที่เปิดใช้งานไปเป็นสถานะที่ปิดใช้งาน คุณควรลบผู้ใช้ออกจากบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="931cc-134">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="931cc-135">และในทางกลับกัน ถ้าคุณเปิดใช้งานความปลอดภัยอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="931cc-135">And vice versa if you re-enable security.</span></span> <span data-ttu-id="931cc-136">ผู้ใช้อาจเป็นสมาชิกของทั้งสองบทบาท</span><span class="sxs-lookup"><span data-stu-id="931cc-136">Users can belong to both roles.</span></span> <span data-ttu-id="931cc-137">การเข้าถึงร่วมกันคือการรวมทั้งสองบทบาท</span><span class="sxs-lookup"><span data-stu-id="931cc-137">Joint access is the union of both roles.</span></span> <span data-ttu-id="931cc-138">ในกรณีของเนื้อหา Power BI ของ **การวิเคราะห์การบัญชีต้นทุน** ผู้ใช้ที่มีการเข้าถึงการเข้าร่วมมีการเข้าถึงข้อมูลที่ไม่จำกัด</span><span class="sxs-lookup"><span data-stu-id="931cc-138">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="931cc-139">ถ้าเป้าหมายของคุณคือการจำกัดการเข้าถึง จะต้องกำหนดผู้ใช้ไปยังบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="931cc-139">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="931cc-140">การอัพเดตความปลอดภัยระดับแถวเหล่านี้จะมีผลทันที</span><span class="sxs-lookup"><span data-stu-id="931cc-140">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="931cc-141">ผู้ใช้ที่ได้รับผลกระทบควรรีเฟรชเบราว์เซอร์ของตน</span><span class="sxs-lookup"><span data-stu-id="931cc-141">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="931cc-142">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="931cc-142">Additional resources</span></span>
<span data-ttu-id="931cc-143">เพื่อเรียนรู้เพิ่มเติมเกี่ยวกับความปลอดภัยระดับแถวของ Power BI ดู [จัดการความปลอดภัยในแบบจำลองของคุณใน Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model)</span><span class="sxs-lookup"><span data-stu-id="931cc-143">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>
