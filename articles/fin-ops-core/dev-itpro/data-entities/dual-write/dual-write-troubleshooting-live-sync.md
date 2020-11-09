---
title: แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง
description: หัวข้อนี้แสดงข้อมูลการแก้ไขปัญหาที่สามารถช่วยคุณแก้ไขปัญหาเกี่ยวกับการซิงโครไนส์ที่เริ่มใช้งานจริง
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 82bdcc71196c22689cc65601f98187aaa9e5e9d6
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997313"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="94472-103">แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="94472-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="94472-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="94472-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="94472-105">กล่าวคือ จะแสดงข้อมูลที่สามารถช่วยคุณแก้ไขปัญหาเกี่ยวกับการซิงโครไนส์ที่เริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="94472-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94472-106">ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="94472-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="94472-107">ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="94472-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="94472-108">การซิงโครไนส์ที่เริ่มใช้งานจริงแสดงข้อผิดพลาด 403 ไม่ได้รับอนุญาต เมื่อคุณสร้างเรกคอร์ดในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="94472-108">Live synchronization throws a 403 Forbidden error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="94472-109">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณสร้างเรกคอร์ดในแอป Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="94472-109">You might receive the following error message when you create a record in a Finance and Operations app:</span></span>

<span data-ttu-id="94472-110">*\[{\\"ข้อผิดพลาด\\":{\\"รหัส\\":\\"0x80072560\\",\\"ข้อความ\\":\\"ผู้ใช้ไม่ใช่สมาชิกขององค์กร\\"}}\] เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (403) ไม่ได้รับอนุญาต"}}"*</span><span class="sxs-lookup"><span data-stu-id="94472-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="94472-111">เมื่อต้องการแก้ไขปัญหานี้ ให้ทำตามขั้นตอนใน [ข้อกำหนดของระบบและข้อกำหนดเบื้องต้น](requirements-and-prerequisites.md)</span><span class="sxs-lookup"><span data-stu-id="94472-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="94472-112">เมื่อต้องการดำเนินการตามขั้นตอนดังกล่าวให้เสร็จสมบูรณ์ ผู้ใช้แอพลิเคชันการรวมแบบสองทิศทางที่สร้างขึ้นใน Common Data Service ต้องมีบทบาทผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="94472-112">To complete those steps, the dual-write application users who are created in Common Data Service must have the system admin role.</span></span> <span data-ttu-id="94472-113">นอกจากนี้ ทีมงานที่เป็นเจ้าของเริ่มต้นต้องมีบทบาทผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="94472-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="94472-114">การซิงโครไนส์ที่เริ่มใช้งานจริงสำหรับเอนทิตี้ใดๆ แสดงข้อผิดพลาดที่คล้ายกันอย่างสม่ำเสมอ เมื่อคุณสร้างเรกคอร์ดในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="94472-114">Live synchronization for any entity consistently throws a similar error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="94472-115">**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="94472-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="94472-116">คุณอาจได้รับข้อความแสดงข้อผิดพลาดเช่นต่อไปนี้ทุกครั้งที่คุณพยายามบันทึกข้อมูลเอนทิตี้ในแอป Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="94472-116">You might receive an error message like the following every time that you try to save entity data in a Finance and Operations app:</span></span>

<span data-ttu-id="94472-117">*ไม่สามารถบันทึกการเปลี่ยนแปลงไปยังฐานข้อมูล หน่วยของงานไม่สามารถส่งธุรกรรมได้ ไม่สามารถเขียนข้อมูลไปยังเอนทิตี้ uoms ได้ เขียนไปยัง UnitOfMeasureEntity ล้มเหลว โดยมีข้อความแสดงข้อผิดพลาดว่า ไม่สามารถซิงค์กับเอนทิตี้ uoms ได้*</span><span class="sxs-lookup"><span data-stu-id="94472-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="94472-118">เมื่อต้องการแก้ไขปัญหานี้ คุณต้องตรวจสอบให้แน่ใจว่ามีข้อมูลอ้างอิงของข้อกำหนดเบื้องต้นอยู่ในทั้งแอป Finance and Operations และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="94472-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Common Data Service.</span></span> <span data-ttu-id="94472-119">ตัวอย่างเช่น ถ้าลูกค้าที่คุณอยู่ในแอป Finance and Operations เป็นของกลุ่มลูกค้าหนึ่งๆ โปรดตรวจสอบให้แน่ใจว่ามีกลุ่มลูกค้าอยู่ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="94472-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Common Data Service.</span></span>

<span data-ttu-id="94472-120">ถ้ามีข้อมูลอยู่ในทั้งสองด้าน และคุณยืนยันว่าปัญหานี้ไม่เกี่ยวข้องกับข้อมูล ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="94472-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="94472-121">หยุดเอนทิตี้ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="94472-121">Stop the related entity.</span></span>
2. <span data-ttu-id="94472-122">ลงชื่อเข้าใช้ในแอป Finance and Operations และตรวจสอบให้แน่ใจว่าเรกคอร์ดสำหรับเอนทิตี้ที่ล้มเหลวมีอยู่ในตาราง DualWriteProjectConfiguration และ DualWriteProjectFieldConfiguration</span><span class="sxs-lookup"><span data-stu-id="94472-122">Sign in to the Finance and Operations app, and make sure that records for the failing entity exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="94472-123">ตัวอย่างเช่น นี่คือลักษณะของแบบสอบถาม ถ้าเอนทิตี้ **ลูกค้า** ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="94472-123">For example, here is what the query looks like if the **Customers** entity is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="94472-124">ถ้ามีเรกคอร์ดสำหรับเอนทิตี้ที่ล้มเหลว แม้แต่หลังจากที่คุณหยุดการแม็ปเอนทิตี้ ให้ลบเรกคอร์ดที่เกี่ยวข้องกับเอนทิตี้ที่ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="94472-124">If there are records for the failing entity even after you stop the entity mapping, delete the records that are related to the failing entity.</span></span> <span data-ttu-id="94472-125">ทำให้บันทึกของคอลัมน์ **projectname** ในตาราง DualWriteProjectConfiguration และดึงข้อมูลเรกคอร์ดในตาราง DualWriteProjectFieldConfiguration โดยใช้ชื่อโครงการเพื่อลบเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="94472-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the record in the DualWriteProjectFieldConfiguration table by using the project name to delete the record.</span></span>
4. <span data-ttu-id="94472-126">เริ่มต้นการแม็ปเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="94472-126">Start the entity mapping.</span></span> <span data-ttu-id="94472-127">ตรวจสอบว่าข้อมูลถูกซิงค์โดยไม่มีปัญหาใดๆ หรือไม่</span><span class="sxs-lookup"><span data-stu-id="94472-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="94472-128">จัดการข้อผิดพลาดของสิทธิ์ในการอ่านหรือเขียน เมื่อคุณสร้างข้อมูลในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="94472-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="94472-129">คุณอาจได้รับข้อความแสดงข้อผิดพลาด "คำขอไม่ถูกต้อง" ซึ่งคล้ายกับตัวอย่างต่อไปนี้ เมื่อคุณสร้างข้อมูลในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="94472-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![ตัวอย่างของข้อความแสดงข้อผิดพลาด คำขอไม่ถูกต้อง](media/error_record_id_source.png)

<span data-ttu-id="94472-131">เมื่อต้องการแก้ไขปัญหานี้ คุณต้องกำหนดบทบาทความปลอดภัยที่ถูกต้องให้กับทีมงานของหน่วยธุรกิจของ Dynamics 365 Sales หรือ Dynamics 365 Customer Service เพื่อเปิดใช้งานสิทธิ์ที่ขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="94472-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="94472-132">ในแอป Finance and Operations ให้ค้นหาหน่วยธุรกิจที่ถูกแม็ปในชุดการเชื่อมต่อการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="94472-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![การแม็ปองค์กร](media/mapped_business_unit.png)

2. <span data-ttu-id="94472-134">ลงชื่อเข้าใช้ในสภาพแวดล้อมในแอปที่เป็นแบบโมเดลใน Dynamics 365 นำทางไปยัง **การตั้งค่า \> การรักษาความปลอดภัย** และค้นหาทีมงานของหน่วยธุรกิจที่ถูกแม็ป</span><span class="sxs-lookup"><span data-stu-id="94472-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security** , and find the team of the mapped business unit.</span></span>

    ![ทีมงานของหน่วยธุรกิจที่ถูกแม็ป](media/setting_security_page.png)

3. <span data-ttu-id="94472-136">เปิดหน้าสำหรับทีมงานสำหรับการแก้ไข และจากนั้น เลือก **จัดการบทบาท** เพื่อเปิดกล่องโต้ตอบ **จัดการบทบาทของทีมงาน**</span><span class="sxs-lookup"><span data-stu-id="94472-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![ปุ่มจัดการบทบาท](media/manage_team_roles.png)

4. <span data-ttu-id="94472-138">กำหนดบทบาทที่มีสิทธิ์อ่าน/เขียนสำหรับเอนทิตี้ที่เกี่ยวข้อง และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="94472-138">Assign the role that has the read/write privilege for the relevant entities, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a><span data-ttu-id="94472-139">แก้ปัญหาการซิงโครไนส์ในสภาพแวดล้อมที่มีสภาพแวดล้อม Common Data Service ที่มีการเปลี่ยนแปลงล่าสุด</span><span class="sxs-lookup"><span data-stu-id="94472-139">Fix synchronization issues in an environment that has a recently changed Common Data Service environment</span></span>

<span data-ttu-id="94472-140">**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="94472-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="94472-141">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณสร้างข้อมูลในแอป Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="94472-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="94472-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":" **ไม่สามารถสร้างส่วนข้อความสำหรับเอนทิตี้ CustCustomerV3Entity** ","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"การสร้างส่วนข้อความล้มเหลวโดยมีข้อผิดพลาด URI ที่ไม่ถูกต้อง: URI ว่างเปล่า"}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="94472-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":" **Unable to generate payload for entity CustCustomerV3Entity** ","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="94472-143">นี่คือลักษณะของข้อผิดพลาดในแอปที่เป็นแบบโมเดลใน Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="94472-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="94472-144">*เกิดข้อผิดพลาดที่ไม่คาดคิดจากรหัส ISV (ErrorType = ClientError) ข้อยกเว้นที่ไม่คาดคิดจากปลั๊กอิน (ดำเนินการ): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: ล้มเหลวในการประมวลผลบัญชีเอนทิตี้ - (ความพยายามในการเชื่อมต่อล้มเหลว เนื่องจากฝ่ายที่เชื่อมต่อไม่ได้ตอบสนองอย่างถูกต้องหลังจากระยะเวลาหนึ่ง หรือการเชื่อมต่อที่สร้างล้มเหลว เนื่องจากโฮสต์ที่เชื่อมต่อล้มเหลวในการตอบสนอง*</span><span class="sxs-lookup"><span data-stu-id="94472-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="94472-145">ข้อผิดพลาดนี้จะเกิดขึ้นเมื่อสภาพแวดล้อม Common Data Service ถูกรีเซ็ตอย่างไม่ถูกต้องในเวลาเดียวกับที่คุณพยายามที่จะสร้างข้อมูลในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="94472-145">This error occurs when the Common Data Service environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="94472-146">เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="94472-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="94472-147">ลงชื่อเข้าใช้ใน เครื่องเสมือน Finance and Operations (VM) เปิด SQL Server Management STUDIO (SSMS) และค้นหาเรกคอร์ดในตาราง DUALWRITEPROJECTCONFIGURATIONENTITY ที่ซึ่ง **Internalentityname** เท่ากับ **ลูกค้า V3** และ **externalentityname** เท่ากับ **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="94472-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for records in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="94472-148">นี่คือลักษณะของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="94472-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="94472-149">ใช้ชื่อโครงการจากผลลัพธ์ของการสอบถามก่อนหน้านี้ เพื่อรันการสอบถามต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="94472-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="94472-150">ตรวจสอบให้แน่ใจว่าคอลัมน์ **externalenvironmentURL** มี Common Data Service หรือ URL ของแอปที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="94472-150">Make sure that the **externalenvironmentURL** column has the correct Common Data Service or app URL.</span></span> <span data-ttu-id="94472-151">ลบเรกคอร์ดที่ซ้ำกันใดๆ ที่ชี้ไปที่ URL Common Data Service ที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="94472-151">Delete any duplicate records that point to the wrong Common Data Service URL.</span></span> <span data-ttu-id="94472-152">ลบเรกคอร์ดที่สอดคล้องกันในตาราง DUALWRITEPROJECTFIELDCONFIGURATION และ DUALWRITEPROJECTCONFIGURATION</span><span class="sxs-lookup"><span data-stu-id="94472-152">Delete the corresponding records in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="94472-153">หยุดการแม็ปเอนทิตี้ แล้วเริ่มการทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="94472-153">Stop the entity mapping, and then restart it</span></span>
