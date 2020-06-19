---
title: แก้ไขปัญหาในระหว่างการซิงโครไนส์เริ่มต้น
description: หัวข้อนี้แสดงข้อมูลการแก้ไขปัญหาที่สามารถช่วยคุณแก้ไขปัญหาที่อาจเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410092"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="cd2ec-103">แก้ไขปัญหาในระหว่างการซิงโครไนส์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cd2ec-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cd2ec-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cd2ec-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="cd2ec-105">กล่าวคือ จะแสดงข้อมูลที่สามารถช่วยคุณแก้ไขปัญหาที่อาจเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cd2ec-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd2ec-106">ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="cd2ec-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="cd2ec-107">ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="cd2ec-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="cd2ec-108">ตรวจสอบข้อผิดพลาดของการซิงโครไนส์เริ่มต้นในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cd2ec-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="cd2ec-109">หลังจากที่คุณเปิดใช้งานเท็มเพลตการแม็ป สถานะของแผนที่ควรเป็น **กำลังรัน**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="cd2ec-110">ถ้าสถานะ **ไม่ได้รันอยู่** ข้อผิดพลาดเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cd2ec-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="cd2ec-111">เมื่อต้องการดูข้อผิดพลาด ให้เลือกแท็บ **รายละเอียดการซิงค์เริ่มต้น** บนหน้า **การรวมแบบสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![แท็บรายละเอียดการซิงค์เริ่มต้น](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="cd2ec-113">คุณไม่สามารถดำเนินการซิงโครไนส์เริ่มต้นให้เสร็จสมบูรณ์ได้: 400 คำขอไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="cd2ec-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="cd2ec-114">**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="cd2ec-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="cd2ec-115">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามรันการแม็ปและการซิงโครไนส์เริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="cd2ec-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="cd2ec-116">*เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (400) คำขอไม่ถูกต้อง) AX การส่งออกพบข้อผิดพลาด*</span><span class="sxs-lookup"><span data-stu-id="cd2ec-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="cd2ec-117">นี่เป็นตัวอย่างของข้อความแสดงข้อผิดพลาดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cd2ec-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="cd2ec-118">ถ้าเกิดข้อผิดพลาดนี้อย่างสม่ำเสมอ และคุณไม่สามารถดำเนินการซิงโครไนส์เริ่มต้นให้เสร็จสมบูรณ์ได้ ให้ทำตามขั้นตอนต่อไปนี้เพื่อแก้ไขปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="cd2ec-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="cd2ec-119">ลงชื่อเข้าใช้ในเครื่องเสมือน (VM) สำหรับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cd2ec-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="cd2ec-120">เปิด Microsoft Management Console</span><span class="sxs-lookup"><span data-stu-id="cd2ec-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="cd2ec-121">ในบานหน้าต่าง **บริการ** ตรวจสอบให้แน่ใจว่ามีการเรียกใช้บริการกรอบงานการนำเข้าการส่งออกข้อมูล Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cd2ec-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="cd2ec-122">เริ่มต้นใหม่ ถ้าถูกหยุดเนื่องจากการซิงโครไนส์เริ่มต้นต้องการ</span><span class="sxs-lookup"><span data-stu-id="cd2ec-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="cd2ec-123">ข้อผิดพลาดการซิงโครไนส์เริ่มต้น: 403 ไม่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="cd2ec-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="cd2ec-124">คุณอาจได้รับข้อความแสดงข้อผิดพลาดในระหว่างการซิงโครไนส์เริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="cd2ec-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="cd2ec-125">*(\[ไม่ได้รับอนุญาต\] เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (403) ไม่ได้รับอนุญาต) AX การส่งออกพบข้อผิดพลาด*</span><span class="sxs-lookup"><span data-stu-id="cd2ec-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="cd2ec-126">เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="cd2ec-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="cd2ec-127">ลงชื่อเข้าใช้แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cd2ec-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="cd2ec-128">บนหน้า **แอพลิเคชัน Azure Active Directory** ให้ลบไคลเอนต์ **DtAppID** และจากนั้น เพิ่มใหม่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="cd2ec-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![รายการของแอพลิเคชัน Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="cd2ec-130">ความล้มเหลวในการอ้างอิงตนเองหรือการอ้างอิงหมุนเวียนในระหว่างการซิงโครไนส์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cd2ec-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="cd2ec-131">คุณอาจได้รับข้อความแสดงข้อผิดพลาด ถ้าการแม็ปใดๆ ของคุณมีการอ้างอิงตนเองหรือการอ้างอิงหมุนเวียน</span><span class="sxs-lookup"><span data-stu-id="cd2ec-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="cd2ec-132">ข้อผิดพลาดจะอยู่ในประเภทเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="cd2ec-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="cd2ec-133">ผู้จัดจำหน่าย V2 สำหรับการแม็ปเอนทิตี msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="cd2ec-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="cd2ec-134">ลูกค้า V3 สำหรับการแม็ปเอนทิตีบัญชี</span><span class="sxs-lookup"><span data-stu-id="cd2ec-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="cd2ec-135">แก้ไขข้อผิดพลาดในผู้จัดจำหน่าย V2 สำหรับการแม็ปเอนทิตี msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="cd2ec-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="cd2ec-136">คุณอาจพบข้อผิดพลาดในการซิงค์เริ่มต้นต่อไปนี้ใน **ผู้จัดจำหน่าย V2** สำหรับการแม็ป **msdyn_vendors** ถ้าเอนทิตีมีเรกคอร์ดที่มีอยู่ซึ่งมีค่าในฟิลด์ **PrimaryContactPersonId** และ **InvoiceVendorAccountNumber**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="cd2ec-137">การทำเช่นนี้เนื่องจาก **InvoiceVendorAccountNumber** เป็นฟิลด์ที่อ้างอิงถึงตนเอง และ **PrimaryContactPersonId** เป็นการอ้างอิงหมุนเวียนในการแม็ปผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="cd2ec-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="cd2ec-138">*ไม่สามารถแก้ไข guid สำหรับฟิลด์: <field> ไม่พบการค้นหา: <value> ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="cd2ec-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="cd2ec-139">นี่คือตัวอย่างสองรายการ:</span><span class="sxs-lookup"><span data-stu-id="cd2ec-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="cd2ec-140">*ไม่สามารถแก้ไข guid สำหรับฟิลด์: msdyn_vendorprimarycontactperson msdyn_contactpersonid ไม่พบการค้นหา: 000056 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="cd2ec-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="cd2ec-141">*ไม่สามารถแก้ไข guid สำหรับฟิลด์: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber ไม่พบการค้นหา: V24-1 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="cd2ec-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="cd2ec-142">ถ้าคุณมีเรกคอร์ดที่มีค่าในฟิลด์เหล่านี้ในเอนทิตีของผู้จัดจำหน่าย ให้ทำตามขั้นตอนในส่วนด้านล่างเพื่อทำการซิงค์เริ่มต้นให้เสร็จเรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="cd2ec-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="cd2ec-143">ในแอป Finance and Operations ให้ลบฟิลด์ **PrimaryContactPersonId** และ **InvoiceVendorAccountNumber** จากการแม็ป และบันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="cd2ec-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="cd2ec-144">นำทางไปยังหน้าการแม็ปการรวมแบบสองทิศทางสำหรับ **ผู้จัดจำหน่าย V2 (msdyn_vendors)** และเลือกแท็บ **การแม็ปเอนทิตี** ในตัวกรองด้านซ้าย ให้เลือก **แอป Finance and Operations ผู้จัดจำหน่าย V2**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="cd2ec-145">ในตัวกรองสิทธิ์ เลือก **Sales.Vendor**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="cd2ec-146">ค้นหา **primarycontactperson** เพื่อค้นหาฟิลด์ต้นทาง **PrimaryContactPersonId**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="cd2ec-147">คลิกปุ่ม **การดำเนินการ** แล้วเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="cd2ec-149">ทำซ้ำเพื่อลบฟิลด์ **InvoiceVendorAccountNumber**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="cd2ec-151">บันทึกการเปลี่ยนแปลงการแม็ป</span><span class="sxs-lookup"><span data-stu-id="cd2ec-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="cd2ec-152">ปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับเอนทิตี **ผู้จัดจำหน่าย V2**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="cd2ec-153">นำทางไปยัง **การจัดการข้อมูล \> เอนทิตีข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="cd2ec-154">เลือกเอนทิตี **ผู้จัดจำหน่าย V2**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="cd2ec-155">คลิก **ตัวเลือก** จากแถบเมนู แล้วจากนั้น **เปลี่ยนแปลงการติดตาม**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 5](media/selfref_options.png)
    
    4. <span data-ttu-id="cd2ec-157">คลิก **ปิดใช้งานเปลี่ยนแปลงการติดตาม**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-157">Click **Disable Change Tracking**.</span></span>
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 6](media/selfref_tracking.png)

3. <span data-ttu-id="cd2ec-159">รันการซิงค์เริ่มต้นของการแม็ป **ผู้จัดจำหน่าย V2 (msdyn_vendors)**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="cd2ec-160">การซิงค์เริ่มต้นควรรันเสร็จเรียบร้อยโดยไม่มีข้อผิดพลาดใดๆ</span><span class="sxs-lookup"><span data-stu-id="cd2ec-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="cd2ec-161">รันการซิงค์เริ่มต้นสำหรับการแม็ป **ผู้ติดต่อของ CDS V2 (ผู้ติดต่อ)**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="cd2ec-162">คุณต้องซิงค์การแม็ปนี้ ถ้าคุณต้องการซิงค์ฟิลด์ผู้ติดต่อหลักบนเอนทิตีของผู้จัดจำหน่าย เนื่องจากเรกคอร์ดผู้ติดต่อยังต้องมีการซิงค์เริ่มต้นด้วย</span><span class="sxs-lookup"><span data-stu-id="cd2ec-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="cd2ec-163">เพิ่มฟิลด์ **PrimaryContactPersonId** และ **InvoiceVendorAccountNumber** กลับไปยังการแม็ป **ผู้จัดจำหน่าย V2 (msdyn_vendors)** และบันทึกการแม็ป</span><span class="sxs-lookup"><span data-stu-id="cd2ec-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="cd2ec-164">รันการซิงค์เริ่มต้นอีกครั้งสำหรับการแม็ป **ผู้จัดจำหน่าย V2 (msdyn_vendors)**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="cd2ec-165">เรกคอร์ดทั้งหมดจะถูกซิงค์ เนื่องจากมีการปิดใช้งานการติดตามการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="cd2ec-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="cd2ec-166">เปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับเอนทิตี **ผู้จัดจำหน่าย V2**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="cd2ec-167">แก้ไขข้อผิดพลาดในลูกค้า V3 สำหรับการแม็ปเอนทิตีบัญชี</span><span class="sxs-lookup"><span data-stu-id="cd2ec-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="cd2ec-168">คุณอาจพบข้อผิดพลาดในการซิงค์เริ่มต้นต่อไปนี้ใน **ลูกค้า V3** สำหรับการแม็ป **บัญชี** ถ้าเอนทิตีมีเรกคอร์ดที่มีอยู่ซึ่งมีค่าในฟิลด์ **ContactPersonID** และ **InvoiceAccount**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="cd2ec-169">การทำเช่นนี้เนื่องจาก **InvoiceAccount** เป็นฟิลด์ที่อ้างอิงตนเอง และ **ContactPersonID** เป็นการอ้างอิงหมุนเวียนในการแม็ปผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="cd2ec-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="cd2ec-170">*ไม่สามารถแก้ไข guid สำหรับฟิลด์: <field> ไม่พบการค้นหา: <value> ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="cd2ec-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="cd2ec-171">*ไม่สามารถแก้ไข guid สำหรับฟิลด์: primarycontactid.msdyn_contactpersonid ไม่พบการค้นหา: 000056 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="cd2ec-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="cd2ec-172">*ไม่สามารถแก้ไข guid สำหรับฟิลด์: msdyn_billingaccount.accountnumber ไม่พบการค้นหา: 1206-1 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="cd2ec-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="cd2ec-173">ถ้าคุณมีเรกคอร์ดที่มีค่าในฟิลด์เหล่านี้ในเอนทิตีของลูกค้า ให้ทำตามขั้นตอนในส่วนด้านล่างเพื่อทำการซิงค์เริ่มต้นให้เสร็จเรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="cd2ec-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="cd2ec-174">คุณสามารถใช้วิธีการนี้สำหรับเอนทิตีแบบสำเร็จรูปใดๆ เช่น ลูกค้าองค์กร และผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="cd2ec-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="cd2ec-175">ในแอป Finance and Operations เพิ่มฟิลด์ **ContactPersonID** และ **InvoiceAccount** จากการแม็ป **ลูกค้า V3 (บัญชี)** และบันทึกการแม็ป</span><span class="sxs-lookup"><span data-stu-id="cd2ec-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="cd2ec-176">นำทางไปยังหน้าการแม็ปการรวมแบบสองทิศทางสำหรับ **ลูกค้า V3 (บัญชี)** และเลือกแท็บ **การแม็ปเอนทิตี** ในตัวกรองด้านซ้าย ให้เลือก **Finance and Operations app.Customers V3**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="cd2ec-177">ในตัวกรองสิทธิ์ เลือก **Common Data Service.Account**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="cd2ec-178">ค้นหา **contactperson** เพื่อค้นหาฟิลด์ต้นทาง **ContactPersonID**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="cd2ec-179">คลิกปุ่ม **การดำเนินการ** แล้วเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="cd2ec-181">ทำซ้ำเพื่อลบฟิลด์ **InvoiceAccount**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![การอ้างอิงตนเองหรือหมุนเวียน](media/cust_selfref4.png)
    
    5. <span data-ttu-id="cd2ec-183">บันทึกการเปลี่ยนแปลงการแม็ป</span><span class="sxs-lookup"><span data-stu-id="cd2ec-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="cd2ec-184">ปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับเอนทิตี **ลูกค้า V3**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="cd2ec-185">นำทางไปยัง **การจัดการข้อมูล \> เอนทิตีข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="cd2ec-186">เลือกเอนทิตี **ลูกค้า V3**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="cd2ec-187">คลิก **ตัวเลือก** จากแถบเมนู แล้วจากนั้น **เปลี่ยนแปลงการติดตาม**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 5](media/selfref_options.png)
    
    4. <span data-ttu-id="cd2ec-189">คลิก **ปิดใช้งานเปลี่ยนแปลงการติดตาม**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-189">Click **Disable Change Tracking**.</span></span>
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 6](media/selfref_tracking.png)

3. <span data-ttu-id="cd2ec-191">รันการซิงค์เริ่มต้นสำหรับการแม็ป **ลูกค้า V3 (บัญชี)**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="cd2ec-192">การซิงค์เริ่มต้นควรรันเสร็จเรียบร้อยโดยไม่มีข้อผิดพลาดใดๆ</span><span class="sxs-lookup"><span data-stu-id="cd2ec-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="cd2ec-193">รันการซิงค์เริ่มต้นสำหรับการแม็ป **ผู้ติดต่อของ CDS V2 (ผู้ติดต่อ)**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="cd2ec-194">มี 2 แผนที่ที่มีชื่อเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="cd2ec-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="cd2ec-195">เลือกหนึ่งรายการที่มีคำอธิบาย **แม่แบบการรวมแบบสองทิศทางสำหรับการซิงค์ระหว่าง FO.CDS Vendor Contacts V2 ไปยัง CDS.Contacts ต้องมีแพคเกจใหม่ \[Dynamics365SupplyChainExtended\]**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="cd2ec-196">บนแท็บ **รายละเอียด** ของแผนที่</span><span class="sxs-lookup"><span data-stu-id="cd2ec-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="cd2ec-197">เพิ่มฟิลด์ **InvoiceAccount** และ **ContactPersonId** กลับไปยังการแม็ป **ลูกค้า V3 (บัญชี)** และบันทึกการแม็ป</span><span class="sxs-lookup"><span data-stu-id="cd2ec-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="cd2ec-198">ตอนนี้ทั้งฟิลด์ **InvoiceAccount** และฟิลด์ **ContactPersonId** เป็นส่วนหนึ่งของโหมดการซิงค์ที่เริ่มใช้งานจริงอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="cd2ec-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="cd2ec-199">ในขั้นตอนถัดไป คุณดำเนินการซิงค์เริ่มต้นสำหรับฟิลด์เหล่านี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="cd2ec-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="cd2ec-200">รันการซิงค์เริ่มต้นอีกครั้งสำหรับการแม็ป **ลูกค้า V3 (บัญชี)**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="cd2ec-201">เนื่องจากการติดตามการเปลี่ยนแปลงถูกปิดใช้งาน การรันการซิงค์จะซิงค์ข้อมูลสำหรับ **InvoiceAccount** และ **ContactPersonId** จากแอป Finance and Operations ไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cd2ec-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="cd2ec-202">เมื่อต้องการซิงค์ข้อมูลสำหรับ **InvoiceAccount** และ **ContactPersonId** จาก Common Data Service ไปยัง Finance and Operations คุณใช้โครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cd2ec-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="cd2ec-203">ใน Power Apps ให้สร้างโครงการการรวมข้อมูลระหว่างเอนทิตี **Sales.Account** และ **Finance and Operations apps.Customers V3**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="cd2ec-204">ทิศทางของข้อมูลต้องมาจาก Common Data Service ไปยังแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cd2ec-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="cd2ec-205">เนื่องจาก **InvoiceAccount** เป็นแอททริบิวต์ใหม่ในการรวมแบบสองทิศทาง คุณอาจต้องการข้ามการซิงค์เริ่มต้นสำหรับแอททริบิวต์นี้</span><span class="sxs-lookup"><span data-stu-id="cd2ec-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="cd2ec-206">สำหรับข้อมูลเพิ่มเติม ดู [รวมข้อมูลลงใน Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator)</span><span class="sxs-lookup"><span data-stu-id="cd2ec-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="cd2ec-207">รูปภาพต่อไปนี้แสดงโครงการที่ปรับปรุง **CustomerAccount** และ **ContactPersonId**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![การอ้างอิงตนเองหรือหมุนเวียน](media/cust_selfref6.png)

    2. <span data-ttu-id="cd2ec-209">เพิ่มเงื่อนไขของบริษัทในตัวกรองในฝั่ง Common Data Service เนื่องจากมีการปรับปรุงเฉพาะเรกคอร์ดที่ตรงกับเงื่อนไขตัวกรองในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cd2ec-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="cd2ec-210">เมื่อต้องการเพิ่มตัวกรอง ให้คลิกไอคอนตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="cd2ec-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="cd2ec-211">ในกล่องโต้ตอบ **แก้ไขการสอบถาม** คุณสามารถเพิ่มการสอบถามตัวกรอง เช่น **_msdyn_company_value eq '\<guid\>'**</span><span class="sxs-lookup"><span data-stu-id="cd2ec-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="cd2ec-212">ถ้าไม่มีไอคอนตัวกรองอยู่ ให้สร้างตั๋วสนับสนุนเพื่อขอทีมงานการรวมข้อมูลเพื่อเปิดใช้งานความสามารถในการกรองของผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="cd2ec-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="cd2ec-213">ถ้าคุณไม่ได้ป้อนการสอบถามตัวกรองสำหรับ **_msdyn_company_value** เรกคอร์ดทั้งหมดจะถูกซิงค์</span><span class="sxs-lookup"><span data-stu-id="cd2ec-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![การอ้างอิงตนเองหรือหมุนเวียน](media/cust_selfref7.png)

        <span data-ttu-id="cd2ec-215">การดำเนินการนี้จะทำให้การซิงค์เริ่มต้นของเรกคอร์ดเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="cd2ec-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="cd2ec-216">เปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับเอนทิตี **ลูกค้า V3** ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cd2ec-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

