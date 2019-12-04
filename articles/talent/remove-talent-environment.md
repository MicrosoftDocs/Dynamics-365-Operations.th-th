---
title: เอาสภาพแวดล้อม Talent ออก
description: หัวข้อนี้นำคุณไปสู่กระบวนการในการลบ Test Drive หรือสภาพแวดล้อมการผลิตสำหรับ Microsoft Dynamics 365 Talent
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: bbc65a77b7c3df6545dfd7aa2109aba5c4e1b57b
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773046"
---
# <a name="remove-talent-environments"></a><span data-ttu-id="c5877-103">เอาสภาพแวดล้อม Talent ออก</span><span class="sxs-lookup"><span data-stu-id="c5877-103">Remove Talent environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c5877-104">หัวข้อนี้นำคุณไปสู่กระบวนการในการลบ Test Drive หรือสภาพแวดล้อมการผลิตสำหรับ Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="c5877-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="c5877-105">การลบสภาพแวดล้อมไดรฟ์ทดสอบ</span><span class="sxs-lookup"><span data-stu-id="c5877-105">Removing a test drive environment</span></span>

<span data-ttu-id="c5877-106">ไดรฟ์ทดสอบ Talent ถูกเตรียมใช้งานโดยมีนโยบายการหมดอายุ 60 วัน</span><span class="sxs-lookup"><span data-stu-id="c5877-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="c5877-107">อย่างไรก็ตาม เจ้าของสภาพแวดล้อมไดรฟ์ทดสอบมีตัวเลือกในการสิ้นสุดการทดลองของพวกเขาก่อนเวลา โดยดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c5877-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="c5877-108">นำทางไปยัง [ศูนย์การจัดการ Power Apps](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="c5877-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="c5877-109">เลือก **สภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="c5877-109">Select **Environments**.</span></span>
3. <span data-ttu-id="c5877-110">เลือกสภาพแวดล้อม Test Drive ซึ่งมีรูปแบบการตั้งชื่อที่คล้ายกับรายการนี้: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="c5877-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="c5877-111">เลือก **ลบ** และยืนยันการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="c5877-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="c5877-112">สภาพแวดล้อมไดรฟ์ทดสอบที่มีอยู่จะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="c5877-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="c5877-113">เมื่อถูกลบออก คุณสามารถลงชื่อสมัครสภาพแวดล้อมไดรฟ์ทดสอบใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="c5877-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="c5877-114">การลบสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="c5877-114">Removing a production environment</span></span>

<span data-ttu-id="c5877-115">หัวข้อนี้สันนิษฐานว่า คุณได้ซื้อ Talent ผ่านผู้ให้บริการโซลูชัน Cloud (CSP) หรือข้อตกลงสถาปัตยกรรมองค์กร (EA)</span><span class="sxs-lookup"><span data-stu-id="c5877-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="c5877-116">เนื่องจากสภาพแวดล้อม Talent เดียวถูก"บรรจุ"อยู่ภายในสภาพแวดล้อม Power Apps เดียวซึ่งคุณมีตัวเลือกสองตัวที่ควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="c5877-116">Since a single Talent environment is “contained” within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="c5877-117">ตัวเลือกแรกเกี่ยวข้องกับการลบสภาพแวดล้อม Power Apps ทั้งหมด; ตัวเลือกที่สองเกี่ยวข้องกับการลบเฉพาะ Talent</span><span class="sxs-lookup"><span data-stu-id="c5877-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="c5877-118">ตัวเลือกแรกเป็นที่ต้องการเมื่อคุณได้สร้างสภาพแวดล้อม Power Apps อย่างชัดเจนสำหรับวัตถุประสงค์ในการเตรียมใช้งาน Talent และคุณเพียงพึ่งเริ่มใช้งานหรือคุณไม่มีการรวมใดๆที่สร้างไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c5877-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="c5877-119">ตัวเลือกที่สองจะเหมาะสมก็ต่อเมื่อคุณได้มีสภาพแวดล้อม Power Apps ที่สร้างไว้แล้วซึ่งเต็มไปด้วยข้อมูลที่หลากหลายที่ถูกยกระดับใน Power Apps และ Power Automate</span><span class="sxs-lookup"><span data-stu-id="c5877-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="c5877-120">ก่อนที่จะลบสภาพแวดล้อม Power Apps คุณต้องแน่ใจว่าจะไม่มีการใช้สำหรับการรวมข้อมูลที่หลากหลายภายนอกขอบเขตของ Talent</span><span class="sxs-lookup"><span data-stu-id="c5877-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="c5877-121">นอกจากนี้โปรดทราบว่าค่าเริ่มต้นของสภาพแวดล้อม Power Apps ไม่สามารถลบได้</span><span class="sxs-lookup"><span data-stu-id="c5877-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="c5877-122">ในการลบสภาพแวดล้อม Power Apps ทั้งหมดซึ่งรวมถึง Talent และแอปและขั้นตอนที่เชื่อมโยง:</span><span class="sxs-lookup"><span data-stu-id="c5877-122">To remove the entire Power Apps environment, including Talent and the associated apps and flows:</span></span>

1. <span data-ttu-id="c5877-123">นำทางไปยัง [ศูนย์การจัดการ Power Apps](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="c5877-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="c5877-124">เลือก **สภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="c5877-124">Select **Environments**.</span></span>
3. <span data-ttu-id="c5877-125">เลือกสภาพแวดล้อมที่จะถูกลบ</span><span class="sxs-lookup"><span data-stu-id="c5877-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="c5877-126">เลือก **ลบ** และยืนยันการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="c5877-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="c5877-127">โปรดรอจนกว่าการลบข้อมูลจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c5877-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="c5877-128">ลงชื่อเข้าใช้ [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) โดยใช้บัญชีที่คุณใช้ในการสมัครสมาชิก Talent</span><span class="sxs-lookup"><span data-stu-id="c5877-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="c5877-129">เลือกโครงการ Talent ที่ประกอบด้วยสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="c5877-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="c5877-130">ในโครงการ LCS ของคุณ เลือกไทล์ **การจัดการแอป Talent**</span><span class="sxs-lookup"><span data-stu-id="c5877-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="c5877-131">เลือกอินสแตนซ์ที่จะลบ</span><span class="sxs-lookup"><span data-stu-id="c5877-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="c5877-132">เลือก **ลบอินสแตนซ์** และยืนยันการตัดสินใจของคุณ</span><span class="sxs-lookup"><span data-stu-id="c5877-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="c5877-133">ในการลบสภาพแวดล้อม Talent จากสภาพแวดล้อม Power Apps ที่มีอยู่ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c5877-133">To remove a Talent environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="c5877-134">โปรดทราบว่า ความจำเป็นในการเกี่ยวข้องกับการสนับสนุน และการติดต่อทีม Talent DevOps เป็นแบบชั่วคราว จนกว่าจะมีการเปิดใช้งานคุณลักษณะนี้โดยตรงใน LCS</span><span class="sxs-lookup"><span data-stu-id="c5877-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="c5877-135">โปรดติดต่อฝ่ายสนับสนุนเพื่อเริ่มต้นคำขอการลบ</span><span class="sxs-lookup"><span data-stu-id="c5877-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="c5877-136">ทีมสนับสนุนจะเริ่มต้นคำขอการลบด้วยทีม Talent DevOps</span><span class="sxs-lookup"><span data-stu-id="c5877-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="c5877-137">ดำเนินการต่อ หลังจากที่คุณได้รับคำที่ว่าสภาพแวดล้อมได้ถูกลบออกแล้ว</span><span class="sxs-lookup"><span data-stu-id="c5877-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="c5877-138">ลงชื่อเข้าใช้ LCS โดยใช้บัญชีที่คุณใช้ในการสมัครสมาชิก Talent</span><span class="sxs-lookup"><span data-stu-id="c5877-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="c5877-139">เลือกโครงการ Talent ที่ประกอบด้วยสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="c5877-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="c5877-140">ในโครงการ LCS ของคุณ เลือกไทล์ **การจัดการแอป Talent**</span><span class="sxs-lookup"><span data-stu-id="c5877-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="c5877-141">เลือกอินสแตนซ์ที่คุณต้องการลบ ซึ่งควรถูกทำเครื่องหมายด้วยสถานะการปรับใช้เป็น **ล้มเหลว**</span><span class="sxs-lookup"><span data-stu-id="c5877-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="c5877-142">เลือก **ลบอินสแตนซ์** และยืนยันการตัดสินใจของคุณ</span><span class="sxs-lookup"><span data-stu-id="c5877-142">Select **Remove instance** and confirm your decision.</span></span> 

