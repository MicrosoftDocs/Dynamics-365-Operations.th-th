---
title: FAQ เกี่ยวกับการเริ่มใช้งานจริง
description: หัวข้อนี้จะแสดงรายการคำถามที่ถามบ่อยเกี่ยวกับการเริ่มใช้งานจริงกับโครงการการใช้งาน Dynamics 365 Human Resources
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
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
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 64a85840be328702a06779390fe383fd1896fd04
ms.sourcegitcommit: d66fd72342931fad25a696b251c05781280d36c4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/14/2020
ms.locfileid: "4011442"
---
# <a name="go-live-faq"></a><span data-ttu-id="1a0d3-103">FAQ เกี่ยวกับการเริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="1a0d3-103">Go-live FAQ</span></span> 

<span data-ttu-id="1a0d3-104">หัวข้อนี้จะแสดงรายการคำถามที่ถามบ่อยเกี่ยวกับการเริ่มใช้งานจริงกับโครงการการใช้งาน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="1a0d3-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="1a0d3-105">ฉันสามารถตั้งค่าคอนฟิกและร้องขอสภาพแวดล้อมการผลิตของฉันได้เมื่อใด</span><span class="sxs-lookup"><span data-stu-id="1a0d3-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="1a0d3-106">โดยทั่วไป สภาพแวดล้อมการผลิตมีการจัดวางหลังจากมีคุณสมบัติตรงตามเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a0d3-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="1a0d3-107">การกำหนดทั้งหมดเป็นรหัสที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="1a0d3-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="1a0d3-108">การทดสอบการยอมรับของผู้ใช้ (UAT) เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="1a0d3-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="1a0d3-109">ลูกค้าได้ลงชื่อออกจากโซลูชันแล้ว</span><span class="sxs-lookup"><span data-stu-id="1a0d3-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="1a0d3-110">ไม่มีปัญหาการบล็อคสำหรับการเริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="1a0d3-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="1a0d3-111">เมื่อลูกค้าที่มีคุณสมบัติตรงตามระยะนี้ ทีม Microsoft FastTrack จะทำงานร่วมกับทีมโครงการเพื่อให้การประเมินผลการเริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="1a0d3-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="1a0d3-112">ข้อกำหนดเบื้องต้นในการปรับใช้สภาพแวดล้อมการผลิตมีอะไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="1a0d3-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="1a0d3-113">สำหรับรายการของข้อกำหนดเบื้องต้น ให้ดูที่  [เตรียมพร้อมสำหรับการใช้งานจริง](hr-admin-go-live-prepare.md)</span><span class="sxs-lookup"><span data-stu-id="1a0d3-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="1a0d3-114">การประเมินการเริ่มใช้งานจริงคืออะไร</span><span class="sxs-lookup"><span data-stu-id="1a0d3-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="1a0d3-115">การประเมินการเริ่มใช้งานจริงเป็นส่วนหนึ่งของ  [โปรแกรม Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview)</span><span class="sxs-lookup"><span data-stu-id="1a0d3-115">The go-live assessment is part of the [Microsoft FastTrack program](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span></span> <span data-ttu-id="1a0d3-116">ในระหว่างการรีวิวนี้ สถาปนิกโซลูชันประเมินว่าโครงการที่ใช้งานพร้อมสำหรับการตัดและการเริ่มใช้งานจริงที่ประสบความสำเร็จหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1a0d3-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="1a0d3-117">การรีวิวนี้บังคับสำหรับโครงการที่ใช้งานอยู่ทั้งหมดก่อนที่คุณจะสามารถร้องขอให้ดำเนินการเริ่มใช้งานจริงต่อไปในสภาพแวดล้อมการผลิตได้</span><span class="sxs-lookup"><span data-stu-id="1a0d3-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="1a0d3-118">สภาพแวดล้อม Sandbox ของเราจะถูกจัดวางในศูนย์ข้อมูลที่ของสหรัฐอเมริกากลาง</span><span class="sxs-lookup"><span data-stu-id="1a0d3-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="1a0d3-119">เราต้องการให้สภาพแวดล้อมการผลิตของเราถูกปรับใช้ในศูนย์ข้อมูลของสหรัฐตะวันตก</span><span class="sxs-lookup"><span data-stu-id="1a0d3-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="1a0d3-120">ฉันสามารถเลือกสหรัฐอเมริกาตะวันออกเป็นศูนย์ข้อมูลในการตั้งค่าคอนฟิกการผลิตของฉันได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="1a0d3-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="1a0d3-121">LCS ไม่จำกัดคุณจากการเลือกศูนย์ข้อมูลอื่นเมื่อคุณปรับใช้สภาพแวดล้อมของทรัพยากรบุคคลแต่เราขอแนะนำว่าไม่ควรเลือกศูนย์ข้อมูลอื่น</span><span class="sxs-lookup"><span data-stu-id="1a0d3-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="1a0d3-122">ถ้าคุณต้องการให้สภาพแวดล้อมการผลิตของคุณเป็นศูนย์ข้อมูลของสหรัฐตะวันตก คุณควรจัดวางสภาพแวดล้อม Sandbox ของคุณใหม่ให้กับศูนย์ข้อมูลของสหรัฐอเมริกาฝั่งตะวันตก แล้วทดสอบ และลงชื่อออก</span><span class="sxs-lookup"><span data-stu-id="1a0d3-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="1a0d3-123">สำหรับข้อมูลเกี่ยวกับการเลือกศูนย์ข้อมูลที่ถูกต้อง ให้ดูที่ [ข้อกำหนดของเครือข่าย](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements)</span><span class="sxs-lookup"><span data-stu-id="1a0d3-123">For information about selecting the correct datacenter, see [Network requirements](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="1a0d3-124">ระดับการเข้าถึงใดที่ฉันต้องมีกับทรัพยากร Azure สำหรับสภาพแวดล้อมของทรัพยากรบุคคลของฉัน</span><span class="sxs-lookup"><span data-stu-id="1a0d3-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="1a0d3-125">การเข้าถึงสภาพแวดล้อมของฝ่ายทรัพยากรบุคคลถูกจำกัด</span><span class="sxs-lookup"><span data-stu-id="1a0d3-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="1a0d3-126">คุณไม่สามารถเข้าถึงเครื่องเสมือน (VM) หรือ Microsoft Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="1a0d3-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="1a0d3-127">นอกจากนี้คุณยังไม่สามารถเข้าถึงฐานข้อมูลผ่าน Microsoft SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="1a0d3-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="1a0d3-128">ถึงแม้ว่าคุณจะไม่สามารถเข้าถึงทรัพยากร Azure หรือสภาพแวดล้อม Dynamics 365 Human Resources ของคุณได้โดยตรง มีคุณลักษณะเพิ่มเติมที่คุณสามารถใช้ในการเข้าถึงข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="1a0d3-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="1a0d3-129">คุณสามารถปรับใช้ฐานข้อมูล SQL Azure ในผู้เช่า Azure ของคุณเอง และใช้ลักษณะการทำงานของฐานข้อมูลของคุณเอง (BYOD) เพื่อซิงโครไนส์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1a0d3-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="1a0d3-130">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การใช้ฐานข้อมูลของคุณเอง (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database)</span><span class="sxs-lookup"><span data-stu-id="1a0d3-130">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span>

- <span data-ttu-id="1a0d3-131">คุณสามารถใช้การรวม Common Data Service กับการซิงโครไนส์เอนทิตีที่เลือกลงในฐานข้อมูล Common Data Service</span><span class="sxs-lookup"><span data-stu-id="1a0d3-131">You can use Common Data Service integration to synchronize select entities into the Common Data Service database.</span></span> <span data-ttu-id="1a0d3-132">สำหรับข้อมูลเพิ่มเติม ให้ดู [เอนทิตี Common Data Service](hr-developer-entities.md)</span><span class="sxs-lookup"><span data-stu-id="1a0d3-132">For more information, see [Common Data Service entities](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="1a0d3-133">การสำรองฐานข้อมูลการผลิตของฉันบ่อยเพียงใด</span><span class="sxs-lookup"><span data-stu-id="1a0d3-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="1a0d3-134">ฐานข้อมูลมีการป้องกันโดยสำเนาสำรองโดยอัตโนมัติที่ความถี่ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a0d3-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="1a0d3-135">ชนิดของการสำรอง</span><span class="sxs-lookup"><span data-stu-id="1a0d3-135">Type of backup</span></span> | <span data-ttu-id="1a0d3-136">ความถี่</span><span class="sxs-lookup"><span data-stu-id="1a0d3-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="1a0d3-137">สำเนาสำรองฐานข้อมูลแบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="1a0d3-137">Full database backup</span></span> | <span data-ttu-id="1a0d3-138">รายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="1a0d3-138">Weekly</span></span> |
| <span data-ttu-id="1a0d3-139">การสำรองฐานข้อมูลส่วนที่แตกต่าง</span><span class="sxs-lookup"><span data-stu-id="1a0d3-139">Differential database backup</span></span> | <span data-ttu-id="1a0d3-140">ทุกๆ 12-24 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="1a0d3-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="1a0d3-141">สำเนาสำรองล็อกธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="1a0d3-141">Transaction log backup</span></span> | <span data-ttu-id="1a0d3-142">ทุกๆ 5 ถึง10 นาที</span><span class="sxs-lookup"><span data-stu-id="1a0d3-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="1a0d3-143">Microsoft ยังคงมีสำเนาสำรองเพียงพอสำหรับการอนุญาตให้มีการคืนสภาพเวลา (PITR) ภายในเจ็ดวันหลังสุด</span><span class="sxs-lookup"><span data-stu-id="1a0d3-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last seven days.</span></span> 

<span data-ttu-id="1a0d3-144">สำหรับข้อมูลเพิ่มเติม ดูที่  [เรียนรู้เกี่ยวกับการสำรองข้อมูลฐานข้อมูล SQL อัตโนมัติ](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database)</span><span class="sxs-lookup"><span data-stu-id="1a0d3-144">For more information, see [Learn about automatic SQL Database backups](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="1a0d3-145">ฉันสามารถร้องขอสำเนาของการสำรองของฐานข้อมูลการผลิตของฉันได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="1a0d3-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="1a0d3-146">ลำดับที่</span><span class="sxs-lookup"><span data-stu-id="1a0d3-146">No.</span></span> <span data-ttu-id="1a0d3-147">คุณสามารถส่งคำขอการรีเฟรชฐานข้อมูลเพื่อคัดลอกสภาพแวดล้อมการผลิตของคุณไปยังสภาพแวดล้อม Sandbox อย่างไรก็ตาม</span><span class="sxs-lookup"><span data-stu-id="1a0d3-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="1a0d3-148">คุณสามารถปรับใช้ฐานข้อมูล SQL Azure ในผู้เช่า Azure ของคุณเอง และใช้ลักษณะการทำงาน BYOD เพื่อซิงโครไนส์ข้อมูลจากสภาพแวดล้อมการผลิตของคุณ</span><span class="sxs-lookup"><span data-stu-id="1a0d3-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="1a0d3-149">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การใช้ฐานข้อมูลของคุณเอง (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database)</span><span class="sxs-lookup"><span data-stu-id="1a0d3-149">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="1a0d3-150">ฉันจะย้ายสภาพแวดล้อม Sandbox ของฉันไปยังการผลิตสำหรับการเริ่มใช้งานจริงได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="1a0d3-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="1a0d3-151">เนื่องจากมีลักษณะการทำงานที่ไม่พร้อมใช้งานเมื่อต้องการย้ายสภาพแวดล้อมของคุณจาก Sandbox ไปยังสภาพแวดล้อมการผลิต คุณต้องใช้แพคเกจข้อมูลเพื่อย้ายข้อมูลไปยังสภาพแวดล้อมการผลิตของคุณ</span><span class="sxs-lookup"><span data-stu-id="1a0d3-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="1a0d3-152">เราขอแนะนำให้คุณเลือกรายการเอนทิตีที่มีการตั้งค่าคอนฟิกไว้ใน Sandbox ของคุณทั่วทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="1a0d3-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="1a0d3-153">หลังจากนั้นทดสอบกระบวนการตัดและการย้ายแพคเกจข้อมูลใดๆ ที่จำเป็นสำหรับการเริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="1a0d3-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="1a0d3-154">คุณต้องย้ายแพคเกจข้อมูลใดๆ เข้าไปในสภาพแวดล้อมการผลิตด้วยตนเองเมื่อคุณพร้อมที่จะไปใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="1a0d3-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="1a0d3-155">ฉันควรทำอย่างไรถ้าสภาพแวดล้อมการผลิตของฉันหยุดทำงาน</span><span class="sxs-lookup"><span data-stu-id="1a0d3-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="1a0d3-156">เมื่อต้องการรายงานการหยุดทำงานการผลิต ให้ทำตามขั้นตอนที่อธิบายไว้ใน  [รายงานการหยุดทำงานของการผลิต](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage)</span><span class="sxs-lookup"><span data-stu-id="1a0d3-156">To report a Production outage, follow the process described in [Report a production outage](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="1a0d3-157">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="1a0d3-157">See also</span></span>

 [<span data-ttu-id="1a0d3-158">จัดเตรียมสำหรับการเริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="1a0d3-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)