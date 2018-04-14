---
title: "เท็มเพลตการบริการ"
description: "คุณสามารถกำหนดข้อตกลงการให้บริการเป็นเท็มเพลต และคัดลอกรายการของเท็มเพลตไปไว้ยังข้อตกลงการให้บริการอื่นหรือใบสั่งบริการในภายหลังได้"
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 24b7ffd18e6f69f497597eb12657d09f8d600dcf
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="service-templates"></a><span data-ttu-id="8493a-103">เท็มเพลตการบริการ</span><span class="sxs-lookup"><span data-stu-id="8493a-103">Service templates</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="8493a-104">คุณสามารถกำหนดข้อตกลงการให้บริการเป็นเท็มเพลต และคัดลอกรายการของเท็มเพลตไปไว้ยังข้อตกลงการให้บริการอื่นหรือใบสั่งบริการในภายหลังได้</span><span class="sxs-lookup"><span data-stu-id="8493a-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="8493a-105">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8493a-105">Example</span></span>

<span data-ttu-id="8493a-106">ลูกค้ารายหนึ่งที่คุณให้บริการมีลิฟต์ที่คุณต้องให้บริการเหมือนกันในสถานที่ต่างๆ ห้าแห่ง</span><span class="sxs-lookup"><span data-stu-id="8493a-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="8493a-107">คุณต้องการตั้งค่าข้อตกลงการให้บริการห้าฉบับให้แก่ลูกค้าดังกล่าวไซต์ละหนึ่งฉบับ </span><span class="sxs-lookup"><span data-stu-id="8493a-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="8493a-108">เพื่อจำกัดการตั้งค่างานที่ซ้ำกัน และเพื่อความแน่ใจว่าข้อมูลการตั้งค่าในข้อตกลงการให้บริการตรงกันทุกฉบับ ให้คุณสร้างข้อตกลงการให้บริการและกำหนดให้ข้อตกลงการให้บริการนั้นเป็นเท็มเพลตสำหรับงานที่ให้บริการเกี่ยวกับลิฟต์</span><span class="sxs-lookup"><span data-stu-id="8493a-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="8493a-109">ตอนนี้ คุณสามารถคัดลอกรายการเท็มเพลตไปไว้ยังข้อตกลงการให้บริการใหม่ทั้งห้าฉบับได้ เพื่อให้ข้อตกลงการให้บริการแต่ละฉบับมีข้อมูลรายการต่างๆ จากเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="8493a-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="8493a-110">สร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="8493a-110">Create a template</span></span>

<span data-ttu-id="8493a-111">เมื่อคุณสร้างเท็มเพลตการให้บริการ ให้คุณสร้างข้อตกลงการให้บริการ สร้างรายการที่จำเป็นในข้อตกลงนั้น และแนบข้อตกลงการให้บริการเข้ากับกลุ่มเท็มเพลตการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="8493a-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="8493a-112">คุณจะสามารถกำหนดข้อตกลงการให้บริการเป็นเท็มเพลตได้ก็ต่อเมื่อข้อตกลงการให้บริการนั้นไม่มีใบสั่งบริการใดๆ แนบอยู่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8493a-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="8493a-113">นอกจากนี้ คุณจะไม่สามารถสร้างใบสั่งบริการใดๆ จากข้อตกลงการให้บริการที่ถูกกำหนดไว้เป็นเท็มเพลตได้</span><span class="sxs-lookup"><span data-stu-id="8493a-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="8493a-114">คัดลอกรายการเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="8493a-114">Copy template lines</span></span>

<span data-ttu-id="8493a-115">คุณสามารถคัดลอกบรรทัดเท็มเพลตจากเท็มเพลตการให้บริการไปไว้ยังข้อตกลงการให้บริการอื่นหรือใบสั่งบริการได้</span><span class="sxs-lookup"><span data-stu-id="8493a-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="8493a-116">เมื่อคุณคัดลอกรายการเท็มเพลตไปไว้ยังใบสั่งบริการหรือข้อตกลงการให้บริการของคุณ กลุ่มเท็มเพลตของคุณจะปรากฏในมุมมองแผนภูมิซึ่งกลุ่มแต่ละกลุ่มสามารถถูกขยายได้</span><span class="sxs-lookup"><span data-stu-id="8493a-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="8493a-117">การแสดงผลนี้จะช่วยให้คุณสามารถดูเท็มเพลตและบรรทัดเท็มเพลตต่างๆ ได้</span><span class="sxs-lookup"><span data-stu-id="8493a-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="8493a-118">กำหนดรายการเท็มเพลตการให้บริการที่คุณต้องการคัดลอกได้ง่ายขึ้น หากคุณจัดกลุ่มเท็มเพลตภายใต้ชื่อที่บ่งบอกการใช้งานของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="8493a-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8493a-119">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8493a-119">Related topics</span></span>

[<span data-ttu-id="8493a-120">การคัดลอกบรรทัดเท็มเพลตการบริการ</span><span class="sxs-lookup"><span data-stu-id="8493a-120">Copy service templates lines</span></span>](copy-service-template-lines.md)

