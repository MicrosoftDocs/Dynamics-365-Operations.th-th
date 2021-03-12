---
title: สลับการออกแบบของผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายวิธีสลับการรวมข้อมูลของผู้จัดจำหน่ายระหว่างแอป Finance and Operations และ Dataverse
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
ms.openlocfilehash: d2c22123d5f05945b34eb107c5b912852aec387a
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744476"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="78243-103">สลับการออกแบบของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="78243-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="78243-104">โฟลว์ข้อมูลของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="78243-104">Vendor data flow</span></span> 

<span data-ttu-id="78243-105">ถ้าคุณเลือกที่จะใช้ตาราง **บัญชี** เพื่อจัดเก็บผู้จัดจำหน่ายของชนิด **องค์กร** และตาราง **ผู้ติดต่อ** เพื่อจัดเก็บผู้จัดจำหน่ายของชนิด **บุคคล** ให้ตั้งค่าคอนฟิกลำดับงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="78243-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="78243-106">มิฉะนั้น ไม่จำเป็นต้องมีการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="78243-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="78243-107">ใช้การออกแบบของผู้จัดจำหน่ายแบบขยายสำหรับผู้จัดจำหน่ายชนิดองค์กร</span><span class="sxs-lookup"><span data-stu-id="78243-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="78243-108">แพคเกจโซลูชัน **Dynamics365FinanceExtended** ประกอบด้วยเท็มเพลตการประมวลผลลำดับงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="78243-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="78243-109">คุณจะสร้างลำดับงานสำหรับเท็มเพลตแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="78243-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="78243-110">สร้างผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="78243-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="78243-111">สร้างผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="78243-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="78243-112">อัปเดตผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="78243-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="78243-113">อัปเดตผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="78243-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="78243-114">เพื่อสร้างกระบวนการลำดับงานใหม่โดยใช้เท็มเพลตการประมวลผลลำดับงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="78243-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="78243-115">สร้างกระบวนการลำดับงานสำหรับตาราง **ผู้จัดจำหน่าย** และเลือกแม่แบบกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายในตารางบัญชี**</span><span class="sxs-lookup"><span data-stu-id="78243-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="78243-116">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="78243-116">Then select **OK**.</span></span> <span data-ttu-id="78243-117">ลำดับงานนี้จะจัดการสถานการณ์จำลองการสร้างผู้จัดจำหน่าย สำหรับตาราง **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="78243-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![สร้างผู้จัดจำหน่ายในกระบวนการลำดับงานตารางบัญชี](media/create_process.png)

2. <span data-ttu-id="78243-119">สร้างกระบวนการลำดับงานสำหรับตาราง **ผู้จัดจำหน่าย** และเลือกแม่แบบกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายในตารางบัญชี**</span><span class="sxs-lookup"><span data-stu-id="78243-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="78243-120">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="78243-120">Then select **OK**.</span></span> <span data-ttu-id="78243-121">ลำดับงานนี้จะจัดการสถานการณ์จำลองการอัปเดตผู้จัดจำหน่าย สำหรับตาราง **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="78243-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="78243-122">สร้างกระบวนการลำดับงานสำหรับตาราง **บัญชี** และเลือกแม่แบบกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="78243-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="78243-123">สร้างกระบวนการลำดับงานสำหรับตาราง **บัญชี** และเลือกแม่แบบกระบวนการลำดับงาน **อัปเดตผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="78243-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="78243-124">คุณสามารถตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานแบบเรียลไทม์ หรือลำดับงานพื้นหลัง อย่างใดอย่างหนึ่ง โดยขึ้นอยู่กับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="78243-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="78243-125">เมื่อต้องการตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานพื้นหลัง เลือก **แปลงเป็นลำดับงานพื้นหลัง**</span><span class="sxs-lookup"><span data-stu-id="78243-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![ปุ่มแปลงเป็นลำดับงานพื้นหลัง](media/background_workflow.png)

6. <span data-ttu-id="78243-127">เปิดใช้ลำดับงานที่คุณสร้างขึ้นสำหรับตาราง **บัญชี** และ **ผู้จัดจำหน่าย** เพื่อเริ่มต้นใช้งานตาราง **บัญชี** เพื่อจัดเก็บข้อมูลสำหรับผู้จัดจำหน่ายของชนิด **องค์กร**</span><span class="sxs-lookup"><span data-stu-id="78243-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="78243-128">ใช้การออกแบบของผู้จัดจำหน่ายแบบขยายสำหรับผู้จัดจำหน่ายชนิดบุคคล</span><span class="sxs-lookup"><span data-stu-id="78243-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="78243-129">แพคเกจโซลูชัน **Dynamics365FinanceExtended** ประกอบด้วยเท็มเพลตการประมวลผลลำดับงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="78243-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="78243-130">คุณจะสร้างลำดับงานสำหรับเท็มเพลตแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="78243-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="78243-131">สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="78243-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="78243-132">สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="78243-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="78243-133">อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="78243-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="78243-134">อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="78243-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="78243-135">เพื่อสร้างกระบวนการลำดับงานใหม่โดยใช้เท็มเพลตการประมวลผลลำดับงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="78243-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="78243-136">สร้างกระบวนการลำดับงานสำหรับตาราง **ผู้จัดจำหน่าย** และเลือกเท็มเพลตกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="78243-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="78243-137">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="78243-137">Then select **OK**.</span></span> <span data-ttu-id="78243-138">ลำดับงานนี้จะจัดการสถานการณ์จำลองการสร้างผู้จัดจำหน่ายสำหรับตาราง **ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="78243-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="78243-139">สร้างกระบวนการลำดับงานสำหรับตาราง **ผู้จัดจำหน่าย** และเลือกแม่แบบกระบวนการลำดับงาน **อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="78243-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="78243-140">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="78243-140">Then select **OK**.</span></span> <span data-ttu-id="78243-141">ลำดับงานนี้จะจัดการสถานการณ์จำลองการปรับปรุงผู้จัดจำหน่ายสำหรับตาราง **ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="78243-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="78243-142">สร้างกระบวนการลำดับงานสำหรับตาราง **ผู้ติดต่อ** และเลือกแม่แบบ **สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="78243-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="78243-143">สร้างกระบวนการลำดับงานสำหรับตาราง **ผู้ติดต่อ** และเลือกแม่แบบ **อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="78243-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="78243-144">คุณสามารถตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานแบบเรียลไทม์ หรือลำดับงานพื้นหลัง อย่างใดอย่างหนึ่ง โดยขึ้นอยู่กับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="78243-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="78243-145">เมื่อต้องการตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานพื้นหลัง เลือก **แปลงเป็นลำดับงานพื้นหลัง**</span><span class="sxs-lookup"><span data-stu-id="78243-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="78243-146">เปิดใช้ลำดับงานที่คุณสร้างขึ้นในเอนทิตี **ผู้ติดต่อ** และเอนทิตี **ผู้จัดจำหน่าย** เพื่อเริ่มต้นใช้งานตาราง **ผู้ติดต่อ** เพื่อจัดเก็บข้อมูลสำหรับผู้จัดจำหน่ายของชนิด **บุคคล**</span><span class="sxs-lookup"><span data-stu-id="78243-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>
