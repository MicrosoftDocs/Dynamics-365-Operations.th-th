---
title: แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง
description: หัวข้อนี้แสดงข้อมูลการแก้ไขปัญหาที่สามารถช่วยคุณแก้ไขปัญหาเกี่ยวกับการซิงโครไนส์ที่เริ่มใช้งานจริง
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1c0dfebb3ef442f67d8489d7aed00305c02cf410
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748908"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="99c4e-103">แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="99c4e-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="99c4e-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="99c4e-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="99c4e-105">กล่าวคือ จะแสดงข้อมูลที่สามารถช่วยคุณแก้ไขปัญหาเกี่ยวกับการซิงโครไนส์ที่เริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="99c4e-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99c4e-106">ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="99c4e-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="99c4e-107">ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="99c4e-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="99c4e-108">การซิงโครไนส์ที่เริ่มใช้งานจริงแสดงข้อผิดพลาด 403 ไม่ได้รับอนุญาต เมื่อคุณสร้างแถวในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="99c4e-108">Live synchronization throws a 403 Forbidden error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="99c4e-109">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณสร้างแถวในแอป Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="99c4e-109">You might receive the following error message when you create a row in a Finance and Operations app:</span></span>

<span data-ttu-id="99c4e-110">*\[{\\"ข้อผิดพลาด\\":{\\"รหัส\\":\\"0x80072560\\",\\"ข้อความ\\":\\"ผู้ใช้ไม่ใช่สมาชิกขององค์กร\\"}}\] เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (403) ไม่ได้รับอนุญาต"}}"*</span><span class="sxs-lookup"><span data-stu-id="99c4e-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="99c4e-111">เมื่อต้องการแก้ไขปัญหานี้ ให้ทำตามขั้นตอนใน [ข้อกำหนดของระบบและข้อกำหนดเบื้องต้น](requirements-and-prerequisites.md)</span><span class="sxs-lookup"><span data-stu-id="99c4e-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="99c4e-112">เมื่อต้องการดำเนินการตามขั้นตอนดังกล่าวให้เสร็จสมบูรณ์ ผู้ใช้แอพลิเคชันการรวมแบบสองทิศทางที่สร้างขึ้นใน Dataverse ต้องมีบทบาทผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="99c4e-112">To complete those steps, the dual-write application users who are created in Dataverse must have the system admin role.</span></span> <span data-ttu-id="99c4e-113">นอกจากนี้ ทีมงานที่เป็นเจ้าของเริ่มต้นต้องมีบทบาทผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="99c4e-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="99c4e-114">การซิงโครไนส์ที่เริ่มใช้งานจริงสำหรับตารางใดๆ แสดงข้อผิดพลาดที่คล้ายกันอย่างสม่ำเสมอ เมื่อคุณสร้างแถวในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="99c4e-114">Live synchronization for any table consistently throws a similar error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="99c4e-115">**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="99c4e-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="99c4e-116">คุณอาจได้รับข้อความแสดงข้อผิดพลาดเช่นต่อไปนี้ทุกครั้งที่คุณพยายามบันทึกข้อมูลตารางในแอป Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="99c4e-116">You might receive an error message like the following every time that you try to save table data in a Finance and Operations app:</span></span>

<span data-ttu-id="99c4e-117">*ไม่สามารถบันทึกการเปลี่ยนแปลงไปยังฐานข้อมูล หน่วยของงานไม่สามารถส่งธุรกรรมได้ ไม่สามารถเขียนข้อมูลไปยังเอนทิตี้ uoms ได้ เขียนไปยัง UnitOfMeasureEntity ล้มเหลว โดยมีข้อความแสดงข้อผิดพลาดว่า ไม่สามารถซิงค์กับเอนทิตี้ uoms ได้*</span><span class="sxs-lookup"><span data-stu-id="99c4e-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="99c4e-118">เมื่อต้องการแก้ไขปัญหานี้ คุณต้องตรวจสอบให้แน่ใจว่ามีข้อมูลอ้างอิงของข้อกำหนดเบื้องต้นอยู่ในทั้งแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="99c4e-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Dataverse.</span></span> <span data-ttu-id="99c4e-119">ตัวอย่างเช่น ถ้าลูกค้าที่คุณอยู่ในแอป Finance and Operations เป็นของกลุ่มลูกค้าหนึ่งๆ โปรดตรวจสอบให้แน่ใจว่ามีกลุ่มลูกค้าอยู่ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="99c4e-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Dataverse.</span></span>

<span data-ttu-id="99c4e-120">ถ้ามีข้อมูลอยู่ในทั้งสองด้าน และคุณยืนยันว่าปัญหานี้ไม่เกี่ยวข้องกับข้อมูล ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="99c4e-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="99c4e-121">หยุดตารางที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="99c4e-121">Stop the related table.</span></span>
2. <span data-ttu-id="99c4e-122">ลงชื่อเข้าใช้ในแอป Finance and Operations และตรวจสอบให้แน่ใจว่ามีแถวสำหรับตารางที่ล้มเหลวอยู่ในตาราง DualWriteProjectConfiguration และตาราง DualWriteProjectFieldConfiguration</span><span class="sxs-lookup"><span data-stu-id="99c4e-122">Sign in to the Finance and Operations app, and make sure that rows for the failing table exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="99c4e-123">ตัวอย่างเช่น นี่คือลักษณะของแบบสอบถาม ถ้าตาราง **ลูกค้า** ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="99c4e-123">For example, here is what the query looks like if the **Customers** table is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="99c4e-124">ถ้ามีแถวสำหรับตารางที่ล้มเหลว แม้แต่หลังจากที่คุณหยุดการแม็ปตาราง ให้ลบแถวที่เกี่ยวข้องกับตารางที่ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="99c4e-124">If there are rows for the failing table even after you stop the table mapping, delete the rows that are related to the failing table.</span></span> <span data-ttu-id="99c4e-125">ทำให้บันทึกของคอลัมน์ **projectname** ในตาราง DualWriteProjectConfiguration และดึงข้อมูลแถวในตาราง DualWriteProjectFieldConfiguration โดยใช้ชื่อโครงการเพื่อลบแถว</span><span class="sxs-lookup"><span data-stu-id="99c4e-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the row in the DualWriteProjectFieldConfiguration table by using the project name to delete the row.</span></span>
4. <span data-ttu-id="99c4e-126">เริ่มต้นการแม็ปตาราง</span><span class="sxs-lookup"><span data-stu-id="99c4e-126">Start the table mapping.</span></span> <span data-ttu-id="99c4e-127">ตรวจสอบว่าข้อมูลถูกซิงค์โดยไม่มีปัญหาใดๆ หรือไม่</span><span class="sxs-lookup"><span data-stu-id="99c4e-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="99c4e-128">จัดการข้อผิดพลาดของสิทธิ์ในการอ่านหรือเขียน เมื่อคุณสร้างข้อมูลในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="99c4e-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="99c4e-129">คุณอาจได้รับข้อความแสดงข้อผิดพลาด "คำขอไม่ถูกต้อง" ซึ่งคล้ายกับตัวอย่างต่อไปนี้ เมื่อคุณสร้างข้อมูลในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="99c4e-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![ตัวอย่างของข้อความแสดงข้อผิดพลาด คำขอไม่ถูกต้อง](media/error_record_id_source.png)

<span data-ttu-id="99c4e-131">เมื่อต้องการแก้ไขปัญหานี้ คุณต้องกำหนดบทบาทความปลอดภัยที่ถูกต้องให้กับทีมงานของหน่วยธุรกิจของ Dynamics 365 Sales หรือ Dynamics 365 Customer Service เพื่อเปิดใช้งานสิทธิ์ที่ขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="99c4e-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="99c4e-132">ในแอป Finance and Operations ให้ค้นหาหน่วยธุรกิจที่ถูกแม็ปในชุดการเชื่อมต่อการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="99c4e-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![การแม็ปองค์กร](media/mapped_business_unit.png)

2. <span data-ttu-id="99c4e-134">ลงชื่อเข้าใช้ในสภาพแวดล้อมในแอปที่เป็นแบบโมเดลใน Dynamics 365 นำทางไปยัง **การตั้งค่า \> การรักษาความปลอดภัย** และค้นหาทีมงานของหน่วยธุรกิจที่ถูกแม็ป</span><span class="sxs-lookup"><span data-stu-id="99c4e-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![ทีมงานของหน่วยธุรกิจที่ถูกแม็ป](media/setting_security_page.png)

3. <span data-ttu-id="99c4e-136">เปิดหน้าสำหรับทีมงานสำหรับการแก้ไข และจากนั้น เลือก **จัดการบทบาท** เพื่อเปิดกล่องโต้ตอบ **จัดการบทบาทของทีมงาน**</span><span class="sxs-lookup"><span data-stu-id="99c4e-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![ปุ่มจัดการบทบาท](media/manage_team_roles.png)

4. <span data-ttu-id="99c4e-138">กำหนดบทบาทที่มีสิทธิ์อ่าน/เขียนสำหรับตารางที่เกี่ยวข้อง และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="99c4e-138">Assign the role that has the read/write privilege for the relevant tables, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a><span data-ttu-id="99c4e-139">แก้ปัญหาการซิงโครไนส์ในสภาพแวดล้อมที่มีสภาพแวดล้อม Dataverse ที่มีการเปลี่ยนแปลงล่าสุด</span><span class="sxs-lookup"><span data-stu-id="99c4e-139">Fix synchronization issues in an environment that has a recently changed Dataverse environment</span></span>

<span data-ttu-id="99c4e-140">**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="99c4e-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="99c4e-141">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณสร้างข้อมูลในแอป Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="99c4e-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="99c4e-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**ไม่สามารถสร้างส่วนข้อความสำหรับเอนทิตี้ CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"การสร้างส่วนข้อความล้มเหลวโดยมีข้อผิดพลาด URI ที่ไม่ถูกต้อง: URI ว่างเปล่า"}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="99c4e-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="99c4e-143">นี่คือลักษณะของข้อผิดพลาดในแอปที่เป็นแบบโมเดลใน Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="99c4e-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="99c4e-144">*เกิดข้อผิดพลาดที่ไม่คาดคิดจากรหัส ISV (ErrorType = ClientError) ข้อยกเว้นที่ไม่คาดคิดจากปลั๊กอิน (ดำเนินการ): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: ล้มเหลวในการประมวลผลบัญชีเอนทิตี้ - (ความพยายามในการเชื่อมต่อล้มเหลว เนื่องจากฝ่ายที่เชื่อมต่อไม่ได้ตอบสนองอย่างถูกต้องหลังจากระยะเวลาหนึ่ง หรือการเชื่อมต่อที่สร้างล้มเหลว เนื่องจากโฮสต์ที่เชื่อมต่อล้มเหลวในการตอบสนอง*</span><span class="sxs-lookup"><span data-stu-id="99c4e-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="99c4e-145">ข้อผิดพลาดนี้จะเกิดขึ้นเมื่อสภาพแวดล้อม Dataverse ถูกรีเซ็ตอย่างไม่ถูกต้องในเวลาเดียวกับที่คุณพยายามที่จะสร้างข้อมูลในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="99c4e-145">This error occurs when the Dataverse environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="99c4e-146">เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="99c4e-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="99c4e-147">ลงชื่อเข้าใช้ใน เครื่องเสมือน Finance and Operations (VM) เปิด SQL Server Management STUDIO (SSMS) และค้นหาแถวในตาราง DUALWRITEPROJECTCONFIGURATIONENTITY ที่ซึ่ง **Internalentityname** เท่ากับ **ลูกค้า V3** และ **externalentityname** เท่ากับ **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="99c4e-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for rows in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="99c4e-148">นี่คือลักษณะของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="99c4e-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="99c4e-149">ใช้ชื่อโครงการจากผลลัพธ์ของการสอบถามก่อนหน้านี้ เพื่อรันการสอบถามต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="99c4e-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="99c4e-150">ตรวจสอบให้แน่ใจว่าคอลัมน์ **externalenvironmentURL** มี Dataverse หรือ URL ของแอปที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="99c4e-150">Make sure that the **externalenvironmentURL** column has the correct Dataverse or app URL.</span></span> <span data-ttu-id="99c4e-151">ลบแถวที่ซ้ำกันใดๆ ที่ชี้ไปที่ URL Dataverse ที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="99c4e-151">Delete any duplicate rows that point to the wrong Dataverse URL.</span></span> <span data-ttu-id="99c4e-152">ลบแถวที่สอดคล้องกันในตาราง DUALWRITEPROJECTFIELDCONFIGURATION และ DUALWRITEPROJECTCONFIGURATION</span><span class="sxs-lookup"><span data-stu-id="99c4e-152">Delete the corresponding rows in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="99c4e-153">หยุดการแม็ปตาราง แล้วเริ่มการทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="99c4e-153">Stop the table mapping, and then restart it</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]