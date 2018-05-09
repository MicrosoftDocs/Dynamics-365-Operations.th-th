---
title: "ตั้งค่าความปลอดภัยสำหรับเนื้อหา Power BI เกี่ยวกับการบัญชีต้นทุน"
description: "หัวข้อนี้อธิบายวิธีที่คุณสามารถถ่ายทอดความปลอดภัยระดับการเข้าถึงในการบัญชีต้นทุนไปยังความปลอดภัยระดับแถวใน Microsoft Power BI ฟังก์ชันนี้ช่วยรับประกันว่าผู้ใช้จะเห็นเฉพาะข้อมูล Power BI ที่พวกเขาได้รับสิทธิ์การเข้าถึง"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 86de46818abc6ea653076c2a6f38c40bbaab18d8
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="ab3db-104">ตั้งค่าความปลอดภัยสำหรับเนื้อหา Power BI เกี่ยวกับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ab3db-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab3db-105">หัวข้อนี้อธิบายวิธีที่คุณสามารถถ่ายทอดความปลอดภัยระดับการเข้าถึงในการบัญชีต้นทุนไปยังความปลอดภัยระดับแถวใน Microsoft Power BI</span><span class="sxs-lookup"><span data-stu-id="ab3db-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="ab3db-106">ฟังก์ชันนี้ช่วยรับประกันว่าผู้ใช้จะเห็นเฉพาะข้อมูล Power BI ที่พวกเขาได้รับสิทธิ์การเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="ab3db-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

<a name="overview"></a><span data-ttu-id="ab3db-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="ab3db-107">Overview</span></span>
--------

<span data-ttu-id="ab3db-108">เนื้อหา Microsoft Power BI **การวิเคราะห์การบัญชีต้นทุน** ใช้ความปลอดภัยระดับแถวของ Power BI เพื่อจำกัดการเข้าถึงของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ab3db-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="ab3db-109">ความปลอดภัยขึ้นอยู่กับลำดับชั้นขององค์กรระดับการเข้าถึงที่ถูกตั้งค่าในพารามิเตอร์การบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ab3db-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="ab3db-110">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเนื้อหา Power BI **การวิเคราะห์การบัญชีต้นทุน** ดูที่ [เนื้อหา Power BI การวิเคราะห์การบัญชีต้นทุน](cost-accounting-analysis-content-pack.md)</span><span class="sxs-lookup"><span data-stu-id="ab3db-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="ab3db-111">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="ab3db-111">Setup</span></span>
<span data-ttu-id="ab3db-112">เพื่อถ่ายทอดความปลอดภัยระดับการเข้าถึงไปยัง Power BI เจ้าของเนื้อหา Power BI ต้องทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="ab3db-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span> <span data-ttu-id="ab3db-113">**หมายเหตุ:** ผู้ใช้ที่เผยแพร่เนื้อหา Power BI **การวิเคราะห์การบัญชีต้นทุน** จะกลายเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="ab3db-113">**Note:** The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="ab3db-114">เฉพาะเจ้าของที่สามารถตั้งค่าความปลอดภัยใน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="ab3db-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="ab3db-115">นอกจากนี้ จนกว่าเจ้าของจะเพิ่มผู้ใช้รายอื่นบน PowerBI.com จะไม่มีผู้ใดสามารถดูข้อมูลใด ๆ ในเนื้อหา Power BI **การวิเคราะห์การบัญชีต้นทุน** ได้นอกจากเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="ab3db-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1.  <span data-ttu-id="ab3db-116">เผยแพร่ไฟล์ข้อกำหนดใน Power BI</span><span class="sxs-lookup"><span data-stu-id="ab3db-116">Publish the definition file to Power BI.</span></span>
2.  <span data-ttu-id="ab3db-117">ลงชื่อเข้าใช้ไปยัง PowerBI.com</span><span class="sxs-lookup"><span data-stu-id="ab3db-117">Sign in to PowerBI.com.</span></span>
3.  <span data-ttu-id="ab3db-118">ค้นหาชุดข้อมูลเนื้อหา Power BI **การวิเคราะห์การบัญชีต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="ab3db-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4.  <span data-ttu-id="ab3db-119">เปิดหน้าความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="ab3db-119">Open the security page.</span></span> 

    ![กำลังเปิดหน้าความปลอดภัย](./media/CA-picture-1.png)

5.  <span data-ttu-id="ab3db-121">บทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** ถูกสร้างไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="ab3db-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="ab3db-122">เพิ่มสมาชิกอื่น ๆ ที่เป็นส่วนหนึ่งของลำดับชั้นขององค์กรระดับการเข้าถึงของการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ab3db-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span> 

    ![การเพิ่มสมาชิก](./media/CA-picture-2.png)

<span data-ttu-id="ab3db-124">ผู้ใช้ที่ถูกเพิ่มไปยังบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** จะเห็นเฉพาะข้อมูลที่พวกเขาได้รับอนุญาตให้ดู ตามข้อกำหนดในลำดับชั้นขององค์กรระดับการเข้าถึงของการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ab3db-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span> <span data-ttu-id="ab3db-125">**หมายเหตุ:** ความปลอดภัยระดับแถวใช้ไทล์และรายงานใน Microsoft Dynamics 365 for Finance and Operations ที่ฝังอยู่จาก Power BI</span><span class="sxs-lookup"><span data-stu-id="ab3db-125">**Note:** Row-level security applies to tiles and reports in Microsoft Dynamics 365 for Finance and Operations that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="ab3db-126">การอัพเดตความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="ab3db-126">Updating security</span></span>
<span data-ttu-id="ab3db-127">ถ้ามีการอัพเดตความปลอดภัยระดับการเข้าถึงในการบัญชีต้นทุน และคุณต้องการให้ Power BI สะท้อนถึงการอัพเดตเหล่านั้น คุณต้องอัพเดตร้านค้าเอนทิตีสำหรับเนื้อหา Power BI **การวิเคราะห์การบัญชีต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="ab3db-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="ab3db-128">หลังจากที่คุณอัพเดตร้านค้าเอนทิตีจาก Dynamics 365 for Finance and Operations เสร็จสมบูรณ์แล้ว คุณต้องอัพเดตวัตถุบน PowerBI.com สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการอัพเดตร้านค้าเอนทิตี ดูที่ [อัพเดตร้านค้าเอนทิตี](power-bi-integration-entity-store.md#update-entity-store)</span><span class="sxs-lookup"><span data-stu-id="ab3db-128">After you complete the entity store update from Finance and Operations, you must update the artifacts on PowerBI.com. For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="ab3db-129">เจ้าของเนื้อหา Power BI **การวิเคราะห์การบัญชีต้นทุน** ยังต้องอัพเดตร้านค้าเอนทิตี ถ้าผู้ใช้ใหม่ได้รับสิทธิ์การเข้าถึงไปยังลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="ab3db-129">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="ab3db-130">นอกจากนี้ เจ้าของต้องเพิ่มผู้ใช้ใหม่ไปยังบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** บน PowerBI.com เพื่อให้ความปลอดภัยระดับแถวนั้นถูกนำไปใช้กับพวกเขา</span><span class="sxs-lookup"><span data-stu-id="ab3db-130">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="ab3db-131">การปิดใช้งานความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="ab3db-131">Disabling security</span></span>
<span data-ttu-id="ab3db-132">เราสมมติว่าองค์กรของคุณต้องการจำกัดการเข้าถึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ab3db-132">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="ab3db-133">ถ้าพารามิเตอร์ความปลอดภัยถูกปิดใช้งานเมื่อคุณเรียกใช้การบัญชีต้นทุนเนื่องด้วยเหตุผลบางประการ เจ้าของจะต้องเพิ่มผู้ใช้ไปยังบทบาท **นักบัญชีต้นทุน** ใน Power BI แทน</span><span class="sxs-lookup"><span data-stu-id="ab3db-133">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="ab3db-134">ถ้าคุณเปลี่ยนความปลอดภัยจากสถานะที่เปิดใช้งานไปเป็นสถานะที่ปิดใช้งาน คุณควรลบผู้ใช้ออกจากบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="ab3db-134">If you change security from an enabled state to a disabled state, it’s a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="ab3db-135">และในทางกลับกัน ถ้าคุณเปิดใช้งานความปลอดภัยอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="ab3db-135">And vice versa if you re-enable security.</span></span> <span data-ttu-id="ab3db-136">ผู้ใช้อาจเป็นสมาชิกของทั้งสองบทบาท</span><span class="sxs-lookup"><span data-stu-id="ab3db-136">Users can belong to both roles.</span></span> <span data-ttu-id="ab3db-137">การเข้าถึงร่วมกันคือการรวมทั้งสองบทบาท</span><span class="sxs-lookup"><span data-stu-id="ab3db-137">Joint access is the union of both roles.</span></span> <span data-ttu-id="ab3db-138">ในกรณีของเนื้อหา Power BI **การวิเคราะห์การบัญชีต้นทุน** ผู้ใช้ที่มีการเข้าถึงร่วมกันจะมีการเข้าถึงข้อมูลที่ไม่จำกัด</span><span class="sxs-lookup"><span data-stu-id="ab3db-138">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="ab3db-139">ถ้าเป้าหมายของคุณคือการจำกัดการเข้าถึง จะต้องกำหนดผู้ใช้ไปยังบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ab3db-139">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="ab3db-140">การอัพเดตความปลอดภัยระดับแถวเหล่านี้จะมีผลทันที</span><span class="sxs-lookup"><span data-stu-id="ab3db-140">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="ab3db-141">ผู้ใช้ที่ได้รับผลกระทบควรรีเฟรชเบราว์เซอร์ของตน</span><span class="sxs-lookup"><span data-stu-id="ab3db-141">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab3db-142">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ab3db-142">Additional resources</span></span>
<span data-ttu-id="ab3db-143">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับความปลอดภัยระดับแถวของ Power BI ดูที่ [จัดการความปลอดภัยบนแบบจำลองของคุณใน Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model)</span><span class="sxs-lookup"><span data-stu-id="ab3db-143">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>




