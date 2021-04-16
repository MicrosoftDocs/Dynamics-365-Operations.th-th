---
title: FAQ เกี่ยวกับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce
description: หัวข้อนี้ให้คำตอบของคำถามที่ถามบ่อยเกี่ยวกับสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e42618a522f5ad551f608605300c30b5ffb8e299
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795942"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="3eba7-103">FAQ เกี่ยวกับสภาพแวดล้อมการประเมิน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3eba7-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3eba7-104">หัวข้อนี้ให้คำตอบของคำถามที่ถามบ่อยเกี่ยวกับสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3eba7-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="3eba7-105">**เราสามารถใช้สภาพแวดล้อมการประเมินของ Commerce เป็นหน้าร้านอีคอมเมิร์ซสำหรับลูกค้าที่ใช้ Retail ในปัจจุบันได้หรือไม่**</span><span class="sxs-lookup"><span data-stu-id="3eba7-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="3eba7-106">ลำดับที่</span><span class="sxs-lookup"><span data-stu-id="3eba7-106">No.</span></span> <span data-ttu-id="3eba7-107">สภาพแวดล้อมการประเมินของ Commerce มีไว้สำหรับการประเมินเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3eba7-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="3eba7-108">ถ้าคุณต้องการสภาพแวดล้อมสำหรับลูกค้าที่ดำเนินการขายปลีกให้ติดต่อ Microsoft</span><span class="sxs-lookup"><span data-stu-id="3eba7-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="3eba7-109">**สามารถใช้สภาพแวดล้อมการประเมินของ Commerce เพื่อเตรียมใช้งานคุณลักษณะอีคอมเมิร์ซเพิ่มเติมจากแอปพลิเคชัน/สภาพแวดล้อมที่ใช้งาน Retail ได้หรือไม่**</span><span class="sxs-lookup"><span data-stu-id="3eba7-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="3eba7-110">ไม่ (ส่วนใหญ่)</span><span class="sxs-lookup"><span data-stu-id="3eba7-110">No (mostly).</span></span> <span data-ttu-id="3eba7-111">ส่วนประกอบการประเมิน Commerce มีอยู่เฉพาะสำหรับสภาพแวดล้อมที่ตรงกับการตั้งค่าคอนฟิกที่ระบุไว้ในคำแนะนำเกี่ยวกับข้อกำหนดเบื้องต้นและการเตรียมใช้งานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3eba7-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="3eba7-112">นอกจากนี้ ข้อมูลการสาธิตพื้นฐานที่จำเป็นจะไม่พร้อมใช้งานในสภาพแวดล้อมที่มีการปรับใช้โดยมีการนำออกใช้เริ่มต้นก่อนหน้า 10.0.8</span><span class="sxs-lookup"><span data-stu-id="3eba7-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="3eba7-113">**ค่าใช้จ่ายอะไรบ้างที่เกี่ยวข้องในการปรับใช้สภาพแวดล้อมการประเมินของ Commerce บน Microsoft Azure ผ่าน Microsoft Dynamics Lifecycle Services (LCS)**</span><span class="sxs-lookup"><span data-stu-id="3eba7-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="3eba7-114">สภาพแวดล้อมการสาธิตของศูนย์ควบคุม Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce แบบดั้งเดิม (เครื่องเสมือน \[VM\]) จะถูกโฮสต์ในการบอกรับเป็นสมาชิก Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eba7-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="3eba7-115">คุณสามารถใช้เครื่องคิดเลข [Azure](https://azure.microsoft.com/pricing/calculator/) เพื่อกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="3eba7-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="3eba7-116">ส่วนประกอบอื่นๆ เช่น Commerce Scale Unit, Commerce site builder และไซต์อีคอมเมิร์ซของคุณ จะพร้อมใช้งานในฐานะการให้บริการซอฟต์แวร์ (SaaS) และโฮสต์โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="3eba7-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="3eba7-117">**ภูมิศาสตร์ Azure ใดที่ได้รับการสนับสนุนสำหรับสภาพแวดล้อมการประเมินของ Commerce ในขณะนี้**</span><span class="sxs-lookup"><span data-stu-id="3eba7-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="3eba7-118">สภาพแวดล้อมการประเมินของ Commerce สามารถปรับใช้ได้เฉพาะในภูมิศาสตร์อเมริกาเหนือเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3eba7-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="3eba7-119">**มีการดาวน์โหลดบนฮาร์ดดิสก์เสมือน (VHD) ที่มีตัวเลือกเครื่องเสมือนที่สมบูรณ์ OneBox (VM) หรือไม่?**</span><span class="sxs-lookup"><span data-stu-id="3eba7-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="3eba7-120">Dynamics 365 Commerce และ Commerce Scale Unit เป็นการให้บริการซอฟต์แวร์ (SaaS) ที่สมบูรณ์ และต้องเป็นโฮสต์แบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="3eba7-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="3eba7-121">**สามารถใช้สภาพแวดล้อมการประเมินของ Commerce ได้นานเท่าใด**</span><span class="sxs-lookup"><span data-stu-id="3eba7-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="3eba7-122">สภาพแวดล้อมการประเมินของ Commerce มีการจำกัดเวลา 30 วัน นับจากวันที่ซึ่งส่วนประกอบของ SaaS เช่น Commerce Scale Unit, Commerce site builder และไซต์อีคอมเมิร์ซของคุณ จะได้รับการเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3eba7-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="3eba7-123">**ฉันสามารถขยายขีดจำกัดเวลาสำหรับสภาพแวดล้อมการประเมินของ Commerce ได้หรือไม่**</span><span class="sxs-lookup"><span data-stu-id="3eba7-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="3eba7-124">ส่วนขยายของขีดจำกัดเวลาเป็นข้อยกเว้นของบรรทัดฐาน และจะถือว่าเป็นตามแต่ละกรณี</span><span class="sxs-lookup"><span data-stu-id="3eba7-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="3eba7-125">คุณควรติดต่อคู่ค้า Microsoft ของคุณสำหรับความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="3eba7-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3eba7-126">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3eba7-126">Additional resources</span></span>

[<span data-ttu-id="3eba7-127">ภาพรวมของสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3eba7-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="3eba7-128">เตรียมใช้งานสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3eba7-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="3eba7-129">ตั้งค่าคอนฟิกภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3eba7-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="3eba7-130">ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3eba7-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="3eba7-131">ตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3eba7-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]