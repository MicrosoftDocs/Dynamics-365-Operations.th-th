---
title: อัปเกรดเป็นรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล
description: หัวข้อนี้จะอธิบายวิธีการอัปเกรดข้อมูลแบบสองทิศทางให้กับรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112684"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="14b95-103">อัปเกรดเป็นรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล</span><span class="sxs-lookup"><span data-stu-id="14b95-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="14b95-104">[แม่แบบ Microsoft Azure Data Factory](https://aka.ms/dual-write-gab-adf) ช่วยคุณในการอัปเกรดข้อมูลตาราง **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** แบบสองทิศทางให้กับไปยังรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล</span><span class="sxs-lookup"><span data-stu-id="14b95-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="14b95-105">แม่แบบจะกระทบยอดข้อมูลจากทั้งแอป Finance and Operations และแอปการมีส่วนร่วมกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="14b95-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="14b95-106">เมื่อสิ้นสุดกระบวนการ ฟิลด์ **ฝ่าย** และ **ผู้ติดต่อ** ของเรกคอร์ด **ฝ่าย** จะมีการสร้างและเชื่อมโยงกับเรกคอร์ด **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ในแอปการมีส่วนร่วมกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="14b95-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="14b95-107">ไฟล์ .csv (`FONewParty.csv`) ถูกสร้างขึ้นเพื่อสร้างเรกคอร์ด **ฝ่าย** ใหม่ภายในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="14b95-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="14b95-108">หัวข้อนี้จะให้คําแนะนําในการใช้แม่แบบ Data Factory และอัปเกรดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="14b95-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="14b95-109">ถ้าคุณไม่มีการกำหนดใด ๆ คุณสามารถใช้แม่แบบตามที่เป็นได้</span><span class="sxs-lookup"><span data-stu-id="14b95-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="14b95-110">ถ้าคุณมีการกำหนดสำหรับ **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** จากนั้นคุณต้องปรับเปลี่ยนแม่แบบโดยใช้คําแนะนําต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="14b95-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="14b95-111">แม่แบบจะอัปเกรดเฉพาะข้อมูล **ฝ่าย**</span><span class="sxs-lookup"><span data-stu-id="14b95-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="14b95-112">ในการนำออกใช้ในอนาคต ที่อยู่ไปรษณีย์และที่อยู่อิเล็กทรอนิกส์จะถูกรวมไว้ด้วย</span><span class="sxs-lookup"><span data-stu-id="14b95-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="14b95-113">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="14b95-113">Prerequisites</span></span>

<span data-ttu-id="14b95-114">ข้อเบื้องต้นต่อไปนี้จำเป็นเพื่ออัปเกรดเป็นแบบโมเดลฝ่ายและสมุดที่อยู่สากล:</span><span class="sxs-lookup"><span data-stu-id="14b95-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="14b95-115">การบอกรับเป็นสมาชิก Azure</span><span class="sxs-lookup"><span data-stu-id="14b95-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="14b95-116">เข้าถึงแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="14b95-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="14b95-117">คุณต้องเป็นลูกค้าการรวมแบบสองทิศทางที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="14b95-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="14b95-118">จัดเตรียมสำหรับการอัปเกรด</span><span class="sxs-lookup"><span data-stu-id="14b95-118">Prepare for the upgrade</span></span>
<span data-ttu-id="14b95-119">กิจกรรมต่อไปนี้ต้องเตรียมการเพื่อเตรียมการอัปเกรด</span><span class="sxs-lookup"><span data-stu-id="14b95-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="14b95-120">**ซิงค์อย่างครบถ้วน**: ทั้งสองสภาพแวดล้อมอยู่ในสถานะถูกซิงค์อย่างครบถ้วนแล้วสำหรับ **บัญชี (ลูกค้า)** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="14b95-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="14b95-121">**คีย์การรวม**: ตาราง **บัญชี (ลูกค้า)** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ในแอปการมีส่วนร่วมกับลูกค้าใช้คีย์การรวมที่จัดส่งแบบสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="14b95-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="14b95-122">ถ้าคุณเลือกกำหนดคีย์การรวมเอง คุณต้องเลือกกำหนดแม่แบบเอง</span><span class="sxs-lookup"><span data-stu-id="14b95-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="14b95-123">**หมายเลขฝ่าย**: เรกคอร์ด **บัญชี (ลูกค้า)** ทั้งหมด **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ที่จะอัปเกรดมีหมายเลข **ฝ่าย**</span><span class="sxs-lookup"><span data-stu-id="14b95-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="14b95-124">เรกคอร์ดที่ไม่มีหมายเลข **ฝ่าย** จะถูกละเว้น</span><span class="sxs-lookup"><span data-stu-id="14b95-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="14b95-125">ถ้าคุณต้องการอัปเกรดเรกคอร์ดเหล่านั้น ให้เพิ่มหมายเลข **ฝ่าย** ก่อนที่คุณจะเริ่มกระบวนการอัปเกรด</span><span class="sxs-lookup"><span data-stu-id="14b95-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="14b95-126">**ความขัดข้องของระบบ**: ในระหว่างกระบวนการอัปเกรด คุณจะต้องใช้ทั้งสภาพแวดล้อม Finance and Operations และการมีส่วนร่วมกับลูกค้าออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="14b95-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="14b95-127">**สแนปช็อต**: ถ่ายภาพสแนปช็อตของทั้งแอป Finance and Operations และแอปการมีส่วนร่วมกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="14b95-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="14b95-128">ใช้สแนปช็อตเพื่อคืนสถานะก่อนหน้านี้ถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="14b95-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="14b95-129">การจัดวาง</span><span class="sxs-lookup"><span data-stu-id="14b95-129">Deployment</span></span>

1. <span data-ttu-id="14b95-130">ดาวน์โหลดแม่แบบจาก [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf)</span><span class="sxs-lookup"><span data-stu-id="14b95-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="14b95-131">ลงชื่อเข้าใช้ [Microsoft Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="14b95-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="14b95-132">สร้าง [กลุ่มทรัพยากร](/azure/azure-resource-manager/management/manage-resource-groups-portal)</span><span class="sxs-lookup"><span data-stu-id="14b95-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="14b95-133">สร้าง [บัญชีการจัดเก็บ](/azure/storage/common/storage-account-create?tabs=azure-portal) ในกลุ่มทรัพยากรที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="14b95-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="14b95-134">สร้าง [Data Factory](/azure/data-factory/quickstart-create-data-factory-portal) เหนือกลุ่มทรัพยากรที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="14b95-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="14b95-135">เปิด Data Factory และเลือกไทล์ **สร้าง & ตรวจสอบ**</span><span class="sxs-lookup"><span data-stu-id="14b95-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="14b95-136">บนแท็บ **จัดการ** ให้เลือก **แม่แบบ ARM**</span><span class="sxs-lookup"><span data-stu-id="14b95-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="14b95-137">เลือกแม่แบบ **นำเข้าแม่แบบ ARM** เพื่อนําเข้าแม่แบบ **ฝ่าย**</span><span class="sxs-lookup"><span data-stu-id="14b95-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="14b95-138">นําเข้าแม่แบบไปยัง Data Factory</span><span class="sxs-lookup"><span data-stu-id="14b95-138">Import the template into the data factory.</span></span> <span data-ttu-id="14b95-139">ป้อนค่าต่อไปนี้ให้กับ **รายละเอียดโครงการ** และ **รายละเอียดอินสแตนซ์**</span><span class="sxs-lookup"><span data-stu-id="14b95-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="14b95-140">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="14b95-140">Field</span></span> | <span data-ttu-id="14b95-141">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="14b95-141">Value</span></span>
    ---|---
    <span data-ttu-id="14b95-142">การบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="14b95-142">Subscription</span></span> | <span data-ttu-id="14b95-143">การบอกรับเป็นสมาชิก Azure</span><span class="sxs-lookup"><span data-stu-id="14b95-143">Azure subscription</span></span>
    <span data-ttu-id="14b95-144">กลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="14b95-144">Resource group</span></span> | <span data-ttu-id="14b95-145">ระบุทรัพยากรเดียวกันกับที่มีการสร้างบัญชีการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="14b95-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="14b95-146">ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="14b95-146">Region</span></span> | <span data-ttu-id="14b95-147">ระบุภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="14b95-147">Specify region.</span></span>
    <span data-ttu-id="14b95-148">ชื่อโรงงาน</span><span class="sxs-lookup"><span data-stu-id="14b95-148">Factory Name</span></span> | <span data-ttu-id="14b95-149">ระบุชื่อโรงงาน</span><span class="sxs-lookup"><span data-stu-id="14b95-149">Specify factory name.</span></span>
    <span data-ttu-id="14b95-150">คีย์หลัก FO ที่เชื่อมโยง Service_service</span><span class="sxs-lookup"><span data-stu-id="14b95-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="14b95-151">ระบุคีย์ของโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="14b95-151">Specify the application's key.</span></span>
    <span data-ttu-id="14b95-152">ที่เก็บข้อมูล Azure Blob_สตริงการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="14b95-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="14b95-153">สตริงการเชื่อมต่อที่เก็บข้อมูล Azure Blob</span><span class="sxs-lookup"><span data-stu-id="14b95-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="14b95-154">Dynamics Crm ที่เชื่อมโยง Service_password</span><span class="sxs-lookup"><span data-stu-id="14b95-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="14b95-155">รหัสผ่านของบัญชีผู้ใช้ที่คุณระบุเป็นชื่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="14b95-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="14b95-156">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="14b95-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="14b95-157">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="14b95-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="14b95-158">ระบุข้อมูลผู้เช่า (ชื่อโดเมนหรือรหัสผู้เช่า) ที่โปรแกรมประยุกต์ของคุณอยู่</span><span class="sxs-lookup"><span data-stu-id="14b95-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="14b95-159">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="14b95-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="14b95-160">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="14b95-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="14b95-161">ระบุรหัสไคลเอนต์ของโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="14b95-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="14b95-162">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="14b95-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="14b95-163">ชื่อผู้ใช้ที่จะเชื่อมต่อกับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="14b95-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="14b95-164">สำหรับข้อมูลเพิ่มเติม โปรดดูหัวข้อต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="14b95-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="14b95-165">เลื่อนระดับแม่แบบ Resource Manager ด้วยตนเองในแต่ละสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="14b95-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="14b95-166">คุณสมบัติของบริการที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="14b95-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="14b95-167">คัดลอกข้อมูลโดยใช้ Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="14b95-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="14b95-168">หลังจากใช้งานแล้ว ให้ตรวจสอบความถูกต้องของชุดข้อมูล ลำดับข้อมูล และบริการที่เชื่อมโยงของ Data Factory</span><span class="sxs-lookup"><span data-stu-id="14b95-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![ชุดข้อมูล ลำดับข้อมูล และบริการที่เชื่อมโยง](media/data-factory-validate.png)

11. <span data-ttu-id="14b95-170">นําทางไปยัง **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="14b95-170">Navigate to **Manage**.</span></span> <span data-ttu-id="14b95-171">ภายใต้ **การเชื่อมต่อ** ให้เลือก **บริการที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="14b95-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="14b95-172">เลือก **DynamicsCrmLinkedService**</span><span class="sxs-lookup"><span data-stu-id="14b95-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="14b95-173">ในฟอร์ม **แก้ไขบริการที่เชื่อมโยง (Dynamics CRM)** ให้ป้อนค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="14b95-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="14b95-174">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="14b95-174">Field</span></span> | <span data-ttu-id="14b95-175">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="14b95-175">Value</span></span>
    ---|---
    <span data-ttu-id="14b95-176">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="14b95-176">Name</span></span> | <span data-ttu-id="14b95-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="14b95-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="14b95-178">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="14b95-178">Description</span></span> | <span data-ttu-id="14b95-179">บริการที่เชื่อมโยงเพื่อเชื่อมต่อกับอินสแตนซ์ CRM เพื่อดึงข้อมูลเอนทิตีมาใช้</span><span class="sxs-lookup"><span data-stu-id="14b95-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="14b95-180">เชื่อมต่อผ่าน Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="14b95-180">Connect via integration runtime</span></span> | <span data-ttu-id="14b95-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="14b95-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="14b95-182">ชนิดการปรับใช้</span><span class="sxs-lookup"><span data-stu-id="14b95-182">Deployment type</span></span> | <span data-ttu-id="14b95-183">ออนไลน์</span><span class="sxs-lookup"><span data-stu-id="14b95-183">Online</span></span>
    <span data-ttu-id="14b95-184">Uri ของการบริการ</span><span class="sxs-lookup"><span data-stu-id="14b95-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="14b95-185">ชนิดการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="14b95-185">Authentication type</span></span> | <span data-ttu-id="14b95-186">Office365</span><span class="sxs-lookup"><span data-stu-id="14b95-186">Office365</span></span>
    <span data-ttu-id="14b95-187">ชื่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="14b95-187">User name</span></span> |
    <span data-ttu-id="14b95-188">รหัสผ่านหรือ Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="14b95-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="14b95-189">รหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="14b95-189">Password</span></span>
    <span data-ttu-id="14b95-190">รหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="14b95-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="14b95-191">เรียกใช้แม่แบบ</span><span class="sxs-lookup"><span data-stu-id="14b95-191">Run the template</span></span>

1. <span data-ttu-id="14b95-192">หยุดแม็ปการรวมแบบสองทิศทาง **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ต่อไปนี้โดยใช้แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="14b95-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="14b95-193">Customers V3 (บัญชี)</span><span class="sxs-lookup"><span data-stu-id="14b95-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="14b95-194">ลูกค้า V3(ผู้ติดต่อ)</span><span class="sxs-lookup"><span data-stu-id="14b95-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="14b95-195">ผู้ติดต่อของ CDS V2(ผู้ติดต่อ)</span><span class="sxs-lookup"><span data-stu-id="14b95-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="14b95-196">ผู้ติดต่อของ CDS V2(ผู้ติดต่อ)</span><span class="sxs-lookup"><span data-stu-id="14b95-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="14b95-197">ผู้จัดจำหน่าย V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="14b95-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="14b95-198">ตรวจสอบให้แน่ใจว่าแผนที่ถูกลบออกจากตาราง `msdy_dualwriteruntimeconfig` ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="14b95-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="14b95-199">ติดตั้ง [ฝ่ายการรวมแบบสองทิศทางและโซลูชันสมุดที่อยู่สากล](https://aka.ms/dual-write-gab) จาก AppSource</span><span class="sxs-lookup"><span data-stu-id="14b95-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="14b95-200">ในแอป Finance and Operations หากตารางต่อไปนี้มีข้อมูล ให้รัน **การซิงค์ครั้งแรก**</span><span class="sxs-lookup"><span data-stu-id="14b95-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="14b95-201">คำขึ้นต้น</span><span class="sxs-lookup"><span data-stu-id="14b95-201">Salutations</span></span>
    + <span data-ttu-id="14b95-202">ชนิดลักษณะส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="14b95-202">Personal character types</span></span>
    + <span data-ttu-id="14b95-203">คำลงท้าย</span><span class="sxs-lookup"><span data-stu-id="14b95-203">Complimentary closing</span></span>
    + <span data-ttu-id="14b95-204">ตำแหน่งของผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="14b95-204">Contact person titles</span></span>
    + <span data-ttu-id="14b95-205">บทบาทในการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="14b95-205">Decision making roles</span></span>
    + <span data-ttu-id="14b95-206">ระดับของสมาชิก</span><span class="sxs-lookup"><span data-stu-id="14b95-206">Loyalty levels</span></span>

5. <span data-ttu-id="14b95-207">ในแอปการมีส่วนร่วมกับลูกค้า ให้ปิดใช้งานขั้นตอนปลั๊กอินต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="14b95-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="14b95-208">การอัปเดตบัญชี</span><span class="sxs-lookup"><span data-stu-id="14b95-208">Account Update</span></span>
         + <span data-ttu-id="14b95-209">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromAccountEntity: อัปเดตบัญชี</span><span class="sxs-lookup"><span data-stu-id="14b95-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="14b95-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: อัปเดตบัญชี</span><span class="sxs-lookup"><span data-stu-id="14b95-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="14b95-211">การอัปเดตผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="14b95-211">Contact Update</span></span>
         + <span data-ttu-id="14b95-212">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromContactEntity: อัปเดตผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="14b95-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="14b95-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: อัปเดตผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="14b95-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="14b95-214">อัปเดต msdyn_party</span><span class="sxs-lookup"><span data-stu-id="14b95-214">msdyn_party Update</span></span>
         + <span data-ttu-id="14b95-215">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromPartyEntity: การอัปเดต msdyn_party</span><span class="sxs-lookup"><span data-stu-id="14b95-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="14b95-216">การอัปเดต msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="14b95-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="14b95-217">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromVendorEntity: การอัปเดต msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="14b95-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="14b95-218">ในแอปการมีส่วนร่วมกับลูกค้า ให้ปิดใช้งานลำดับงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b95-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="14b95-219">สร้างผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="14b95-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="14b95-220">สร้างผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="14b95-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="14b95-221">สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="14b95-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="14b95-222">สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="14b95-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="14b95-223">อัปเดตผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="14b95-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="14b95-224">อัปเดตผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="14b95-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="14b95-225">อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="14b95-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="14b95-226">อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="14b95-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="14b95-227">ใน Data Factory ให้รันแม่แบบโดยการเลือก **ทริกเกอร์ตอนนี้** ดังที่แสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="14b95-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="14b95-228">กระบวนการนี้อาจใช้เวลาสักครู่เพื่อกรอกข้อมูลตามปริมาณข้อมูล</span><span class="sxs-lookup"><span data-stu-id="14b95-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![การรันทริกเกอร์](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="14b95-230">ถ้าคุณมีการกำหนดสำหรับ **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** จากนั้นคุณต้องปรับเปลี่ยนแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="14b95-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="14b95-231">นําเข้าเรกคอร์ด **ฝ่าย** ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="14b95-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="14b95-232">ดาวน์โหลดไฟล์ `FONewParty.csv` จากที่จัดเก็บ Azure blob</span><span class="sxs-lookup"><span data-stu-id="14b95-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="14b95-233">พาธคือ `partybootstrapping/output/FONewParty.csv`</span><span class="sxs-lookup"><span data-stu-id="14b95-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="14b95-234">แปลงไฟล์ `FONewParty.csv` เป็นไฟล์ Excel และนําเข้าไฟล์ Excel ไปยังแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="14b95-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="14b95-235">หากการนําเข้า csv ใช้ได้ คุณสามารถนําเข้าไฟล์ csv ได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="14b95-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="14b95-236">การนําเข้าอาจใช้เวลาสองสามชั่วโมงในการรัน ทั้งนี้ขึ้นอยู่กับปริมาณข้อมูล</span><span class="sxs-lookup"><span data-stu-id="14b95-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="14b95-237">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของงานนำเข้าและส่งออกข้อมูล](../data-import-export-job.md)</span><span class="sxs-lookup"><span data-stu-id="14b95-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![นําเข้าเรกคอร์ดฝ่ายของ Datavers](media/data-factory-import-party.png)

9. <span data-ttu-id="14b95-239">ในแอปการมีส่วนร่วมกับลูกค้า ให้เปิดใช้งานขั้นตอนปลั๊กอินต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b95-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="14b95-240">การอัปเดตบัญชี</span><span class="sxs-lookup"><span data-stu-id="14b95-240">Account Update</span></span>
         + <span data-ttu-id="14b95-241">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromAccountEntity: อัปเดตบัญชี</span><span class="sxs-lookup"><span data-stu-id="14b95-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="14b95-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: อัปเดตบัญชี</span><span class="sxs-lookup"><span data-stu-id="14b95-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="14b95-243">การอัปเดตผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="14b95-243">Contact Update</span></span>
         + <span data-ttu-id="14b95-244">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromContactEntity: อัปเดตผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="14b95-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="14b95-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: อัปเดตผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="14b95-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="14b95-246">อัปเดต msdyn_party</span><span class="sxs-lookup"><span data-stu-id="14b95-246">msdyn_party Update</span></span>
         + <span data-ttu-id="14b95-247">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromPartyEntity: การอัปเดต msdyn_party</span><span class="sxs-lookup"><span data-stu-id="14b95-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="14b95-248">การอัปเดต msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="14b95-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="14b95-249">Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromVendorEntity: การอัปเดต msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="14b95-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="14b95-250">ในแอปการมีส่วนร่วมกับลูกค้า ให้เรียกใช้ลำดับงานต่อไปนี้ หากคุณยกเลิกการเรียกใช้ในขั้นตอนก่อนหน้า:</span><span class="sxs-lookup"><span data-stu-id="14b95-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="14b95-251">สร้างผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="14b95-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="14b95-252">สร้างผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="14b95-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="14b95-253">สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="14b95-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="14b95-254">สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="14b95-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="14b95-255">อัปเดตผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="14b95-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="14b95-256">อัปเดตผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="14b95-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="14b95-257">อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="14b95-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="14b95-258">อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="14b95-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="14b95-259">รันแผนผังที่เกี่ยวข้องกับ **ฝ่าย** ตามที่สั่งใน [สมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล](party-gab.md)</span><span class="sxs-lookup"><span data-stu-id="14b95-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="14b95-260">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="14b95-260">Troubleshooting</span></span>

1. <span data-ttu-id="14b95-261">ถ้ากระบวนการล้มเหลว ให้รัน Data Factory ใหม่เริ่มต้นจากกิจกรรมที่ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="14b95-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="14b95-262">บางไฟล์จะถูกสร้างขึ้นโดย Data Factory ที่คุณสามารถใช้เพื่อวัตถุประสงค์การตรวจสอบความถูกต้องของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="14b95-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="14b95-263">Data Factory จะรันตามไฟล์ csv ที่คั่นด้วยเครื่องหมายจุลภาค</span><span class="sxs-lookup"><span data-stu-id="14b95-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="14b95-264">ถ้ามีค่าฟิลด์ที่มีเครื่องหมายจุลภาค อาจใช้เฉพาะกับผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="14b95-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="14b95-265">คุณต้องลบเครื่องหมายจุลภาค</span><span class="sxs-lookup"><span data-stu-id="14b95-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="14b95-266">แท็บ **การตรวจสอบ** แสดงข้อมูลเกี่ยวกับขั้นตอนและข้อมูลทั้งหมดที่ประมวลผล</span><span class="sxs-lookup"><span data-stu-id="14b95-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="14b95-267">เลือกขั้นตอนเฉพาะเพื่อดีบักขั้นตอนนั้น</span><span class="sxs-lookup"><span data-stu-id="14b95-267">Select a specific step to debug it.</span></span>

    ![แท็บการตรวจสอบ](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="14b95-269">เรียนรู้เพิ่มเติมเกี่ยวกับแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="14b95-269">Learn more about the template</span></span>

<span data-ttu-id="14b95-270">คุณสามารถค้นหาข้อมูลเพิ่มเติมเกี่ยวกับแม่แบบใน [ข้อคิดเห็นสำหรับ readme ของแม่แบบ Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)</span><span class="sxs-lookup"><span data-stu-id="14b95-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
