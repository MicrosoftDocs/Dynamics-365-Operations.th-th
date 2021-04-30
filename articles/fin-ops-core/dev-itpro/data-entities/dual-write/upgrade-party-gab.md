---
title: อัปเกรดเป็นรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล
description: หัวข้อนี้จะอธิบายวิธีการอัปเกรดข้อมูลแบบสองทิศทางให้กับรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 76e64d483e833782733277a64d8dc37cbeba6130
ms.sourcegitcommit: 011468a6cffea8641bebc2922e0676d9f44b36fc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857381"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="2c299-103">อัปเกรดเป็นรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล</span><span class="sxs-lookup"><span data-stu-id="2c299-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2c299-104">[แม่แบบ Azure Data Factory](https://aka.ms/dual-write-gab-adf) ช่วยคุณในการอัปเกรดข้อมูลตาราง **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** แบบสองทิศทางให้กับไปยังรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล</span><span class="sxs-lookup"><span data-stu-id="2c299-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="2c299-105">แม่แบบจะกระทบยอดข้อมูลจากทั้งแอป Finance and Operations และแอปการมีส่วนร่วมกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2c299-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="2c299-106">เมื่อสิ้นสุดกระบวนการ ฟิลด์ **ฝ่าย** และ **ผู้ติดต่อ** ของเรกคอร์ด **ฝ่าย** จะมีการสร้างและเชื่อมโยงกับเรกคอร์ด **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ในแอปการมีส่วนร่วมกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2c299-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="2c299-107">ไฟล์ .csv (`FONewParty.csv`) ถูกสร้างขึ้นเพื่อสร้างเรกคอร์ด **ฝ่าย** ใหม่ภายในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2c299-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="2c299-108">หัวข้อนี้จะให้คําแนะนําในการใช้แม่แบบ Data Factory และอัปเกรดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="2c299-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="2c299-109">ถ้าคุณไม่มีการกำหนดใด ๆ คุณสามารถใช้แม่แบบตามที่เป็นได้</span><span class="sxs-lookup"><span data-stu-id="2c299-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="2c299-110">ถ้าคุณมีการกำหนดสำหรับ **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** จากนั้นคุณต้องปรับเปลี่ยนแม่แบบโดยใช้คําแนะนําต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2c299-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="2c299-111">แม่แบบจะช่วยคุณอัปเกรดเฉพาะข้อมูล **ฝ่าย**</span><span class="sxs-lookup"><span data-stu-id="2c299-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="2c299-112">ในการนำออกใช้ในอนาคต ที่อยู่ไปรษณีย์และที่อยู่อิเล็กทรอนิกส์จะถูกรวมไว้ด้วย</span><span class="sxs-lookup"><span data-stu-id="2c299-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2c299-113">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="2c299-113">Prerequisites</span></span>

<span data-ttu-id="2c299-114">ข้อกำหนดเบื้องต้นเหล่านี้จำเป็น:</span><span class="sxs-lookup"><span data-stu-id="2c299-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="2c299-115">การบอกรับเป็นสมาชิก Azure</span><span class="sxs-lookup"><span data-stu-id="2c299-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="2c299-116">เข้าถึงแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="2c299-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="2c299-117">คุณเป็นลูกค้าการรวมแบบสองทิศทางที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="2c299-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="2c299-118">จัดเตรียมสำหรับการอัปเกรด</span><span class="sxs-lookup"><span data-stu-id="2c299-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="2c299-119">**ซิงค์อย่างครบถ้วน**: ทั้งสองสภาพแวดล้อมอยู่ในสถานะถูกซิงค์อย่างครบถ้วนแล้วสำหรับ **บัญชี (ลูกค้า)** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="2c299-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="2c299-120">**คีย์การรวม**: ตาราง **บัญชี (ลูกค้า)** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ในแอปการมีส่วนร่วมกับลูกค้าใช้คีย์การรวมที่จัดส่งแบบสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="2c299-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="2c299-121">ถ้าคุณเลือกกำหนดคีย์การรวมเอง คุณต้องเลือกกำหนดแม่แบบเอง</span><span class="sxs-lookup"><span data-stu-id="2c299-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="2c299-122">**หมายเลขฝ่าย**: เรกคอร์ด **บัญชี (ลูกค้า)** ทั้งหมด **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ที่จะอัปเกรดมีหมายเลข **ฝ่าย**</span><span class="sxs-lookup"><span data-stu-id="2c299-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="2c299-123">เรกคอร์ดที่ไม่มีหมายเลข **ฝ่าย** จะถูกละเว้น</span><span class="sxs-lookup"><span data-stu-id="2c299-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="2c299-124">ถ้าคุณต้องการอัปเกรดเรกคอร์ดเหล่านั้น ให้เพิ่มหมายเลข **ฝ่าย** ก่อนที่คุณจะเริ่มกระบวนการอัปเกรด</span><span class="sxs-lookup"><span data-stu-id="2c299-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="2c299-125">**ความขัดข้องของระบบ**: ในระหว่างกระบวนการอัปเกรด คุณจะต้องใช้ทั้งสภาพแวดล้อม Finance and Operations และการมีส่วนร่วมกับลูกค้าออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="2c299-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="2c299-126">**สแนปช็อต**: ถ่ายภาพสแนปช็อตของทั้งแอป Finance and Operations และแอปการมีส่วนร่วมกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2c299-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="2c299-127">ใช้สแนปช็อตเพื่อคืนสถานะก่อนหน้านี้ถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="2c299-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="2c299-128">การจัดวาง</span><span class="sxs-lookup"><span data-stu-id="2c299-128">Deployment</span></span>

1. <span data-ttu-id="2c299-129">ดาวน์โหลดแม่แบบจาก [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf)</span><span class="sxs-lookup"><span data-stu-id="2c299-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="2c299-130">ลงชื่อเข้าใช้ [Microsoft Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="2c299-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="2c299-131">สร้าง [กลุ่มทรัพยากร](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal)</span><span class="sxs-lookup"><span data-stu-id="2c299-131">Create a [resource group](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="2c299-132">สร้าง [บัญชีการจัดเก็บ](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) ในกลุ่มทรัพยากรที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="2c299-132">Create a [storage account](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="2c299-133">สร้าง [Data Factory](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) เหนือกลุ่มทรัพยากรที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="2c299-133">Create a [data factory](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="2c299-134">เปิด Data Factory และเลือกไทล์ **สร้าง & ตรวจสอบ**</span><span class="sxs-lookup"><span data-stu-id="2c299-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="2c299-135">บนแท็บ **จัดการ** ให้เลือก **แม่แบบ ARM**</span><span class="sxs-lookup"><span data-stu-id="2c299-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="2c299-136">เลือกแม่แบบ **นำเข้าแม่แบบ ARM** เพื่อนําเข้าแม่แบบ **ฝ่าย**</span><span class="sxs-lookup"><span data-stu-id="2c299-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="2c299-137">นําเข้าแม่แบบไปยัง Data Factory</span><span class="sxs-lookup"><span data-stu-id="2c299-137">Import the template into the data factory.</span></span> <span data-ttu-id="2c299-138">ป้อนค่าต่อไปนี้ให้กับ **รายละเอียดโครงการ** และ **รายละเอียดอินสแตนซ์**</span><span class="sxs-lookup"><span data-stu-id="2c299-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="2c299-139">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="2c299-139">Field</span></span> | <span data-ttu-id="2c299-140">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="2c299-140">Value</span></span>
    ---|---
    <span data-ttu-id="2c299-141">การบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="2c299-141">Subscription</span></span> | <span data-ttu-id="2c299-142">การบอกรับเป็นสมาชิก Azure</span><span class="sxs-lookup"><span data-stu-id="2c299-142">Azure subscription</span></span>
    <span data-ttu-id="2c299-143">กลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="2c299-143">Resource group</span></span> | <span data-ttu-id="2c299-144">ระบุทรัพยากรเดียวกันกับที่มีการสร้างบัญชีการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="2c299-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="2c299-145">ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="2c299-145">Region</span></span> | <span data-ttu-id="2c299-146">ระบุภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="2c299-146">Specify region.</span></span>
    <span data-ttu-id="2c299-147">ชื่อโรงงาน</span><span class="sxs-lookup"><span data-stu-id="2c299-147">Factory Name</span></span> | <span data-ttu-id="2c299-148">ระบุชื่อโรงงาน</span><span class="sxs-lookup"><span data-stu-id="2c299-148">Specify factory name.</span></span>
    <span data-ttu-id="2c299-149">คีย์หลัก FO ที่เชื่อมโยง Service_service</span><span class="sxs-lookup"><span data-stu-id="2c299-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="2c299-150">ระบุคีย์ของโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="2c299-150">Specify the application's key.</span></span>
    <span data-ttu-id="2c299-151">ที่เก็บข้อมูล Azure Blob_สตริงการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="2c299-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="2c299-152">สตริงการเชื่อมต่อที่เก็บข้อมูล Azure Blob</span><span class="sxs-lookup"><span data-stu-id="2c299-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="2c299-153">Dynamics Crm ที่เชื่อมโยง Service_password</span><span class="sxs-lookup"><span data-stu-id="2c299-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="2c299-154">รหัสผ่านของบัญชีผู้ใช้ที่คุณระบุเป็นชื่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2c299-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="2c299-155">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="2c299-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="2c299-156">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="2c299-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="2c299-157">ระบุข้อมูลผู้เช่า (ชื่อโดเมนหรือรหัสผู้เช่า) ที่โปรแกรมประยุกต์ของคุณอยู่</span><span class="sxs-lookup"><span data-stu-id="2c299-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="2c299-158">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="2c299-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="2c299-159">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="2c299-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="2c299-160">ระบุรหัสไคลเอนต์ของโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="2c299-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="2c299-161">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="2c299-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="2c299-162">ชื่อผู้ใช้ที่จะเชื่อมต่อกับ Dynamics</span><span class="sxs-lookup"><span data-stu-id="2c299-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="2c299-163">หากต้องการข้อมูลเพิ่มเติม โปรดดูที่ [เลื่อนระดับแม่แบบ Resource Manager ด้วยตนเองในแต่ละสภาพแวดล้อม](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment) [คุณสมบัติบริการที่เชื่อมโยง](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties) และ [คัดลอกข้อมูลโดยใช้ Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="2c299-163">For more information, see [Manually promote a Resource Manager template for each environment](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="2c299-164">หลังจากใช้งานแล้ว ให้ตรวจสอบความถูกต้องของชุดข้อมูล ลำดับข้อมูล และบริการที่เชื่อมโยงของ Data Factory</span><span class="sxs-lookup"><span data-stu-id="2c299-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![ชุดข้อมูล ลำดับข้อมูล และบริการที่เชื่อมโยง](media/data-factory-validate.png)

11. <span data-ttu-id="2c299-166">นําทางไปยัง **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="2c299-166">Navigate to **Manage**.</span></span> <span data-ttu-id="2c299-167">ภายใต้ **การเชื่อมต่อ** ให้เลือก **บริการที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="2c299-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="2c299-168">เลือก **DynamicsCrmLinkedService**</span><span class="sxs-lookup"><span data-stu-id="2c299-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="2c299-169">ในฟอร์ม **แก้ไขบริการที่เชื่อมโยง (Dynamics CRM)** ให้ป้อนค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2c299-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="2c299-170">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="2c299-170">Field</span></span> | <span data-ttu-id="2c299-171">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="2c299-171">Value</span></span>
    ---|---
    <span data-ttu-id="2c299-172">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="2c299-172">Name</span></span> | <span data-ttu-id="2c299-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="2c299-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="2c299-174">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2c299-174">Description</span></span> | <span data-ttu-id="2c299-175">บริการที่เชื่อมโยงเพื่อเชื่อมต่อกับอินสแตนซ์ CRM เพื่อดึงข้อมูลเอนทิตีมาใช้</span><span class="sxs-lookup"><span data-stu-id="2c299-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="2c299-176">เชื่อมต่อผ่าน Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="2c299-176">Connect via integration runtime</span></span> | <span data-ttu-id="2c299-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2c299-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="2c299-178">ชนิดการปรับใช้</span><span class="sxs-lookup"><span data-stu-id="2c299-178">Deployment type</span></span> | <span data-ttu-id="2c299-179">ออนไลน์</span><span class="sxs-lookup"><span data-stu-id="2c299-179">Online</span></span>
    <span data-ttu-id="2c299-180">Uri ของการบริการ</span><span class="sxs-lookup"><span data-stu-id="2c299-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="2c299-181">ชนิดการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="2c299-181">Authentication type</span></span> | <span data-ttu-id="2c299-182">Office365</span><span class="sxs-lookup"><span data-stu-id="2c299-182">Office365</span></span>
    <span data-ttu-id="2c299-183">ชื่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2c299-183">User name</span></span> |
    <span data-ttu-id="2c299-184">รหัสผ่านหรือ Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="2c299-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="2c299-185">รหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="2c299-185">Password</span></span>
    <span data-ttu-id="2c299-186">รหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="2c299-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="2c299-187">เรียกใช้แม่แบบ</span><span class="sxs-lookup"><span data-stu-id="2c299-187">Run the template</span></span>

1. <span data-ttu-id="2c299-188">หยุดการรวมแบบสองทิศทาง **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ต่อไปนี้โดยใช้แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2c299-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="2c299-189">Customers V3 (บัญชี)</span><span class="sxs-lookup"><span data-stu-id="2c299-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="2c299-190">ลูกค้า V3(ผู้ติดต่อ)</span><span class="sxs-lookup"><span data-stu-id="2c299-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="2c299-191">ผู้ติดต่อของ CDS V2(ผู้ติดต่อ)</span><span class="sxs-lookup"><span data-stu-id="2c299-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="2c299-192">ผู้ติดต่อของ CDS V2(ผู้ติดต่อ)</span><span class="sxs-lookup"><span data-stu-id="2c299-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="2c299-193">ผู้จัดจำหน่าย V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="2c299-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="2c299-194">ตรวจสอบให้แน่ใจว่าแผนที่ถูกลบออกจากตาราง `msdy_dualwriteruntimeconfig` ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="2c299-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="2c299-195">ติดตั้ง [ฝ่ายการรวมแบบสองทิศทางและโซลูชันสมุดที่อยู่สากล](https://aka.ms/dual-write-gab) จาก AppSource</span><span class="sxs-lookup"><span data-stu-id="2c299-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="2c299-196">ในแอป Finance and Operations หากตารางต่อไปนี้มีข้อมูล ให้รัน **การซิงค์ครั้งแรก**</span><span class="sxs-lookup"><span data-stu-id="2c299-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="2c299-197">คำขึ้นต้น</span><span class="sxs-lookup"><span data-stu-id="2c299-197">Salutations</span></span>
    + <span data-ttu-id="2c299-198">ชนิดลักษณะส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="2c299-198">Personal character types</span></span>
    + <span data-ttu-id="2c299-199">คำลงท้าย</span><span class="sxs-lookup"><span data-stu-id="2c299-199">Complimentary closing</span></span>
    + <span data-ttu-id="2c299-200">ตำแหน่งของผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2c299-200">Contact person titles</span></span>
    + <span data-ttu-id="2c299-201">บทบาทในการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="2c299-201">Decision making roles</span></span>
    + <span data-ttu-id="2c299-202">ระดับของสมาชิก</span><span class="sxs-lookup"><span data-stu-id="2c299-202">Loyalty levels</span></span>

5. <span data-ttu-id="2c299-203">ในแอปการมีส่วนร่วมกับลูกค้า ให้ปิดใช้งานขั้นตอนปลั๊กอินต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2c299-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="2c299-204">การอัปเดตบัญชี</span><span class="sxs-lookup"><span data-stu-id="2c299-204">Account Update</span></span>
         + <span data-ttu-id="2c299-205">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromAccountEntity: อัปเดตบัญชี</span><span class="sxs-lookup"><span data-stu-id="2c299-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="2c299-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: อัปเดตบัญชี</span><span class="sxs-lookup"><span data-stu-id="2c299-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="2c299-207">การอัปเดตผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2c299-207">Contact Update</span></span>
         + <span data-ttu-id="2c299-208">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromContactEntity: อัปเดตผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2c299-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="2c299-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: อัปเดตผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2c299-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="2c299-210">อัปเดต msdyn_party</span><span class="sxs-lookup"><span data-stu-id="2c299-210">msdyn_party Update</span></span>
         + <span data-ttu-id="2c299-211">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromPartyEntity: การอัปเดต msdyn_party</span><span class="sxs-lookup"><span data-stu-id="2c299-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="2c299-212">การอัปเดต msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="2c299-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="2c299-213">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromVendorEntity: การอัปเดต msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="2c299-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="2c299-214">ในแอปการมีส่วนร่วมกับลูกค้า ให้ปิดใช้งานลำดับงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c299-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="2c299-215">สร้างผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="2c299-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="2c299-216">สร้างผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="2c299-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="2c299-217">สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2c299-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="2c299-218">สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2c299-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="2c299-219">อัปเดตผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="2c299-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="2c299-220">อัปเดตผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2c299-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="2c299-221">อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2c299-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="2c299-222">อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2c299-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="2c299-223">ใน Data Factory ให้รันแม่แบบโดยการเลือก **ทริกเกอร์ตอนนี้** ดังที่แสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2c299-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="2c299-224">กระบวนการนี้อาจใช้เวลาสักครู่เพื่อกรอกข้อมูลตามปริมาณข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2c299-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![การรันทริกเกอร์](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="2c299-226">ถ้าคุณมีการกำหนดสำหรับ **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** จากนั้นคุณต้องปรับเปลี่ยนแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="2c299-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="2c299-227">นําเข้าเรกคอร์ด **ฝ่าย** ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2c299-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="2c299-228">ดาวน์โหลดไฟล์ `FONewParty.csv` จากที่จัดเก็บ Azure blob</span><span class="sxs-lookup"><span data-stu-id="2c299-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="2c299-229">พาธคือ `partybootstrapping/output/FONewParty.csv`</span><span class="sxs-lookup"><span data-stu-id="2c299-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="2c299-230">แปลงไฟล์ `FONewParty.csv` เป็นไฟล์ Excel และนําเข้าไฟล์ Excel ไปยังแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2c299-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="2c299-231">หากการนําเข้า csv ใช้ได้ คุณสามารถนําเข้าไฟล์ csv ได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="2c299-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="2c299-232">การนําเข้าอาจใช้เวลาสองสามชั่วโมงในการรัน ทั้งนี้ขึ้นอยู่กับปริมาณข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2c299-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="2c299-233">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของงานนำเข้าและส่งออกข้อมูล](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job)</span><span class="sxs-lookup"><span data-stu-id="2c299-233">For more information, see [Data import and export jobs overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span></span>

    ![นําเข้าเรกคอร์ดฝ่ายของ Datavers](media/data-factory-import-party.png)

9. <span data-ttu-id="2c299-235">ในแอปการมีส่วนร่วมกับลูกค้า ให้เปิดใช้งานขั้นตอนปลั๊กอินต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c299-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="2c299-236">การอัปเดตบัญชี</span><span class="sxs-lookup"><span data-stu-id="2c299-236">Account Update</span></span>
         + <span data-ttu-id="2c299-237">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromAccountEntity: อัปเดตบัญชี</span><span class="sxs-lookup"><span data-stu-id="2c299-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="2c299-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: อัปเดตบัญชี</span><span class="sxs-lookup"><span data-stu-id="2c299-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="2c299-239">การอัปเดตผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2c299-239">Contact Update</span></span>
         + <span data-ttu-id="2c299-240">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromContactEntity: อัปเดตผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2c299-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="2c299-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: อัปเดตผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2c299-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="2c299-242">อัปเดต msdyn_party</span><span class="sxs-lookup"><span data-stu-id="2c299-242">msdyn_party Update</span></span>
         + <span data-ttu-id="2c299-243">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromPartyEntity: การอัปเดต msdyn_party</span><span class="sxs-lookup"><span data-stu-id="2c299-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="2c299-244">การอัปเดต msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="2c299-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="2c299-245">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromVendorEntity: การอัปเดต msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="2c299-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="2c299-246">ในแอปการมีส่วนร่วมกับลูกค้า ให้เรียกใช้ลำดับงานต่อไปนี้ หากคุณยกเลิกการเรียกใช้ในขั้นตอนก่อนหน้า:</span><span class="sxs-lookup"><span data-stu-id="2c299-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="2c299-247">สร้างผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="2c299-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="2c299-248">สร้างผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="2c299-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="2c299-249">สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2c299-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="2c299-250">สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2c299-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="2c299-251">อัปเดตผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="2c299-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="2c299-252">อัปเดตผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2c299-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="2c299-253">อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2c299-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="2c299-254">อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2c299-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="2c299-255">รันแผนผังที่เกี่ยวข้องกับ **ฝ่าย** ตามที่สั่งใน [สมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล](party-gab.md)</span><span class="sxs-lookup"><span data-stu-id="2c299-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2c299-256">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="2c299-256">Troubleshooting</span></span>

1. <span data-ttu-id="2c299-257">ในกระบวนการล้มเหลว ให้รัน Data Factory ใหม่เริ่มต้นจากกิจกรรมที่ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="2c299-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="2c299-258">บางไฟล์จะถูกสร้างขึ้นโดย Data Factory ที่คุณสามารถใช้เพื่อวัตถุประสงค์การตรวจสอบความถูกต้องของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2c299-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="2c299-259">Data Factory จะรันตามไฟล์ csv ที่คั่นด้วยเครื่องหมายจุลภาค</span><span class="sxs-lookup"><span data-stu-id="2c299-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="2c299-260">ถ้ามีค่าฟิลด์ที่มีเครื่องหมายจุลภาค อาจใช้เฉพาะกับผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="2c299-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="2c299-261">คุณต้องลบเครื่องหมายจุลภาค</span><span class="sxs-lookup"><span data-stu-id="2c299-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="2c299-262">แท็บ **การตรวจสอบ** แสดงข้อมูลเกี่ยวกับขั้นตอนและข้อมูลทั้งหมดที่ประมวลผล</span><span class="sxs-lookup"><span data-stu-id="2c299-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="2c299-263">เลือกขั้นตอนเฉพาะเพื่อดีบักขั้นตอนนั้น</span><span class="sxs-lookup"><span data-stu-id="2c299-263">Select a specific step to debug it.</span></span>

    ![แท็บการตรวจสอบ](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="2c299-265">เรียนรู้เพิ่มเติมเกี่ยวกับแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="2c299-265">Learn more about the template</span></span>

<span data-ttu-id="2c299-266">คุณสามารถค้นหาข้อคิดเห็นเกี่ยวกับแม่แบบไฟล์ [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)</span><span class="sxs-lookup"><span data-stu-id="2c299-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>
