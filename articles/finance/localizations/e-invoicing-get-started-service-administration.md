---
title: เริ่มต้นใช้งานการจัดการบริการ Add-On ของใบแจ้งหนี้ทางอิเล็กทรอนิกส์
description: หัวข้อนี้จะอธิบายวิธีการเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592537"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="cdb19-103">เริ่มต้นใช้งานการจัดการบริการ Add-On ของใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cdb19-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="cdb19-104">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="cdb19-104">Prerequisites</span></span>

<span data-ttu-id="cdb19-105">ก่อนที่คุณจะดำเนินการกระบวนงานต่างๆ ในหัวข้อนี้ให้เสร็จสมบูรณ์ ต้องมีข้อกำหนดเบื้องต้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cdb19-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="cdb19-106">คุณต้องมีสิทธิ์เข้าถึงบัญชี Microsoft Dynamics Lifecycle Services (LCS) ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cdb19-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="cdb19-107">คุณต้องมีโครงการ LCS ที่มีรุ่น 10.0.17 หรือใหม่กว่าของ Microsoft Dynamics 365 Finance และ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cdb19-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="cdb19-108">นอกจากนี้ แอปเหล่านี้ต้องถูกปรับใช้ในหนึ่งในภูมิศาสตร์ Azure ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cdb19-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="cdb19-109">สหรัฐอเมริกาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="cdb19-109">East US</span></span>
    - <span data-ttu-id="cdb19-110">สหรัฐอเมริกาตะวันตก</span><span class="sxs-lookup"><span data-stu-id="cdb19-110">West US</span></span>
    - <span data-ttu-id="cdb19-111">EU เหนือ</span><span class="sxs-lookup"><span data-stu-id="cdb19-111">North EU</span></span>
    - <span data-ttu-id="cdb19-112">EU ตะวันตก</span><span class="sxs-lookup"><span data-stu-id="cdb19-112">West EU</span></span>

- <span data-ttu-id="cdb19-113">คุณต้องมีสิทธิ์เข้าถึงบัญชี Dynamics 365 Regulatory Configuration Services (RCS) ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cdb19-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="cdb19-114">คุณต้องเปิดใช้งานคุณลักษณะที่ใช้ทั่วโลกสำหรับบัญชี RCS ของคุณในการจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="cdb19-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="cdb19-115">สำหรับข้อมูลเพิ่มเติม ดู [Regulatory Configuration Services (RCS) - คุณลักษณะที่ใช้ทั่วโลก](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="cdb19-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="cdb19-116">คุณต้องสร้าง Key Vault และบัญชีการจัดเก็บใน Azure</span><span class="sxs-lookup"><span data-stu-id="cdb19-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="cdb19-117">สำหรับข้อมูลเพิ่มเติม ดู [สร้างบัญชีการจัดเก็บของ Azure และ Key Vault](e-invoicing-create-azure-storage-account-key-vault.md)</span><span class="sxs-lookup"><span data-stu-id="cdb19-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="cdb19-118">ติดตั้ง Add-on สำหรับ microservices ใน Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="cdb19-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="cdb19-119">ลงชื่อเข้าใช้บัญชี LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cdb19-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="cdb19-120">เลือกไทล์ **การจัดการคุณลักษณะพรีวิว**</span><span class="sxs-lookup"><span data-stu-id="cdb19-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="cdb19-121">ในส่วน **คุณลักษณะพรีวิวสำหรับสาธารณะ** ให้เลือก **บริการออกใบแจ้งหนี้อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="cdb19-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="cdb19-122">ตรวจสอบให้แน่ใจว่าตัวเลือก **เปิดใช้งานคุณลักษณะพรีวิวแล้ว** ได้ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="cdb19-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="cdb19-123">บนกระดานข้อมูล LCS ของคุณ ให้เลือกโครงการปรับใช้ LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cdb19-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="cdb19-124">โครงการ LCS ต้องทำงานอยู่</span><span class="sxs-lookup"><span data-stu-id="cdb19-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="cdb19-125">บนแท็บ **add-in ของสภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="cdb19-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="cdb19-126">เลือก **บริการออกใบแจ้งหนี้อิเล็กทรอนิกส์** และในเขตข้อมูล **รหัสแอพลิเคชัน AAD** ให้ป้อน **091c98b0-a1c9-4b02-b62c-7753395ccabe**</span><span class="sxs-lookup"><span data-stu-id="cdb19-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="cdb19-127">ค่านี้เป็นค่าคงที่</span><span class="sxs-lookup"><span data-stu-id="cdb19-127">This is a fixed value.</span></span>
10. <span data-ttu-id="cdb19-128">ในเขตข้อมูล **รหัสผู้เช่า AAD** ป้อนรหัสผู้เช่าของบัญชีสมัครสมาชิก Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cdb19-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="cdb19-129">ตรวจสอบข้อกำหนดและเงื่อนไข จากนั้นเลือกกล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="cdb19-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="cdb19-130">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="cdb19-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="cdb19-131">ตั้งค่าพารามิเตอร์สำหรับการรวม RCS กับ add-on ใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cdb19-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="cdb19-132">ลงชื่อเข้าใช้บัญชี RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cdb19-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="cdb19-133">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ในส่วน **ลิงค์ที่เกี่ยวข้อง** ให้เลือก **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="cdb19-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="cdb19-134">บนแท็บ **บริการการออกใบแจ้งหนี้อิเล็กทรอนิกส์** ในฟิลด์ **URI ปลายทางของบริการ** ให้ป้อนปลายทางของบริการที่เหมาะสมสำหรับภูมิศาสตร์ Azure ของคุณ ดังแสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cdb19-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="cdb19-135">ภูมิศาสตร์ของ Datacenter Azure</span><span class="sxs-lookup"><span data-stu-id="cdb19-135">Datacenter Azure geography</span></span> | <span data-ttu-id="cdb19-136">URI ปลายทางของบริการ</span><span class="sxs-lookup"><span data-stu-id="cdb19-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="cdb19-137">สหรัฐอเมริกาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="cdb19-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="cdb19-138">สหรัฐอเมริกาตะวันตก</span><span class="sxs-lookup"><span data-stu-id="cdb19-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="cdb19-139">EU เหนือ</span><span class="sxs-lookup"><span data-stu-id="cdb19-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="cdb19-140">EU ตะวันตก</span><span class="sxs-lookup"><span data-stu-id="cdb19-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="cdb19-141">ตรวจสอบว่ามีการตั้งค่าฟิลด์ **รหัสแอปพลิเคชัน** เป็น **0cdb527f-a8d1-4bf8-9436-b352c68682b2**</span><span class="sxs-lookup"><span data-stu-id="cdb19-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="cdb19-142">ค่านี้เป็นค่าคงที่</span><span class="sxs-lookup"><span data-stu-id="cdb19-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="cdb19-143">ในฟิลด์ **รหัสสภาพแวดล้อม LCS** ป้อนรหัสของบัญชีการบอกรับเป็นสมาชิก LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cdb19-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="cdb19-144">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cdb19-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="cdb19-145">สร้างข้อมูลลับของ Key Vault</span><span class="sxs-lookup"><span data-stu-id="cdb19-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="cdb19-146">ลงชื่อเข้าใช้บัญชี RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cdb19-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="cdb19-147">ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** ในส่วน **สภาพแวดล้อม** ให้เลือกไทล์ **โปรแกรมเสริมของใบแจ้งหนี้อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="cdb19-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="cdb19-148">บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **สภาพแวดล้อมบริการ** และจากนั้น เลือก **พารามิเตอร์ Key Vault**</span><span class="sxs-lookup"><span data-stu-id="cdb19-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="cdb19-149">เลือก **สร้าง** เพื่อสร้างข้อมูลลับของ Key Vault</span><span class="sxs-lookup"><span data-stu-id="cdb19-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="cdb19-150">ในฟิลด์ **ชื่อ** ป้อนชื่อสำหรับข้อมูลลับของ Key Vault</span><span class="sxs-lookup"><span data-stu-id="cdb19-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="cdb19-151">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="cdb19-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="cdb19-152">ในฟิลด์ **URI ของ Key URI** ให้วางข้อมูลลับจาก Azure Key Suite</span><span class="sxs-lookup"><span data-stu-id="cdb19-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="cdb19-153">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cdb19-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="cdb19-154">สร้างข้อมูลลับของบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="cdb19-154">Create Storage account secret</span></span>

1. <span data-ttu-id="cdb19-155">ไปที่ **การจัดการระบบ** > **การตั้งค่า** > **คีย์พารามิเตอร์** และเลือกความลับของคีย์ความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="cdb19-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="cdb19-156">ในส่วน **ใบรับรอง** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="cdb19-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="cdb19-157">ในเขตข้อมูล **ชื่อ** ให้ป้อนชื่อของความลับของบัญชีการจัดเก็บและในเขตข้อมูล **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="cdb19-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="cdb19-158">ในฟิลด์ **ชนิด** เลือก **ใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="cdb19-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="cdb19-159">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cdb19-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="cdb19-160">สร้างความลับของใบรับรองดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="cdb19-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="cdb19-161">ไปที่ **การจัดการระบบ** > **การตั้งค่า** > **คีย์พารามิเตอร์** และเลือกความลับของคีย์ความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="cdb19-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="cdb19-162">ในส่วน **ใบรับรอง** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="cdb19-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="cdb19-163">ในเขตข้อมูล **ชื่อ** ให้ป้อนชื่อของใบรับรองดิจิทัลและในเขตข้อมูล **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="cdb19-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="cdb19-164">ในฟิลด์ **ชนิด** เลือก **ใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="cdb19-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="cdb19-165">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cdb19-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="cdb19-166">สร้างสภาพแวดล้อม add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cdb19-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="cdb19-167">ลงชื่อเข้าใช้บัญชี RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cdb19-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="cdb19-168">ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** ในส่วน **สภาพแวดล้อม** ให้เลือกไทล์ **โปรแกรมเสริมของใบแจ้งหนี้อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="cdb19-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="cdb19-169">สร้างสภาพแวดล้อมบริการ</span><span class="sxs-lookup"><span data-stu-id="cdb19-169">Create a service environment</span></span>

1. <span data-ttu-id="cdb19-170">บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **สภาพแวดล้อมบริการ**</span><span class="sxs-lookup"><span data-stu-id="cdb19-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="cdb19-171">เลือก **สร้าง** เพื่อสร้างสภาพแวดล้อมบริการใหม่</span><span class="sxs-lookup"><span data-stu-id="cdb19-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="cdb19-172">ในฟิลด์ **ชื่อ** ป้อนชื่อของสภาพแวดล้อมการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cdb19-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="cdb19-173">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="cdb19-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="cdb19-174">ในเขตข้อมูล **ข้อมูลลับของที่จัดเก็บโทเค็น SAS** ให้เลือกชื่อของความลับของบัญชีจัดเก็บที่ต้องใช้เพื่อตรวจสอบสิทธิ์ในการเข้าถึงบัญชีที่เก็บข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cdb19-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="cdb19-175">ในส่วน **ผู้ใช้** ให้เลือก **เพิ่ม** เพื่อเพิ่มผู้ใช้ที่ได้รับอนุญาตให้ส่งใบแจ้งหนี้อิเล็กทรอนิกส์ผ่านสภาพแวดล้อม และเชื่อมต่อกับบัญชีการจัดเก็บด้วย</span><span class="sxs-lookup"><span data-stu-id="cdb19-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="cdb19-176">ในฟิลด์ **รหัสผู้ใช้** ให้ป้อนนามแฝงของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="cdb19-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="cdb19-177">ในฟิลด์ **อีเมล** ป้อนอยู่อีเมลของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="cdb19-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="cdb19-178">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cdb19-178">Select **Save**.</span></span>
8. <span data-ttu-id="cdb19-179">ถ้าใบแจ้งหนี้เฉพาะประเทศ/ภูมิภาคของคุณ จำเป็นต้องมีกลุ่มของใบรับรองเพื่อใช้ลายเซ็นดิจิทัล บนบานหน้าต่างการดำเนินการ เลือก **พารามิเตอร์ Key Vault** แล้วเลือก **กลุ่มของใบรับรอง** และทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="cdb19-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="cdb19-180">เลือก **สร้าง** เพื่อสร้างกลุ่มของใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="cdb19-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="cdb19-181">ในฟิลด์ **ชื่อ** ป้อนชื่อของกลุ่มของใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="cdb19-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="cdb19-182">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="cdb19-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="cdb19-183">ในส่วน **ใบรับรอง** ให้เลือก **เพิ่ม** เพื่อเพิ่มใบรับรองให้กับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="cdb19-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="cdb19-184">ใช้ปุ่ม **ขึ้น** หรือ **ลง** เพื่อเปลี่ยนตําแหน่งของใบรับรองในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="cdb19-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="cdb19-185">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cdb19-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="cdb19-186">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cdb19-186">Close the page.</span></span>
9. <span data-ttu-id="cdb19-187">บนหน้า **สภาพแวดล้อมบริการ** บนบานหน้าต่างการดำเนินการ ให้เลือก **เผยแพร่** เพื่อเผยแพร่สภาพแวดล้อมไปยังระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="cdb19-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="cdb19-188">ค่าของฟิลด์ **สถานะ** ถูกเปลี่ยนเป็น **เผยแพร่แล้ว**</span><span class="sxs-lookup"><span data-stu-id="cdb19-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="cdb19-189">สร้างแอปพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="cdb19-189">Create a connected application</span></span>

1. <span data-ttu-id="cdb19-190">บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **แอปพลิเคชันที่เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="cdb19-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="cdb19-191">เลือก **สร้าง** เพื่อสร้างแอปพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="cdb19-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="cdb19-192">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อของแอปพลิเคชันที่จะเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="cdb19-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="cdb19-193">ในฟิลด์ **แอปพลิเคชัน** ให้ป้อน URL ของสภาพแวดล้อม Finance และ Supply Chain Management ที่จะเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="cdb19-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="cdb19-194">ในฟิลด์ **ผู้เช่า** ให้ป้อนผู้เช่าของสภาพแวดล้อม Finance และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cdb19-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="cdb19-195">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cdb19-195">Select **Save**.</span></span>
6. <span data-ttu-id="cdb19-196">ในบานหน้าต่างการดำเนินการ ให้เลือก **ตรวจสอบการเชื่อมต่อ** เพื่อทดสอบการเชื่อมต่อกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="cdb19-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="cdb19-197">จากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cdb19-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="cdb19-198">เชื่อมโยงแอปพลิเคชันที่เชื่อมต่อกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="cdb19-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="cdb19-199">บนหน้า **การตั้งค่าสภาพแวดล้อม** ให้เลือก **สร้าง** เพื่อกําหนดแอปพลิเคชันที่เชื่อมต่อให้กับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="cdb19-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="cdb19-200">ในฟิลด์ **แอปพลิเคชันที่เชื่อมต่อ** ให้เลือกแอปพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="cdb19-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="cdb19-201">ในฟิลด์ **สภาพแวดล้อมบริการ** เลือกสภาพแวดล้อมบริการ</span><span class="sxs-lookup"><span data-stu-id="cdb19-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="cdb19-202">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cdb19-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="cdb19-203">ตั้งค่าการรวม add-on ของการออกใบแจ้งหนี้อิเล็กทรอนิกส์ใน Finance และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cdb19-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="cdb19-204">เปิดคุณลักษณะการรวมของ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cdb19-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="cdb19-205">ลงชื่อเข้าใช้อินสแตนซ์ Finance หรือ Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cdb19-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="cdb19-206">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้ค้นหาคุณลักษณะ **การรวม add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="cdb19-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="cdb19-207">ถ้าคุณลักษณะนี้ไม่ปรากฏบนหน้า ให้เลือก **ตรวจสอบการอัปเดต**</span><span class="sxs-lookup"><span data-stu-id="cdb19-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="cdb19-208">เลือกคุณลักษณะ และจากนั้นเลือก **เปิดใช้งานตอนนี้**</span><span class="sxs-lookup"><span data-stu-id="cdb19-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="cdb19-209">ตั้งค่า URL ปลายทางการบริการ</span><span class="sxs-lookup"><span data-stu-id="cdb19-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="cdb19-210">ไปที่ **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="cdb19-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="cdb19-211">บนแท็บ **บริการการส่ง** ในฟิลด์ **URL ปลายทางของบริการ** ให้ป้อนปลายทางของบริการที่เหมาะสมสำหรับภูมิศาสตร์ Azure ของคุณ ดังแสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cdb19-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="cdb19-212">ภูมิศาสตร์ของ Datacenter Azure</span><span class="sxs-lookup"><span data-stu-id="cdb19-212">Datacenter Azure geography</span></span> | <span data-ttu-id="cdb19-213">URL ปลายทางของบริการ</span><span class="sxs-lookup"><span data-stu-id="cdb19-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="cdb19-214">สหรัฐอเมริกาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="cdb19-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="cdb19-215">สหรัฐอเมริกาตะวันตก</span><span class="sxs-lookup"><span data-stu-id="cdb19-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="cdb19-216">EU เหนือ</span><span class="sxs-lookup"><span data-stu-id="cdb19-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="cdb19-217">EU ตะวันตก</span><span class="sxs-lookup"><span data-stu-id="cdb19-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="cdb19-218">ในฟิลด์ **สภาพแวดล้อม** ป้อนชื่อของสภาพแวดล้อม add-on ของการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cdb19-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="cdb19-219">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cdb19-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
