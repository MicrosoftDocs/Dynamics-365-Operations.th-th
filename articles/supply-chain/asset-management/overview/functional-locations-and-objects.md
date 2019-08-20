---
title: ตำแหน่งที่ทำงานและสินทรัพย์
description: หัวข้อนี้จะอธิบายตำแหน่งที่ทำงานและสินทรัพย์ในการจัดการสินทรัพย์ การจัดการสินทรัพย์เป็นโมดูลขั้นสูงสำหรับการจัดการสินทรัพและงานบำรุงรักษาใน Microsoft Dynamics 365 for Finance and Operations
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 351e27dfbbd5227a9642f14a48afe194c447a0f3
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783642"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="906a2-104">ตำแหน่งที่ทำงานและสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="906a2-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="906a2-105">หัวข้อนี้จะอธิบายตำแหน่งที่ทำงานและสินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="906a2-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="906a2-106">การจัดการสินทรัพย์เป็นโมดูลขั้นสูงสำหรับการจัดการสินทรัพและงานบำรุงรักษาใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="906a2-106">Asset Management is an advanced module for managing assets and maintenance jobs in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="overview"></a><span data-ttu-id="906a2-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="906a2-107">Overview</span></span>

<span data-ttu-id="906a2-108">การจัดการสินทรัพย์ถูกรวมกันอย่างต่อเนื่องกับโมดูลหลายรายการใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="906a2-108">Asset Management is integrated seamlessly with several modules in Finance and Operations.</span></span> <span data-ttu-id="906a2-109">ภาพประกอบต่อไปนี้แสดงอินเทอร์เฟซที่มีโมดูลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="906a2-109">The following illustration shows the interfaces with other modules.</span></span>

![รูปที่ 1](media/01-overview-image.png)

<span data-ttu-id="906a2-111">การจัดการสินทรัพย์ช่วยให้คุณสามารถจัดการและดำเนินงานทั้งหมดที่เกี่ยวข้องกับการจัดการและการให้บริการอุปกรณ์หลายชนิดในบริษัทของคุณได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="906a2-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="906a2-112">อุปกรณ์นี้รวมถึงเครื่องจักร อุปกรณ์การผลิต และยานพาหนะ</span><span class="sxs-lookup"><span data-stu-id="906a2-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="906a2-113">นอกจากนี้ การจัดการสินทรัพย์สนับสนุนโซลูชันในอุตสาหกรรมมากมาย</span><span class="sxs-lookup"><span data-stu-id="906a2-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="906a2-114">ภาพประกอบต่อไปนี้แสดงภาพรวมของฟังก์ชันหลักที่ครอบคลุมโดยการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="906a2-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![รูปที่ 2](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="906a2-116">ตำแหน่งที่ทำงานและสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="906a2-116">Functional locations and assets</span></span>

<span data-ttu-id="906a2-117">ตำแหน่งที่ทำงานจะใช้จัดการสินทรัพย์ในสถานที่</span><span class="sxs-lookup"><span data-stu-id="906a2-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="906a2-118">การจัดการนี้รวมถึงการติดตามต้นทุนสินทรัพย์ในตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="906a2-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="906a2-119">มีการจัดโครงสร้างตำแหน่งที่ทำงานตามลำดับชั้น และสถานที่สามารถมีสถานที่ย่อยได้</span><span class="sxs-lookup"><span data-stu-id="906a2-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="906a2-120">โครงสร้างของตำแหน่งที่ทำงานเป็นแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="906a2-120">The structure of functional locations is static.</span></span> <span data-ttu-id="906a2-121">กล่าวคือ ที่ตั้งไม่สามารถเปลี่ยนสถานที่ได้</span><span class="sxs-lookup"><span data-stu-id="906a2-121">In other words, locations can't change place.</span></span> <span data-ttu-id="906a2-122">สินทรัพย์สามารถติดตั้งได้ในตำแหน่งที่ทำงานและ ตามความจำเป็น สามารถติดตั้งได้ในตำแหน่งที่ทำงานอื่นๆ ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="906a2-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="906a2-123">ต้นทุนสินทรัพย์จะติดตามสถานที่ของสินทรัพย์เสมอ</span><span class="sxs-lookup"><span data-stu-id="906a2-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="906a2-124">กล่าวคือ ถ้าคุณติดตั้งสินทรัพย์ในตำแหน่งที่ทำงานใหม่ สินทรัพย์จะใช้มิติทางการเงินที่เกี่ยวข้องกับตำแหน่งที่ทำงานใหม่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="906a2-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="906a2-125">ดังนั้น ต้นทุนสินทรัพย์จะเกี่ยวข้องกับตำแหน่งที่ทำงานที่มีการติดตั้งสินทรัพย์ในปัจจุบันเสมอ</span><span class="sxs-lookup"><span data-stu-id="906a2-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="906a2-126">การจัดการแบบอัตโนมัติของมิติทางการเงินนี้จะช่วยรับประกันการติดตามต้นทุนที่เสร็จสมบูรณ์ เมื่อบริษัทของคุณทำการควบคุมโครงการและการรายงานเกี่ยวกับตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="906a2-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="906a2-127">วิธีที่คุณสร้างลำดับชั้นของตำแหน่งที่ทำงานขึ้นอยู่กับความต้องการของบริษัทของคุณ สำหรับการรักษาอุปกรณ์ภายในหรือการให้บริการอุปกรณ์ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="906a2-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="906a2-128">รูปต่อไปนี้แสดงตัวอย่างของตำแหน่งที่ทำงานที่ขึ้นอยู่กับสถานที่ตั้งทางภูมิศาสตร์</span><span class="sxs-lookup"><span data-stu-id="906a2-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![รูปที่ 3](media/03-overview-image.png)

<span data-ttu-id="906a2-130">รูปต่อไปนี้แสดงตัวอย่างของตำแหน่งที่ทำงานที่ขึ้นอยู่กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="906a2-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![รูปที่ 4](media/04-overview-image.png)
