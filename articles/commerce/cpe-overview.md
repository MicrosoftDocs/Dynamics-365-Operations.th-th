---
title: ภาพรวมของสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce
description: หัวข้อนี้จะแสดงภาพรวมของสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 25c0574e8d4502bcb846fba0ddf913d81eded87b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416023"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="f915a-103">ภาพรวมของสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f915a-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f915a-104">หัวข้อนี้จะแสดงภาพรวมของสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f915a-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="f915a-105">สภาพแวดล้อมการประเมิน Commerce โดยทั่วไปไม่พร้อมใช้งาน และจะถูกกำหนดให้กับคู่ค้าและลูกค้าในแต่ละคำขอ</span><span class="sxs-lookup"><span data-stu-id="f915a-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="f915a-106">สำหรับข้อมูลเพิ่มเติม ติดต่อคู่ค้า Microsoft ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f915a-106">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="f915a-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="f915a-107">Overview</span></span>

<span data-ttu-id="f915a-108">สภาพแวดล้อมการประเมินของ Commerce คือสภาพแวดล้อมที่ครอบคลุมที่ไม่จำเป็นต้องระบุของ Dynamics 365 Commerce ที่อนุญาตให้คู่ค้าและผู้ที่มีแนวโน้มจะเป็นลูกค้าทดลองใช้ผลิตภัณฑ์ Commerce ได้</span><span class="sxs-lookup"><span data-stu-id="f915a-108">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="f915a-109">สภาพแวดล้อมการประเมินมีการตั้งค่าคอนฟิกไว้ล่วงหน้าเพียงบางส่วนเพื่อลดขั้นตอนหลังการเตรียมใช้งานที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="f915a-109">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="f915a-110">นอกเหนือจากข้อจำกัดเล็กน้อยบางอย่างผลิตภัณฑ์ที่ไม่มีผลต่อคุณลักษณะหรือฟังก์ชัน สภาพแวดล้อมการประเมินของ Commerce จะมอบประสบการณ์ Commerce ที่สมบูรณ์ และสามารถนำมาใช้โดยลูกค้าและคู่ค้าที่ดำเนินการเพื่อประเมินผลิตภัณฑ์ ให้ความคิดเห็น และทำการวิเคราะห์ความเหมาะสม/ช่องว่าง</span><span class="sxs-lookup"><span data-stu-id="f915a-110">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="f915a-111">ข้อจำกัดของสภาพแวดล้อมการประเมินของ Commerce</span><span class="sxs-lookup"><span data-stu-id="f915a-111">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="f915a-112">ถึงแม้ว่าสภาพแวดล้อมการประเมินของ Commerce จะให้ชุดของคุณลักษณะและการทำงานของ Commerce อย่างเต็มรูปแบบ แต่ก็มีข้อจำกัดเล็กน้อยบางอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f915a-112">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="f915a-113">ถึงแม้ว่าสภาพแวดล้อมการประเมินของ Commerce จะไม่มีข้อจำกัดทางภูมิศาสตร์ ส่วนประกอบของสภาพแวดล้อม เช่น Retail Cloud Scale Unit (RCSU) และแอปพลิเคชันอีคอมเมิร์ซ ควรถูกเตรียมใช้งานเฉพาะในสหรัฐอเมริกาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f915a-113">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="f915a-114">การใช้สภาพแวดล้อมการประเมินของ Commerce ถูกจำกัดที่ 30 วัน นับจากวันที่มีการเตรียมใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="f915a-114">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="f915a-115">สามารถปรับใช้สภาพแวดล้อมการประเมินของ Commerce ได้สำเร็จแล้ว และเริ่มต้นเฉพาะในสภาพแวดล้อมที่ใช้โทโพโลยีสาธิต ที่ซึ่งส่วนประกอบทั้งหมดของสภาพแวดล้อมถูกปรับใช้ในเครื่องเสมือน (VM) ที่โฮสต์บนระบบคลาวด์เดียว</span><span class="sxs-lookup"><span data-stu-id="f915a-115">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="f915a-116">ข้อจำกัดหลักของโทโพโลยีนี้คือ จำนวนของผู้ใช้พร้อมกันที่สภาพแวดล้อมสามารถรองรับได้</span><span class="sxs-lookup"><span data-stu-id="f915a-116">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="f915a-117">เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f915a-117">Get started</span></span>

<span data-ttu-id="f915a-118">เมื่อต้องการเตรียมใช้งานสภาพแวดล้อมการประเมินของ Commerce โปรดดูที่ [เตรียมใช้งานสภาพแวดล้อมการประเมินของ Commerce](provisioning-guide.md)</span><span class="sxs-lookup"><span data-stu-id="f915a-118">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f915a-119">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f915a-119">Additional resources</span></span>

[<span data-ttu-id="f915a-120">เตรียมใช้งานสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f915a-120">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="f915a-121">ตั้งค่าคอนฟิกภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f915a-121">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="f915a-122">ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f915a-122">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="f915a-123">ตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f915a-123">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="f915a-124">FAQ เกี่ยวกับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f915a-124">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)
