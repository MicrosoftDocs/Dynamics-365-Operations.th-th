---
title: เริ่มต้นใช้งานการจัดการบริการการออกใบแจ้งหนี้อิเล็กทรอนิกส์
description: หัวข้อนี้จะอธิบายวิธีการเริ่มต้นใช้งานการออกใบแจ้งหนี้อิเล็กทรอนิกส์
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840159"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="c40c3-103">เริ่มต้นใช้งานการจัดการบริการการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c40c3-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="c40c3-104">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="c40c3-104">Prerequisites</span></span>

<span data-ttu-id="c40c3-105">ก่อนที่คุณจะดำเนินการกระบวนงานต่างๆ ในหัวข้อนี้ให้เสร็จสมบูรณ์ ต้องมีข้อกำหนดเบื้องต้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c40c3-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="c40c3-106">คุณต้องมีสิทธิ์เข้าถึงบัญชี Microsoft Dynamics Lifecycle Services (LCS) ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c40c3-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="c40c3-107">คุณต้องมีโครงการ LCS ที่มีรุ่น 10.0.17 หรือใหม่กว่าของ Microsoft Dynamics 365 Finance และ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c40c3-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c40c3-108">นอกจากนี้ แอปเหล่านี้ต้องถูกปรับใช้ในหนึ่งในภูมิศาสตร์ Azure ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c40c3-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="c40c3-109">สหรัฐอเมริกาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="c40c3-109">East US</span></span>
    - <span data-ttu-id="c40c3-110">สหรัฐอเมริกาตะวันตก</span><span class="sxs-lookup"><span data-stu-id="c40c3-110">West US</span></span>
    - <span data-ttu-id="c40c3-111">EU เหนือ</span><span class="sxs-lookup"><span data-stu-id="c40c3-111">North EU</span></span>
    - <span data-ttu-id="c40c3-112">EU ตะวันตก</span><span class="sxs-lookup"><span data-stu-id="c40c3-112">West EU</span></span>

- <span data-ttu-id="c40c3-113">คุณต้องมีสิทธิ์เข้าถึงบัญชี Dynamics 365 Regulatory Configuration Services (RCS) ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c40c3-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="c40c3-114">คุณต้องเปิดใช้งานคุณลักษณะที่ใช้ทั่วโลกสำหรับบัญชี RCS ของคุณในการจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="c40c3-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="c40c3-115">สำหรับข้อมูลเพิ่มเติม ดู [Regulatory Configuration Services (RCS) - คุณลักษณะที่ใช้ทั่วโลก](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="c40c3-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="c40c3-116">คุณต้องสร้าง Key Vault และบัญชีการจัดเก็บใน Azure</span><span class="sxs-lookup"><span data-stu-id="c40c3-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="c40c3-117">สำหรับข้อมูลเพิ่มเติม ดู [สร้างบัญชีการจัดเก็บของ Azure และ Key Vault](e-invoicing-create-azure-storage-account-key-vault.md)</span><span class="sxs-lookup"><span data-stu-id="c40c3-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="c40c3-118">ติดตั้ง add-in สำหรับไมโครเซอร์วิสใน Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="c40c3-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="c40c3-119">ลงชื่อเข้าใช้บัญชี LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c40c3-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="c40c3-120">เลือกไทล์ **การจัดการคุณลักษณะพรีวิว**</span><span class="sxs-lookup"><span data-stu-id="c40c3-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="c40c3-121">ในส่วน **คุณลักษณะพรีวิวสำหรับสาธารณะ** ให้เลือก **บริการออกใบแจ้งหนี้อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="c40c3-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="c40c3-122">ตรวจสอบให้แน่ใจว่าตัวเลือก **เปิดใช้งานคุณลักษณะพรีวิวแล้ว** ได้ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="c40c3-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="c40c3-123">บนกระดานข้อมูล LCS ของคุณ ให้เลือกโครงการปรับใช้ LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c40c3-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="c40c3-124">โครงการ LCS ต้องทำงานอยู่</span><span class="sxs-lookup"><span data-stu-id="c40c3-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="c40c3-125">บนแท็บ **add-in ของสภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c40c3-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="c40c3-126">เลือก **บริการออกใบแจ้งหนี้อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="c40c3-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="c40c3-127">ในฟิลด์ **รหัสแอปพลิเคชัน AAD** ให้ป้อน **091c98b0-a1c9-4b02-b62c-7753395ccabe**</span><span class="sxs-lookup"><span data-stu-id="c40c3-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="c40c3-128">ค่านี้เป็นค่าคงที่</span><span class="sxs-lookup"><span data-stu-id="c40c3-128">This is a fixed value.</span></span>
10. <span data-ttu-id="c40c3-129">ในเขตข้อมูล **รหัสผู้เช่า AAD** ป้อนรหัสผู้เช่าของบัญชีสมัครสมาชิก Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c40c3-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="c40c3-130">ตรวจสอบข้อกำหนดและเงื่อนไข จากนั้นเลือกกล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="c40c3-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="c40c3-131">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="c40c3-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="c40c3-132">ตั้งค่าพารามิเตอร์สำหรับการรวม RCS กับการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c40c3-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="c40c3-133">ลงชื่อเข้าใช้บัญชี RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c40c3-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="c40c3-134">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ในส่วน **ลิงค์ที่เกี่ยวข้อง** ให้เลือก **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="c40c3-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="c40c3-135">บนแท็บ **บริการการออกใบแจ้งหนี้อิเล็กทรอนิกส์** ในฟิลด์ **URI ปลายทางของบริการ** ให้ป้อนปลายทางของบริการที่เหมาะสมสำหรับภูมิศาสตร์ Azure ของคุณ ดังแสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c40c3-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="c40c3-136">ภูมิศาสตร์ของ Datacenter Azure</span><span class="sxs-lookup"><span data-stu-id="c40c3-136">Datacenter Azure geography</span></span> | <span data-ttu-id="c40c3-137">URI ปลายทางของบริการ</span><span class="sxs-lookup"><span data-stu-id="c40c3-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="c40c3-138">สหรัฐอเมริกาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="c40c3-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="c40c3-139">สหรัฐอเมริกาตะวันตก</span><span class="sxs-lookup"><span data-stu-id="c40c3-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="c40c3-140">EU เหนือ</span><span class="sxs-lookup"><span data-stu-id="c40c3-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="c40c3-141">EU ตะวันตก</span><span class="sxs-lookup"><span data-stu-id="c40c3-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="c40c3-142">ตรวจสอบว่ามีการตั้งค่าฟิลด์ **รหัสแอปพลิเคชัน** เป็น **0cdb527f-a8d1-4bf8-9436-b352c68682b2**</span><span class="sxs-lookup"><span data-stu-id="c40c3-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="c40c3-143">ค่านี้เป็นค่าคงที่</span><span class="sxs-lookup"><span data-stu-id="c40c3-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="c40c3-144">ในฟิลด์ **รหัสสภาพแวดล้อม LCS** ป้อนรหัสของสภาพแวดล้อม LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c40c3-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="c40c3-145">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c40c3-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="c40c3-146">สร้างการอ้างอิง Key Vault</span><span class="sxs-lookup"><span data-stu-id="c40c3-146">Create Key Vault references</span></span>

1. <span data-ttu-id="c40c3-147">ลงชื่อเข้าใช้บัญชี RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c40c3-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="c40c3-148">ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** ในส่วน **สภาพแวดล้อม** ให้เลือกไทล์ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="c40c3-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="c40c3-149">บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **สภาพแวดล้อมบริการ** และจากนั้น เลือก **พารามิเตอร์ Key Vault**</span><span class="sxs-lookup"><span data-stu-id="c40c3-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="c40c3-150">เลือก **สร้าง** เพื่อสร้างการอ้างอิง Key Vault</span><span class="sxs-lookup"><span data-stu-id="c40c3-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="c40c3-151">ในฟิลด์ **ชื่อ** ป้อนชื่อสำหรับการอ้างอิง Key Vault</span><span class="sxs-lookup"><span data-stu-id="c40c3-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="c40c3-152">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c40c3-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="c40c3-153">ในฟิลด์ **URI ของ Key URI** ให้วางข้อมูลลับของ Key Vault จาก Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="c40c3-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="c40c3-154">สำหรับข้อมูลเพิ่มเติม ดู [สร้างบัญชีการจัดเก็บของ Azure และ Key Vault](e-invoicing-create-azure-storage-account-key-vault.md)</span><span class="sxs-lookup"><span data-stu-id="c40c3-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="c40c3-155">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c40c3-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="c40c3-156">สร้างข้อมูลลับของบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="c40c3-156">Create Storage account secret</span></span>

1. <span data-ttu-id="c40c3-157">บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **สภาพแวดล้อมบริการ** > **พารามิเตอร์ Key Vault**</span><span class="sxs-lookup"><span data-stu-id="c40c3-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="c40c3-158">เลือก **การอ้างอิง Key Vault** และในส่วน **ใบรับรอง** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="c40c3-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="c40c3-159">ในฟิลด์ **ชื่อ** ป้อนชื่อข้อมูลลับของบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="c40c3-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="c40c3-160">สำหรับข้อมูลเพิ่มเติม ดู [สร้างบัญชีการจัดเก็บของ Azure และ Key Vault](e-invoicing-create-azure-storage-account-key-vault.md)</span><span class="sxs-lookup"><span data-stu-id="c40c3-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="c40c3-161">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c40c3-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c40c3-162">ในฟิลด์ **ชนิด** เลือก **ข้อมูลลับ**</span><span class="sxs-lookup"><span data-stu-id="c40c3-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="c40c3-163">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c40c3-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="c40c3-164">สร้างความลับของใบรับรองดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="c40c3-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="c40c3-165">บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **สภาพแวดล้อมบริการ** และจากนั้น เลือก **พารามิเตอร์ Key Vault**</span><span class="sxs-lookup"><span data-stu-id="c40c3-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="c40c3-166">เลือก **การอ้างอิง Key Vault** และจากนั้น ในส่วน **ใบรับรอง** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="c40c3-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="c40c3-167">ในฟิลด์ **ชื่อ** ป้อนชื่อข้อมูลลับของใบรับรองดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="c40c3-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="c40c3-168">สำหรับข้อมูลเพิ่มเติม ดู [สร้างบัญชีการจัดเก็บของ Azure และ Key Vault](e-invoicing-create-azure-storage-account-key-vault.md)</span><span class="sxs-lookup"><span data-stu-id="c40c3-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="c40c3-169">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c40c3-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c40c3-170">ในฟิลด์ **ชนิด** เลือก **ใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="c40c3-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="c40c3-171">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c40c3-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="c40c3-172">สร้างสภาพแวดล้อมบริการ</span><span class="sxs-lookup"><span data-stu-id="c40c3-172">Create a service environment</span></span>

1. <span data-ttu-id="c40c3-173">ลงชื่อเข้าใช้บัญชี RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c40c3-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="c40c3-174">ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** ในส่วน **สภาพแวดล้อม** ให้เลือกไทล์ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="c40c3-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="c40c3-175">บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **สภาพแวดล้อมบริการ**</span><span class="sxs-lookup"><span data-stu-id="c40c3-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="c40c3-176">เลือก **สร้าง** เพื่อสร้างสภาพแวดล้อมบริการใหม่</span><span class="sxs-lookup"><span data-stu-id="c40c3-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="c40c3-177">ในฟิลด์ **ชื่อ** ป้อนชื่อของสภาพแวดล้อมการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c40c3-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="c40c3-178">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c40c3-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="c40c3-179">ในเขตข้อมูล **ข้อมูลลับของที่จัดเก็บโทเค็น SAS** ให้เลือกชื่อของความลับของบัญชีจัดเก็บที่ต้องใช้เพื่อตรวจสอบสิทธิ์ในการเข้าถึงบัญชีที่เก็บข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c40c3-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="c40c3-180">ในส่วน **ผู้ใช้** ให้เลือก **เพิ่ม** เพื่อเพิ่มผู้ใช้ที่ได้รับอนุญาตให้ส่งใบแจ้งหนี้อิเล็กทรอนิกส์ผ่านสภาพแวดล้อม และเชื่อมต่อกับบัญชีการจัดเก็บด้วย</span><span class="sxs-lookup"><span data-stu-id="c40c3-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="c40c3-181">ในฟิลด์ **รหัสผู้ใช้** ให้ป้อนนามแฝงของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c40c3-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="c40c3-182">ในฟิลด์ **อีเมล** ป้อนอยู่อีเมลของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c40c3-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="c40c3-183">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c40c3-183">Select **Save**.</span></span>
10. <span data-ttu-id="c40c3-184">ถ้าใบแจ้งหนี้เฉพาะประเทศ/ภูมิภาคของคุณ จำเป็นต้องมีกลุ่มของใบรับรองเพื่อใช้ลายเซ็นดิจิทัล บนบานหน้าต่างการดำเนินการ เลือก **พารามิเตอร์ Key Vault** แล้วเลือก **กลุ่มของใบรับรอง** และทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="c40c3-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="c40c3-185">เลือก **สร้าง** เพื่อสร้างกลุ่มของใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="c40c3-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="c40c3-186">ในฟิลด์ **ชื่อ** ป้อนชื่อของกลุ่มของใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="c40c3-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="c40c3-187">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c40c3-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="c40c3-188">ในส่วน **ใบรับรอง** ให้เลือก **เพิ่ม** เพื่อเพิ่มใบรับรองให้กับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="c40c3-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="c40c3-189">ใช้ปุ่ม **ขึ้น** หรือ **ลง** เพื่อเปลี่ยนตําแหน่งของใบรับรองในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="c40c3-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="c40c3-190">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c40c3-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="c40c3-191">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c40c3-191">Close the page.</span></span>
11. <span data-ttu-id="c40c3-192">บนหน้า **สภาพแวดล้อมบริการ** บนบานหน้าต่างการดำเนินการ ให้เลือก **เผยแพร่** เพื่อเผยแพร่สภาพแวดล้อมไปยังระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="c40c3-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="c40c3-193">ค่าของฟิลด์ **สถานะ** ถูกเปลี่ยนเป็น **เผยแพร่แล้ว**</span><span class="sxs-lookup"><span data-stu-id="c40c3-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="c40c3-194">สร้างแอปพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="c40c3-194">Create a connected application</span></span>

1. <span data-ttu-id="c40c3-195">บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **แอปพลิเคชันที่เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="c40c3-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="c40c3-196">เลือก **สร้าง** เพื่อสร้างแอปพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="c40c3-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="c40c3-197">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อของแอปพลิเคชันที่จะเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="c40c3-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="c40c3-198">ในฟิลด์ **แอปพลิเคชัน** ให้ป้อน URL ของสภาพแวดล้อม Finance และ Supply Chain Management ที่จะเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="c40c3-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="c40c3-199">ในฟิลด์ **ผู้เช่า** ให้ป้อนผู้เช่าของสภาพแวดล้อม Finance และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c40c3-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="c40c3-200">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c40c3-200">Select **Save**.</span></span>
6. <span data-ttu-id="c40c3-201">ในบานหน้าต่างการดำเนินการ ให้เลือก **ตรวจสอบการเชื่อมต่อ** เพื่อทดสอบการเชื่อมต่อกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="c40c3-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="c40c3-202">จากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c40c3-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="c40c3-203">เชื่อมโยงแอปพลิเคชันที่เชื่อมต่อกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="c40c3-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="c40c3-204">บนหน้า **การตั้งค่าสภาพแวดล้อม** ให้เลือก **สร้าง** เพื่อกําหนดแอปพลิเคชันที่เชื่อมต่อให้กับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="c40c3-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="c40c3-205">ในฟิลด์ **แอปพลิเคชันที่เชื่อมต่อ** ให้เลือกแอปพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="c40c3-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="c40c3-206">ในฟิลด์ **สภาพแวดล้อมบริการ** เลือกสภาพแวดล้อมบริการ</span><span class="sxs-lookup"><span data-stu-id="c40c3-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="c40c3-207">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c40c3-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="c40c3-208">ตั้งค่าการรวมการออกใบแจ้งหนี้อิเล็กทรอนิกส์ใน Finance และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c40c3-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="c40c3-209">เปิดคุณลักษณะการรวมของการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c40c3-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="c40c3-210">ลงชื่อเข้าใช้อินสแตนซ์ Finance หรือ Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c40c3-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="c40c3-211">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้ค้นหาคุณลักษณะ **การรวมการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="c40c3-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="c40c3-212">ถ้าคุณลักษณะนี้ไม่ปรากฏบนหน้า ให้เลือก **ตรวจสอบการอัปเดต**</span><span class="sxs-lookup"><span data-stu-id="c40c3-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="c40c3-213">เลือกคุณลักษณะ และจากนั้นเลือก **เปิดใช้งานตอนนี้**</span><span class="sxs-lookup"><span data-stu-id="c40c3-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="c40c3-214">ตั้งค่า URL ปลายทางการบริการ</span><span class="sxs-lookup"><span data-stu-id="c40c3-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="c40c3-215">ไปที่ **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="c40c3-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="c40c3-216">บนแท็บ **บริการการส่ง** ในฟิลด์ **URL ปลายทางของบริการ** ให้ป้อนปลายทางของบริการที่เหมาะสมสำหรับภูมิศาสตร์ Azure ของคุณ ดังแสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c40c3-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="c40c3-217">ภูมิศาสตร์ของ Datacenter Azure</span><span class="sxs-lookup"><span data-stu-id="c40c3-217">Datacenter Azure geography</span></span> | <span data-ttu-id="c40c3-218">URL ปลายทางของบริการ</span><span class="sxs-lookup"><span data-stu-id="c40c3-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="c40c3-219">สหรัฐอเมริกาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="c40c3-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="c40c3-220">สหรัฐอเมริกาตะวันตก</span><span class="sxs-lookup"><span data-stu-id="c40c3-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="c40c3-221">EU เหนือ</span><span class="sxs-lookup"><span data-stu-id="c40c3-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="c40c3-222">EU ตะวันตก</span><span class="sxs-lookup"><span data-stu-id="c40c3-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="c40c3-223">ในฟิลด์ **สภาพแวดล้อม** ป้อนชื่อของสภาพแวดล้อมบริการที่เผยแพร่ในการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c40c3-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="c40c3-224">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c40c3-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="c40c3-225">เปิดใช้งานคีย์การสลับ</span><span class="sxs-lookup"><span data-stu-id="c40c3-225">Enable Flighting keys</span></span>

<span data-ttu-id="c40c3-226">เปิดใช้งานคีย์การสลับสำหรับ Microsoft Dynamics 365 Finance หรือ Microsoft Dynamics 365 Supply Chain Management รุ่น 10.0.17 หรือรุ่นก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="c40c3-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="c40c3-227">ดำเนินการคำสั่ง SQL ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c40c3-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="c40c3-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="c40c3-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="c40c3-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="c40c3-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="c40c3-230">ปฏิบัติการตามคำสั่ง IISreset สำหรับของ AOS ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c40c3-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
