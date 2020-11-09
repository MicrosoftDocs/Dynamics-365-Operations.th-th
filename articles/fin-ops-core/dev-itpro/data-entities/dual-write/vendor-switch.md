---
title: สลับการออกแบบของผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายวิธีสลับการรวมข้อมูลของผู้จัดจำหน่ายระหว่างแอป Finance and Operations และ Common Data Service
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997563"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="3c551-103">สลับการออกแบบของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="3c551-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="3c551-104">โฟลว์ข้อมูลของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="3c551-104">Vendor data flow</span></span> 

<span data-ttu-id="3c551-105">ถ้าคุณเลือกที่จะใช้เอนทิตี้ **บัญชี** เพื่อจัดเก็บผู้จัดจำหน่ายของชนิด **องค์กร** และเอนทิตี้ **ผู้ติดต่อ** เพื่อจัดเก็บผู้จัดจำหน่ายของชนิด **บุคคล** ให้ตั้งค่าคอนฟิกลำดับงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3c551-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="3c551-106">มิฉะนั้น ไม่จำเป็นต้องมีการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="3c551-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="3c551-107">ใช้การออกแบบของผู้จัดจำหน่ายแบบขยายสำหรับผู้จัดจำหน่ายชนิดองค์กร</span><span class="sxs-lookup"><span data-stu-id="3c551-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="3c551-108">แพคเกจโซลูชัน **Dynamics365FinanceExtended** ประกอบด้วยเท็มเพลตการประมวลผลลำดับงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3c551-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="3c551-109">คุณจะสร้างลำดับงานสำหรับเท็มเพลตแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="3c551-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="3c551-110">สร้างผู้จัดจำหน่ายในเอนทิตี้บัญชี</span><span class="sxs-lookup"><span data-stu-id="3c551-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="3c551-111">สร้างผู้จัดจำหน่ายในเอนทิตีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="3c551-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="3c551-112">ปรับปรุงผู้จัดจำหน่ายในเอนทิตี้บัญชี</span><span class="sxs-lookup"><span data-stu-id="3c551-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="3c551-113">ปรับปรุงผู้จัดจำหน่ายในเอนทิตีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="3c551-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="3c551-114">เพื่อสร้างกระบวนการลำดับงานใหม่โดยใช้เท็มเพลตการประมวลผลลำดับงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="3c551-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="3c551-115">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **ผู้จัดจำหน่าย** และเลือกเท็มเพลตกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายในเอนทิตี้บัญชี**</span><span class="sxs-lookup"><span data-stu-id="3c551-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="3c551-116">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3c551-116">Then select **OK**.</span></span> <span data-ttu-id="3c551-117">ลำดับงานนี้จะจัดการสถานการณ์จำลองการสร้างผู้จัดจำหน่าย สำหรับเอนทิตี **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="3c551-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![สร้างผู้จัดจำหน่ายในกระบวนการลำดับงานเอนทิตี้บัญชี](media/create_process.png)

2. <span data-ttu-id="3c551-119">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **ผู้จัดจำหน่าย** และเลือกเท็มเพลตกระบวนการลำดับงาน **ปรับปรุงผู้จัดจำหน่ายในเอนทิตี้บัญชี**</span><span class="sxs-lookup"><span data-stu-id="3c551-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="3c551-120">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3c551-120">Then select **OK**.</span></span> <span data-ttu-id="3c551-121">ลำดับงานนี้จะจัดการสถานการณ์จำลองการอัปเดตผู้จัดจำหน่าย สำหรับเอนทิตี **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="3c551-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="3c551-122">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **บัญชี** และเลือกเท็มเพลตกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายในเอนทิตี้ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="3c551-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="3c551-123">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **บัญชี** และเลือกเท็มเพลตกระบวนการลำดับงาน **ปรับปรุงผู้จัดจำหน่ายในเอนทิตี้ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="3c551-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="3c551-124">คุณสามารถตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานแบบเรียลไทม์ หรือลำดับงานพื้นหลัง อย่างใดอย่างหนึ่ง โดยขึ้นอยู่กับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="3c551-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="3c551-125">เมื่อต้องการตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานพื้นหลัง เลือก **แปลงเป็นลำดับงานพื้นหลัง**</span><span class="sxs-lookup"><span data-stu-id="3c551-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![ปุ่มแปลงเป็นลำดับงานพื้นหลัง](media/background_workflow.png)

6. <span data-ttu-id="3c551-127">เปิดใช้ลำดับงานที่คุณสร้างขึ้นสำหรับเอนทิตี้ **บัญชี** และ **ผู้จัดจำหน่าย** เพื่อเริ่มต้นใช้งานเอนทิตี้ **บัญชี** เพื่อจัดเก็บข้อมูลสำหรับผู้จัดจำหน่ายของชนิด **องค์กร**</span><span class="sxs-lookup"><span data-stu-id="3c551-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="3c551-128">ใช้การออกแบบของผู้จัดจำหน่ายแบบขยายสำหรับผู้จัดจำหน่ายชนิดบุคคล</span><span class="sxs-lookup"><span data-stu-id="3c551-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="3c551-129">แพคเกจโซลูชัน **Dynamics365FinanceExtended** ประกอบด้วยเท็มเพลตการประมวลผลลำดับงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3c551-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="3c551-130">คุณจะสร้างลำดับงานสำหรับเท็มเพลตแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="3c551-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="3c551-131">สร้างผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="3c551-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="3c551-132">สร้างผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="3c551-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="3c551-133">ปรับปรุงผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="3c551-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="3c551-134">ปรับปรุงผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="3c551-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="3c551-135">เพื่อสร้างกระบวนการลำดับงานใหม่โดยใช้เท็มเพลตการประมวลผลลำดับงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="3c551-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="3c551-136">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **ผู้จัดจำหน่าย** และเลือกเท็มเพลตกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="3c551-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="3c551-137">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3c551-137">Then select **OK**.</span></span> <span data-ttu-id="3c551-138">ลำดับงานนี้จะจัดการสถานการณ์จำลองการสร้างผู้จัดจำหน่ายสำหรับเอนทิตี **ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="3c551-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="3c551-139">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **ผู้จัดจำหน่าย** และเลือกเท็มเพลตกระบวนการลำดับงาน **ปรับปรุงผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="3c551-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="3c551-140">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3c551-140">Then select **OK**.</span></span> <span data-ttu-id="3c551-141">ลำดับงานนี้จะจัดการสถานการณ์จำลองการปรับปรุงผู้จัดจำหน่ายสำหรับเอนทิตี้ **ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="3c551-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="3c551-142">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **ผู้ติดต่อ** และเลือกเท็มเพลต **สร้างผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="3c551-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="3c551-143">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **ผู้ติดต่อ** และเลือกเท็มเพลต **ปรับปรุงผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="3c551-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="3c551-144">คุณสามารถตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานแบบเรียลไทม์ หรือลำดับงานพื้นหลัง อย่างใดอย่างหนึ่ง โดยขึ้นอยู่กับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="3c551-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="3c551-145">เมื่อต้องการตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานพื้นหลัง เลือก **แปลงเป็นลำดับงานพื้นหลัง**</span><span class="sxs-lookup"><span data-stu-id="3c551-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="3c551-146">เปิดใช้ลำดับงานที่คุณสร้างขึ้นในเอนทิตี้ **ผู้ติดต่อ** และเอนทิตี้ **ผู้จัดจำหน่าย** เพื่อเริ่มต้นใช้งานเอนทิตี้ **ผู้ติดต่อ** เพื่อจัดเก็บข้อมูลสำหรับผู้จัดจำหน่ายของชนิด **บุคคล**</span><span class="sxs-lookup"><span data-stu-id="3c551-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
