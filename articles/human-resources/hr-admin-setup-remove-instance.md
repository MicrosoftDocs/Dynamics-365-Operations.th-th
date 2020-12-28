---
title: เอาอินสแตนซ์ออก
description: บทความนี้นำคุณไปสู่กระบวนการในการลบ Test Drive หรือสภาพแวดล้อมการผลิตสำหรับ Microsoft Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0a8eac74f0d840251ab56445dd5af4d19d3c0490
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420799"
---
# <a name="remove-an-instance"></a><span data-ttu-id="4ced9-103">เอาอินสแตนซ์ออก</span><span class="sxs-lookup"><span data-stu-id="4ced9-103">Remove an instance</span></span>

<span data-ttu-id="4ced9-104">บทความนี้นำคุณไปสู่กระบวนการในการลบ Test Drive หรือสภาพแวดล้อมการผลิตสำหรับ Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="4ced9-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="4ced9-105">เอาสภาพแวดล้อมไดรฟ์ทดสอบออก</span><span class="sxs-lookup"><span data-stu-id="4ced9-105">Remove a test drive environment</span></span>

<span data-ttu-id="4ced9-106">ไดรฟ์ทดสอบทรัพยากรบุคคลถูกเตรียมใช้งานโดยมีนโยบายการหมดอายุ 60 วัน</span><span class="sxs-lookup"><span data-stu-id="4ced9-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="4ced9-107">อย่างไรก็ตาม เจ้าของสภาพแวดล้อมไดรฟ์ทดสอบมีตัวเลือกในการสิ้นสุดการทดลองของพวกเขาก่อนเวลา โดยดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4ced9-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="4ced9-108">นำทางไปยัง [ศูนย์การจัดการ Power Apps](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="4ced9-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="4ced9-109">เลือก **สภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="4ced9-109">Select **Environments**.</span></span>
3. <span data-ttu-id="4ced9-110">เลือกสภาพแวดล้อม Test Drive ซึ่งมีรูปแบบการตั้งชื่อที่คล้ายกับรายการนี้: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="4ced9-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="4ced9-111">เลือก **ลบ** และยืนยันการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="4ced9-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="4ced9-112">สภาพแวดล้อมไดรฟ์ทดสอบที่มีอยู่จะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="4ced9-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="4ced9-113">เมื่อถูกลบออก คุณสามารถลงชื่อสมัครสภาพแวดล้อมไดรฟ์ทดสอบใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="4ced9-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="4ced9-114">เอาสภาพแวดล้อมการผลิตออก</span><span class="sxs-lookup"><span data-stu-id="4ced9-114">Remove a production environment</span></span>

<span data-ttu-id="4ced9-115">บทความนี้สันนิษฐานว่า คุณได้ซื้อทรัพยากรบุคคลผ่านผู้ให้บริการโซลูชัน Cloud (CSP) หรือข้อตกลงสถาปัตยกรรมองค์กร (EA)</span><span class="sxs-lookup"><span data-stu-id="4ced9-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="4ced9-116">เนื่องจากสภาพแวดล้อมทรัพยากรบุคคลเดียวถูก"บรรจุ"อยู่ภายในสภาพแวดล้อม Power Apps เดียวซึ่งคุณมีตัวเลือกสองตัวที่ควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="4ced9-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="4ced9-117">ตัวเลือกแรกเกี่ยวข้องกับการลบสภาพแวดล้อม Power Apps ทั้งหมด; ตัวเลือกที่สองเกี่ยวข้องกับการลบเฉพาะทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4ced9-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="4ced9-118">ตัวเลือกแรกเป็นที่ต้องการเมื่อคุณได้สร้างสภาพแวดล้อม Power Apps อย่างชัดเจนสำหรับวัตถุประสงค์ในการเตรียมใช้งานทรัพยากรบุคคล และคุณเพียงพึ่งเริ่มใช้งานหรือคุณไม่มีการรวมใดๆที่สร้างไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="4ced9-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="4ced9-119">ตัวเลือกที่สองจะเหมาะสมก็ต่อเมื่อคุณได้มีสภาพแวดล้อม Power Apps ที่สร้างไว้แล้วซึ่งเต็มไปด้วยข้อมูลที่หลากหลายที่ถูกยกระดับใน Power Apps และ Power Automate</span><span class="sxs-lookup"><span data-stu-id="4ced9-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="4ced9-120">ก่อนที่จะลบสภาพแวดล้อม Power Apps คุณต้องแน่ใจว่าจะไม่มีการใช้สำหรับการรวมข้อมูลที่หลากหลายภายนอกขอบเขตของทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4ced9-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="4ced9-121">นอกจากนี้โปรดทราบว่าค่าเริ่มต้นของสภาพแวดล้อม Power Apps ไม่สามารถลบได้</span><span class="sxs-lookup"><span data-stu-id="4ced9-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="4ced9-122">ในการลบสภาพแวดล้อม Power Apps ทั้งหมดซึ่งรวมถึงทรัพยากรบุคคล และแอปและขั้นตอนที่เชื่อมโยง:</span><span class="sxs-lookup"><span data-stu-id="4ced9-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="4ced9-123">นำทางไปยัง [ศูนย์การจัดการ Power Apps](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="4ced9-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="4ced9-124">เลือก **สภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="4ced9-124">Select **Environments**.</span></span>
3. <span data-ttu-id="4ced9-125">เลือกสภาพแวดล้อมที่จะถูกลบ</span><span class="sxs-lookup"><span data-stu-id="4ced9-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="4ced9-126">เลือก **ลบ** และยืนยันการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="4ced9-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="4ced9-127">โปรดรอจนกว่าการลบข้อมูลจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4ced9-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="4ced9-128">ลงชื่อเข้าใช้ [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) โดยใช้บัญชีที่คุณใช้ในการสมัครสมาชิกทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4ced9-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="4ced9-129">เลือกโครงการทรัพยากรบุคคลที่ประกอบด้วยสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="4ced9-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="4ced9-130">ในโครงการ LCS ของคุณ เลือกไทล์ **การจัดการแอป Human Resources**</span><span class="sxs-lookup"><span data-stu-id="4ced9-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="4ced9-131">เลือกอินสแตนซ์ที่จะลบ</span><span class="sxs-lookup"><span data-stu-id="4ced9-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="4ced9-132">เลือก **ลบอินสแตนซ์** และยืนยันการตัดสินใจของคุณ</span><span class="sxs-lookup"><span data-stu-id="4ced9-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="4ced9-133">ในการลบสภาพแวดล้อมทรัพยากรบุคคลจากสภาพแวดล้อม Power Apps ที่มีอยู่ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4ced9-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="4ced9-134">โปรดทราบว่า ความจำเป็นในการเกี่ยวข้องกับการสนับสนุน และการติดต่อทีม DevOps ทรัพยากรบุคคลเป็นแบบชั่วคราว จนกว่าจะมีการเปิดใช้งานคุณลักษณะนี้โดยตรงใน LCS</span><span class="sxs-lookup"><span data-stu-id="4ced9-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="4ced9-135">โปรดติดต่อฝ่ายสนับสนุนเพื่อเริ่มต้นคำขอการลบ</span><span class="sxs-lookup"><span data-stu-id="4ced9-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="4ced9-136">ทีมสนับสนุนจะเริ่มต้นคำขอการลบด้วยทีม DevOps ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4ced9-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="4ced9-137">ดำเนินการต่อ หลังจากที่คุณได้รับคำที่ว่าสภาพแวดล้อมได้ถูกลบออกแล้ว</span><span class="sxs-lookup"><span data-stu-id="4ced9-137">Continue after you receive word that the environment has been removed.</span></span>
4. <span data-ttu-id="4ced9-138">ลงชื่อเข้าใช้ LCS โดยใช้บัญชีที่คุณใช้ในการสมัครสมาชิกทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4ced9-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="4ced9-139">เลือกโครงการทรัพยากรบุคคลที่ประกอบด้วยสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="4ced9-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="4ced9-140">ในโครงการ LCS ของคุณ เลือกไทล์ **การจัดการแอป Human Resources**</span><span class="sxs-lookup"><span data-stu-id="4ced9-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="4ced9-141">เลือกอินสแตนซ์ที่คุณต้องการลบ ซึ่งควรทำเครื่องหมายไว้ด้วยสถานะการปรับใช้เป็น **ถูกลบ**</span><span class="sxs-lookup"><span data-stu-id="4ced9-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Deleted**.</span></span>
8. <span data-ttu-id="4ced9-142">เลือก **ลบอินสแตนซ์** และยืนยันการตัดสินใจของคุณ</span><span class="sxs-lookup"><span data-stu-id="4ced9-142">Select **Remove instance** and confirm your decision.</span></span> 

## <a name="recover-a-soft-deleted-environment"></a><span data-ttu-id="4ced9-143">การกู้คืนสภาพแวดล้อมที่ถูกลบแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="4ced9-143">Recover a soft-deleted environment</span></span>

<span data-ttu-id="4ced9-144">ถ้าคุณลบสภาพแวดล้อม Power Apps ที่มีการเชื่อมต่อกับสภาพแวดล้อมของทรัพยากรบุคคล สถานะของสภาพแวดล้อมของทรัพยากรบุคคลใน Lifecycle Services จะถูก **ลบชั่วคราว**</span><span class="sxs-lookup"><span data-stu-id="4ced9-144">If you delete the Power Apps environment that your Human Resources environment is connected to, the status of the Human Resources environment in Lifecycle Services will be **Soft deleted**.</span></span> <span data-ttu-id="4ced9-145">ในกรณีนี้ ผู้ใช้ไม่สามารถเชื่อมต่อกับทรัพยากรบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="4ced9-145">In this case, users can't connect to Human Resources.</span></span>

<span data-ttu-id="4ced9-146">เมื่อต้องการคืนสภาพแวดล้อมให้ปฏิบัติดังนี้:</span><span class="sxs-lookup"><span data-stu-id="4ced9-146">To restore the environment:</span></span>

1. <span data-ttu-id="4ced9-147">ทำตามคำแนะนำในหน้าต่าง [คืนค่าสภาพแวดล้อม Power Apps](/power-platform/admin/recover-environment.md)</span><span class="sxs-lookup"><span data-stu-id="4ced9-147">Follow the instructions in [Recover the Power Apps environment](/power-platform/admin/recover-environment.md).</span></span>

2. <span data-ttu-id="4ced9-148">โปรดติดต่อฝ่ายสนับสนุนเพื่อคืนสภาพแวดล้อมของทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4ced9-148">Contact Support to restore the Human Resources environment.</span></span> <span data-ttu-id="4ced9-149">สำหรับข้อมูลเพิ่มเติม ดู [รับการสนับสนุน](hr-admin-troubleshooting-support.md)</span><span class="sxs-lookup"><span data-stu-id="4ced9-149">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

> [!Warning]
> <span data-ttu-id="4ced9-150">สภาพแวดล้อม Power Apps จะถูกบันทึกไว้เป็นเวลาเจ็ดวันหลังจากลบ</span><span class="sxs-lookup"><span data-stu-id="4ced9-150">Power Apps environments are only saved for seven days after deletion.</span></span> <span data-ttu-id="4ced9-151">คุณต้องกู้คืนสภาพแวดล้อมภายในรอบระยะเวลาเจ็ดวัน</span><span class="sxs-lookup"><span data-stu-id="4ced9-151">You must recover the environment within the seven day period.</span></span>
