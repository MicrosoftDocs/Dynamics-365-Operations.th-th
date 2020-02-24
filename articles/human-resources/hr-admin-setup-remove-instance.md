---
title: เอาอินสแตนซ์ออก
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010683"
---
# <a name="remove-an-instance"></a><span data-ttu-id="b1261-102">เอาอินสแตนซ์ออก</span><span class="sxs-lookup"><span data-stu-id="b1261-102">Remove an instance</span></span>

<span data-ttu-id="b1261-103">บทความนี้นำคุณไปสู่กระบวนการในการลบ Test Drive หรือสภาพแวดล้อมการผลิตสำหรับ Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="b1261-103">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="b1261-104">เอาสภาพแวดล้อมไดรฟ์ทดสอบออก</span><span class="sxs-lookup"><span data-stu-id="b1261-104">Remove a test drive environment</span></span>

<span data-ttu-id="b1261-105">ไดรฟ์ทดสอบทรัพยากรบุคคลถูกเตรียมใช้งานโดยมีนโยบายการหมดอายุ 60 วัน</span><span class="sxs-lookup"><span data-stu-id="b1261-105">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="b1261-106">อย่างไรก็ตาม เจ้าของสภาพแวดล้อมไดรฟ์ทดสอบมีตัวเลือกในการสิ้นสุดการทดลองของพวกเขาก่อนเวลา โดยดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b1261-106">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="b1261-107">นำทางไปยัง [ศูนย์การจัดการ Power Apps](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="b1261-107">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="b1261-108">เลือก **สภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="b1261-108">Select **Environments**.</span></span>
3. <span data-ttu-id="b1261-109">เลือกสภาพแวดล้อม Test Drive ซึ่งมีรูปแบบการตั้งชื่อที่คล้ายกับรายการนี้: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="b1261-109">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="b1261-110">เลือก **ลบ** และยืนยันการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="b1261-110">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="b1261-111">สภาพแวดล้อมไดรฟ์ทดสอบที่มีอยู่จะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="b1261-111">The existing test drive environment will be removed.</span></span> <span data-ttu-id="b1261-112">เมื่อถูกลบออก คุณสามารถลงชื่อสมัครสภาพแวดล้อมไดรฟ์ทดสอบใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="b1261-112">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="b1261-113">เอาสภาพแวดล้อมการผลิตออก</span><span class="sxs-lookup"><span data-stu-id="b1261-113">Remove a production environment</span></span>

<span data-ttu-id="b1261-114">บทความนี้สันนิษฐานว่า คุณได้ซื้อทรัพยากรบุคคลผ่านผู้ให้บริการโซลูชัน Cloud (CSP) หรือข้อตกลงสถาปัตยกรรมองค์กร (EA)</span><span class="sxs-lookup"><span data-stu-id="b1261-114">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="b1261-115">เนื่องจากสภาพแวดล้อมทรัพยากรบุคคลเดียวถูก"บรรจุ"อยู่ภายในสภาพแวดล้อม Power Apps เดียวซึ่งคุณมีตัวเลือกสองตัวที่ควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="b1261-115">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="b1261-116">ตัวเลือกแรกเกี่ยวข้องกับการลบสภาพแวดล้อม Power Apps ทั้งหมด; ตัวเลือกที่สองเกี่ยวข้องกับการลบเฉพาะทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="b1261-116">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="b1261-117">ตัวเลือกแรกเป็นที่ต้องการเมื่อคุณได้สร้างสภาพแวดล้อม Power Apps อย่างชัดเจนสำหรับวัตถุประสงค์ในการเตรียมใช้งานทรัพยากรบุคคล และคุณเพียงพึ่งเริ่มใช้งานหรือคุณไม่มีการรวมใดๆที่สร้างไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="b1261-117">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="b1261-118">ตัวเลือกที่สองจะเหมาะสมก็ต่อเมื่อคุณได้มีสภาพแวดล้อม Power Apps ที่สร้างไว้แล้วซึ่งเต็มไปด้วยข้อมูลที่หลากหลายที่ถูกยกระดับใน Power Apps และ Power Automate</span><span class="sxs-lookup"><span data-stu-id="b1261-118">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="b1261-119">ก่อนที่จะลบสภาพแวดล้อม Power Apps คุณต้องแน่ใจว่าจะไม่มีการใช้สำหรับการรวมข้อมูลที่หลากหลายภายนอกขอบเขตของทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="b1261-119">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="b1261-120">นอกจากนี้โปรดทราบว่าค่าเริ่มต้นของสภาพแวดล้อม Power Apps ไม่สามารถลบได้</span><span class="sxs-lookup"><span data-stu-id="b1261-120">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="b1261-121">ในการลบสภาพแวดล้อม Power Apps ทั้งหมดซึ่งรวมถึงทรัพยากรบุคคล และแอปและขั้นตอนที่เชื่อมโยง:</span><span class="sxs-lookup"><span data-stu-id="b1261-121">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="b1261-122">นำทางไปยัง [ศูนย์การจัดการ Power Apps](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="b1261-122">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="b1261-123">เลือก **สภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="b1261-123">Select **Environments**.</span></span>
3. <span data-ttu-id="b1261-124">เลือกสภาพแวดล้อมที่จะถูกลบ</span><span class="sxs-lookup"><span data-stu-id="b1261-124">Select the environment to be removed.</span></span>
4. <span data-ttu-id="b1261-125">เลือก **ลบ** และยืนยันการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="b1261-125">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="b1261-126">โปรดรอจนกว่าการลบข้อมูลจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b1261-126">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="b1261-127">ลงชื่อเข้าใช้ [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) โดยใช้บัญชีที่คุณใช้ในการสมัครสมาชิกทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="b1261-127">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="b1261-128">เลือกโครงการทรัพยากรบุคคลที่ประกอบด้วยสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="b1261-128">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="b1261-129">ในโครงการ LCS ของคุณ เลือกไทล์ **การจัดการแอป Human Resources**</span><span class="sxs-lookup"><span data-stu-id="b1261-129">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="b1261-130">เลือกอินสแตนซ์ที่จะลบ</span><span class="sxs-lookup"><span data-stu-id="b1261-130">Select the instance to remove.</span></span> 
10. <span data-ttu-id="b1261-131">เลือก **ลบอินสแตนซ์** และยืนยันการตัดสินใจของคุณ</span><span class="sxs-lookup"><span data-stu-id="b1261-131">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="b1261-132">ในการลบสภาพแวดล้อมทรัพยากรบุคคลจากสภาพแวดล้อม Power Apps ที่มีอยู่ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b1261-132">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="b1261-133">โปรดทราบว่า ความจำเป็นในการเกี่ยวข้องกับการสนับสนุน และการติดต่อทีม DevOps ทรัพยากรบุคคลเป็นแบบชั่วคราว จนกว่าจะมีการเปิดใช้งานคุณลักษณะนี้โดยตรงใน LCS</span><span class="sxs-lookup"><span data-stu-id="b1261-133">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="b1261-134">โปรดติดต่อฝ่ายสนับสนุนเพื่อเริ่มต้นคำขอการลบ</span><span class="sxs-lookup"><span data-stu-id="b1261-134">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="b1261-135">ทีมสนับสนุนจะเริ่มต้นคำขอการลบด้วยทีม DevOps ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="b1261-135">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="b1261-136">ดำเนินการต่อ หลังจากที่คุณได้รับคำที่ว่าสภาพแวดล้อมได้ถูกลบออกแล้ว</span><span class="sxs-lookup"><span data-stu-id="b1261-136">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="b1261-137">ลงชื่อเข้าใช้ LCS โดยใช้บัญชีที่คุณใช้ในการสมัครสมาชิกทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="b1261-137">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="b1261-138">เลือกโครงการทรัพยากรบุคคลที่ประกอบด้วยสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="b1261-138">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="b1261-139">ในโครงการ LCS ของคุณ เลือกไทล์ **การจัดการแอป Human Resources**</span><span class="sxs-lookup"><span data-stu-id="b1261-139">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="b1261-140">เลือกอินสแตนซ์ที่คุณต้องการลบ ซึ่งควรถูกทำเครื่องหมายด้วยสถานะการปรับใช้เป็น **ล้มเหลว**</span><span class="sxs-lookup"><span data-stu-id="b1261-140">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="b1261-141">เลือก **ลบอินสแตนซ์** และยืนยันการตัดสินใจของคุณ</span><span class="sxs-lookup"><span data-stu-id="b1261-141">Select **Remove instance** and confirm your decision.</span></span> 
