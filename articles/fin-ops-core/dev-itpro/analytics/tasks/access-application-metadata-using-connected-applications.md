---
title: เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้แอพลิเคชันที่เชื่อมต่อ
description: ขั้นตอนในหัวข้อนี้จะอธิบายวิธีการที่ผู้ใช้ Regulatory configuration service สามารถออกแบบการแม็ปแบบจำลองการรายงานทางอิเล็กทรอนิกส์ใหม่โดยใช้ข้อมูลเมตา
author: NickSelin
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88fb3a947dd15f80238baab5f315c889f47f5b3b
ms.sourcegitcommit: 273903b7b73ac726d447c50f7086e6d8b0f0f74e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087026"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="02da7-103">เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้แอพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="02da7-103">Access application metadata by using connected applications</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02da7-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ Regulatory configuration service (RCS) ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถออกแบบการแม็ปแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) ใหม่ โดยใช้ข้อมูลเมตาใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="02da7-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="02da7-105">จะมีการเข้าถึงข้อมูลเมตาของแอพลิเคชันแบบออนไลน์โดยใช้แอพลิเคชันที่เชื่อมต่อ RCS</span><span class="sxs-lookup"><span data-stu-id="02da7-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="02da7-106">จะมีการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ของตัวอย่างเพื่อเข้าถึงธุรกรรมการค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="02da7-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="02da7-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ใน RCS อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในหัวข้อให้เสร็จสมบูรณ์ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="02da7-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="02da7-108">ถ้าคุณยังไม่ได้ดำเนินการขั้นตอนในหัวข้อให้เสร็จสมบูรณ์ [ให้เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้การตั้งค่าคอนฟิก ER](access-application-metadata-er-configuration.md) ให้ดาวน์โหลด [ตัวอย่างการรายงานทางอิเล็กทรอนิกส์](https://download.microsoft.com/download/0/4/e/04e13839-e423-442b-a6c2-dd35b1045c2d/Dynamics%20365%20for%20Finance%20and%20Operations%208.1%20Electronic%20reporting%20task%20guides.zip) และบันทึกการตั้งค่าคอนฟิก ER ต่อไปนี้: Foreign trade metadata.xml Foreign trade model.xml Foreign trade mapping.xml และจากนั้น ดำเนินการขั้นตอนต่างๆ ในกระบวนงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="02da7-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), download the [Electronic reporting examples](https://download.microsoft.com/download/0/4/e/04e13839-e423-442b-a6c2-dd35b1045c2d/Dynamics%20365%20for%20Finance%20and%20Operations%208.1%20Electronic%20reporting%20task%20guides.zip) and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="02da7-109">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="02da7-109">Prerequisites</span></span>
1. <span data-ttu-id="02da7-110">ไปที่ **พื้นที่ทำงานทั้งหมด** > **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="02da7-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="02da7-111">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และถูกทำเครื่องหมายเป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="02da7-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="02da7-112">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ในกระบวนงาน [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md) ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="02da7-112">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="02da7-113">รับการตั้งค่าคอนฟิก ER ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="02da7-113">Get required ER configurations</span></span>
1. <span data-ttu-id="02da7-114">คลิก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="02da7-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="02da7-115">หากคุณดำเนินการขั้นตอนต่างๆ ในกระบวนงาน [เข้าถึงข้อมูลเมตาของโปรแกรมประยุกต์โดยใช้การตั้งค่าคอนฟิก ER](access-application-metadata-er-configuration.md) เสร็จสมบูรณ์แล้ว คุณมีการตั้งค่าคอนฟิก ER ที่จำเป็นทั้งหมดแล้ว (ข้อมูลเมตาการค้าต่างประเทศ การตั้งค่าคอนฟิกแบบจำลองและการแม็ป) ในอินสแตนซ์ RCS ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="02da7-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="02da7-116">คุณสามารถข้ามขั้นตอนที่เหลือทั้งหมดของงานย่อยนี้ได้</span><span class="sxs-lookup"><span data-stu-id="02da7-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="02da7-117">คลิก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="02da7-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="02da7-118">คลิก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="02da7-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="02da7-119">คลิก **เรียกดู** และเลือกไฟล์ **Foreign trade metadata.xml**</span><span class="sxs-lookup"><span data-stu-id="02da7-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="02da7-120">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="02da7-120">Click **OK**.</span></span> 
7. <span data-ttu-id="02da7-121">คลิก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="02da7-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="02da7-122">คลิก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="02da7-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="02da7-123">คลิก **เรียกดู** และเลือกไฟล์ **Foreign trade model.xml**</span><span class="sxs-lookup"><span data-stu-id="02da7-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="02da7-124">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="02da7-124">Click **OK**.</span></span> 
11. <span data-ttu-id="02da7-125">คลิก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="02da7-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="02da7-126">คลิก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="02da7-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="02da7-127">คลิก **เรียกดู** และเลือกไฟล์ **Foreign trade mapping.xml**</span><span class="sxs-lookup"><span data-stu-id="02da7-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="02da7-128">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="02da7-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="02da7-129">ลงทะเบียนแอพลิเคชันที่เชื่อมต่อแล้ว</span><span class="sxs-lookup"><span data-stu-id="02da7-129">Register a connected application</span></span>
1. <span data-ttu-id="02da7-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="02da7-130">Close the page.</span></span> 
2. <span data-ttu-id="02da7-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="02da7-131">Close the page.</span></span> 
3. <span data-ttu-id="02da7-132">ไปที่ **พื้นที่ทำงานทั้งหมด** > **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="02da7-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="02da7-133">คลิก **แอพลิเคชันที่เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="02da7-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="02da7-134">ตรวจสอบให้แน่ใจว่าแอพลิเคชันที่ได้รับการตั้งค่าคอนฟิกขึ้นอยู่กับ Azure และสามารถเข้าถึงได้สำหรับผู้ใช้ RCS ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="02da7-134">Make sure that the configured application is Azure based and accessible for the current RCS user.</span></span> <span data-ttu-id="02da7-135">นอกจากนี้ คุณต้องระบุว่าผู้ใช้ RCS ปัจจุบันมีสิทธิ์เข้าถึงแอพลิเคชันที่เลือก และได้รับการลงทะเบียนเป็นผู้ใช้ของแอพลิเคชันนี้ในการเล่นบทบาทที่ให้สิทธิ์พวกเขาในการเข้าถึงข้อมูลเมตาของแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="02da7-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving them privileges to access application's metadata.</span></span> 
6. <span data-ttu-id="02da7-136">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="02da7-136">Click **New**.</span></span> 
7. <span data-ttu-id="02da7-137">ในฟิลด์ **ชื่อ** พิมพ์ 'MyConnectedApp'</span><span class="sxs-lookup"><span data-stu-id="02da7-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="02da7-138">ในฟิลด์ **แอพลิเคชัน** ให้พิมพ์ 'https:// mycompany.operations.dynamics.com '</span><span class="sxs-lookup"><span data-stu-id="02da7-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="02da7-139">ในฟิลด์ **ผู้เช่า** ให้พิมพ์ 'mycompany.onmicrosoft.com'</span><span class="sxs-lookup"><span data-stu-id="02da7-139">In the **Tenant** field, type 'mycompany.onmicrosoft.com'.</span></span> 
10. <span data-ttu-id="02da7-140">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="02da7-140">Click **Save**.</span></span> 
11. <span data-ttu-id="02da7-141">เมื่อคุณตรวจสอบการเชื่อมต่อกับแอพลิเคชันที่ตั้งค่าคอนฟิก บนหน้า **เชื่อมต่อกับแอพลิเคชันระยะไกล** คลิกที่ลิงค์ **คลิกที่นี่เพื่อเชื่อมต่อกับแอพลิเคชันระยะไกลที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="02da7-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="02da7-142">คลิก **ตรวจสอบการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="02da7-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="02da7-143">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="02da7-143">Click **Close**.</span></span> 
14. <span data-ttu-id="02da7-144">เมื่อการตรวจสอบความถูกต้องของการเชื่อมต่อเสร็จเรียบร้อยแล้ว จะมีการปรับปรุงรายการรายละเอียดรุ่นและผู้เช่าสำหรับแอพลิเคชันที่ตั้งค่าคอนฟิกในกริดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="02da7-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="02da7-145">ตรวจทานการตั้งค่าคอนฟิกการแม็ปแบบจำลองที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="02da7-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="02da7-146">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="02da7-146">Close the page.</span></span> 
2. <span data-ttu-id="02da7-147">คลิก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="02da7-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="02da7-148">ในแผนภูมิ ขยาย **แบบจำลองการค้าต่างประเทศ**</span><span class="sxs-lookup"><span data-stu-id="02da7-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="02da7-149">ในแผนภูมิ ให้เลือก **แบบจำลองการค้าต่างประเทศ\การแม็ปการค้าต่างประเทศ**</span><span class="sxs-lookup"><span data-stu-id="02da7-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="02da7-150">ขยายส่วน **ข้อกำหนดเบื้องต้น**</span><span class="sxs-lookup"><span data-stu-id="02da7-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="02da7-151">ในขณะนี้ การแม็ปนี้อ้างอิงถึงการตั้งค่าคอนฟิกข้อมูลเมตา</span><span class="sxs-lookup"><span data-stu-id="02da7-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="02da7-152">ข้อมูลเมตาของแอพลิเคชันจากการตั้งค่าคอนฟิกนี้จะถูกนำเสนอ ในขณะที่การแม็ปแบบจำลองนี้จะถูกออกแบบ</span><span class="sxs-lookup"><span data-stu-id="02da7-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="02da7-153">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="02da7-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="02da7-154">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="02da7-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="02da7-155">ในแผนภูมิ ให้เลือก **Dynamics 365 for Operations\เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="02da7-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="02da7-156">คลิก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="02da7-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="02da7-157">ในฟิลด์ **ตาราง** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="02da7-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="02da7-158">ในขณะนี้ การแม็ปนี้อ้างอิงถึงการตั้งค่าคอนฟิกข้อมูลเมตา</span><span class="sxs-lookup"><span data-stu-id="02da7-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="02da7-159">ข้อมูลเมตาของแอพลิเคชันจากการตั้งค่าคอนฟิกนี้จะถูกนำเสนอ ในขณะที่การแม็ปแบบจำลองนี้จะถูกออกแบบ</span><span class="sxs-lookup"><span data-stu-id="02da7-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="02da7-160">คลิก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="02da7-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="02da7-161">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="02da7-161">Close the page.</span></span> 
13. <span data-ttu-id="02da7-162">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="02da7-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="02da7-163">กำหนดแอพลิเคชันที่เชื่อมโยงให้กับการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="02da7-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="02da7-164">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="02da7-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="02da7-165">เลือกแอพลิเคชัน **MyConnectedApp**</span><span class="sxs-lookup"><span data-stu-id="02da7-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="02da7-166">ในปัจจุบัน การแม็ปนี้อ้างอิงถึงข้อมูลเมตาของแอพลิเคชันที่เชื่อมต่อที่เลือก</span><span class="sxs-lookup"><span data-stu-id="02da7-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="02da7-167">เมื่อการแม็ปเดียวกันอ้างอิงถึงการตั้งค่าคอนฟิกข้อมูลเมตาและแอพลิเคชันที่เชื่อมต่อในเวลาเดียวกัน จะมีการใช้ข้อมูลเมตาของแอพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="02da7-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="02da7-168">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="02da7-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="02da7-169">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="02da7-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="02da7-170">ในแผนภูมิ ให้เลือก **Dynamics 365 for Operations\เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="02da7-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="02da7-171">คลิก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="02da7-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="02da7-172">ในฟิลด์ **ตาราง** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="02da7-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="02da7-173">มีการนำเสนอตารางแอพลิเคชันมากกว่าสองตารางในขณะนี้ เนื่องจากการแม็ปนี้ใช้ข้อมูลเมตาของแอพลิเคชันที่เชื่อมต่อทั้งหมดที่ได้รับการกำหนดไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="02da7-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="02da7-174">คลิก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="02da7-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="02da7-175">คลิก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="02da7-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="02da7-176">เราประสบความสำเร็จในการผูกองค์ประกอบของแบบจำลองข้อมูลกับรายการของแหล่งข้อมูลที่อธิบาย โดยใช้รายละเอียดของข้อมูลเมตาของแอพลิเคชันที่เชื่อมต่อซึ่งได้รับการกำหนดสำหรับการแม็ปนี้</span><span class="sxs-lookup"><span data-stu-id="02da7-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="02da7-177">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="02da7-177">Close the page.</span></span> 
11. <span data-ttu-id="02da7-178">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="02da7-178">Close the page.</span></span> 

<span data-ttu-id="02da7-179">เมื่อคุณต้องการประเมินการแม็ปแบบจำลองนี้โดยใช้ข้อมูลเมตาของแอพลิเคชันรุ่นอื่น ลงทะเบียนแอพลิเคชันอื่นที่เชื่อมต่อ กำหนดให้กับการแม็ปแบบจำลองนี้ และตรวจสอบความถูกต้องเทียบกับข้อมูลเมตาใหม่</span><span class="sxs-lookup"><span data-stu-id="02da7-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
