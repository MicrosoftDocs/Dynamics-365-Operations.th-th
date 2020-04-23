---
title: เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b5f83474e56c996a40bdbdf7d3a7c8d495429c6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208949"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="44bd3-103">เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="44bd3-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="44bd3-104">เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบสามารถเกี่ยวข้องกับชนิดของสินทรัพย์ สินทรัพย์ ตำแหน่งที่ทำงาน ประเภทของชนิดงานบำรุงรักษา ชนิดงานการบำรุงรักษา ตัวแปรชนิดงานการบำรุงรักษา และการซื้อขาย</span><span class="sxs-lookup"><span data-stu-id="44bd3-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="44bd3-105">สามารถใช้ได้ในใบสั่งงานและคำขอการบำรุงรักษาเพื่อบ่งชี้การกำหนดลักษณะเกี่ยวกับเจ้าหน้าที่บำรุงรักษาที่ควรรับผิดชอบใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="44bd3-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="44bd3-106">(อย่างไรก็ตาม เจ้าหน้าที่บำรุงรักษาเหล่านั้นไม่จำเป็นต้องเป็นผู้ปฏิบัติงานคนเดียวกันที่ถูกจัดกำหนดเวลาให้ดำเนินการใบสั่งงาน) การใช้ฟังก์ชันนี้เป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="44bd3-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="44bd3-107">ตัวอย่างเช่น สามารถใช้เพื่อเลือกผู้ปฏิบัติงานที่รับผิดชอบหรือกลุ่มผู้ปฏิบัติงานสำหรับชนิดงานหรือพื้นที่ทำงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="44bd3-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="44bd3-108">ในระหว่างวงจรการใช้งานใบสั่งงานหรือวงจรการใช้งานคำขอการบำรุงรักษา คุณสามารถเปลี่ยนหรือปรับปรุงเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="44bd3-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="44bd3-109">การเปลี่ยนแปลงหรือการปรับปรุงนี้อาจเกี่ยวข้องกับ ตัวอย่างเช่น การเปลี่ยนแปลงในสสถานะของวงจรการใช้ของคำขอการบำรุงรักษา หรือสถานะของวงจรการใช้ของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="44bd3-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="44bd3-110">การตั้งค่าในหน้า **เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ** *ไม่* ถูกใช้ในระหว่างการจัดกำหนดการใบสั่งาน</span><span class="sxs-lookup"><span data-stu-id="44bd3-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="44bd3-111">ในการจัดการสินทรัพย์ คุณยังสามารถตั้งค่าเจ้าหน้าที่บำรุงรักษา *ที่ต้องการ* ซึ่งอาจถูกปันส่วนให้กับใบสั่งงานในระหว่างการจัดกำหนดการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="44bd3-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="44bd3-112">ก่อนที่คุณจะสามารถตั้งค่าเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบได้ คุณต้องตั้งค่ากลุ่มผู้ปฏิบัติงานและกลุ่มเจ้าหน้าที่บำรุงรักษาที่ควรพร้อมใช้งานสำหรับการเลือก</span><span class="sxs-lookup"><span data-stu-id="44bd3-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="44bd3-113">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่ากลุ่มผู้ปฏิบัติงานและกลุ่มเจ้าหน้าที่บำรุงรักษา ดู [กลุ่มผู้ปฏิบัติงานและกลุ่มเจ้าหน้าที่บำรุงรักษา](../setup-for-objects/workers-and-worker-groups.md)</span><span class="sxs-lookup"><span data-stu-id="44bd3-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="44bd3-114">ตั้งค่าเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="44bd3-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="44bd3-115">เลือก **สินทรัพย์** \> **การตั้งค่า** \> **ผู้ปฏิบัติ** \> **เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ**</span><span class="sxs-lookup"><span data-stu-id="44bd3-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="44bd3-116">เลือก **สร้าง** เพื่อสร้างเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="44bd3-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="44bd3-117">อันดับแรก สร้างการตั้งค่าเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบเริ่มต้น หรือกลุ่มเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ ที่ซึ่งคุณตั้งค่าเฉพาะฟิลด์ **กลุ่มเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ** และ/หรือฟิลด์ **ผู้ปฏิบัติงานที่รับผิดชอบ**</span><span class="sxs-lookup"><span data-stu-id="44bd3-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="44bd3-118">ปล่อยให้ฟิลด์ที่เหลือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="44bd3-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="44bd3-119">การตั้งค่าเริ่มต้นนี้จะใช้ในระหว่างการจัดกำหนดการใบสั่งงาน ถ้าไม่มีรายการอื่น การรวมกันที่เฉพาะเจาะจงมากขึ้นจับคู่เนื้อหาของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="44bd3-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="44bd3-120">ในระหว่างการสร้างคำขอการบำรุงรักษา เมื่อเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบหรือกลุ่มเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ ถูกทำให้พร้อมใช้งานสำหรับการเลือกในหน้า **คำขอการบำรุงรักษาทั้งหมด** การจัดการสินทรัพย์จะผ่านเรกคอร์ดเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบเพื่อตรวจสอบการจับคู่ที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="44bd3-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="44bd3-121">ซึ่งจะตรวจสอบชุดที่เฉพาะเจาะจงมากที่สุดก่อน</span><span class="sxs-lookup"><span data-stu-id="44bd3-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="44bd3-122">กล่าวคือ อันดับแรกการจัดการสินทรัพย์ตรวจสอบการจับคู่สำหรับฟิลด์ **การค้า**</span><span class="sxs-lookup"><span data-stu-id="44bd3-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="44bd3-123">ถ้าไม่พบการจับคู่ จะตรวจสอบการจับคู่สำหรับฟิลด์ **ตัวแปรชนิดงานบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="44bd3-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="44bd3-124">ถ้าไม่พบการจับคู่ จะตรวจสอบการจับคู่สำหรับฟิลด์ **ชนิดงานบำรุงรักษา** เป็นต้น</span><span class="sxs-lookup"><span data-stu-id="44bd3-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="44bd3-125">ดังที่คุณสามารถเห็นได้ในโครงร่างของหน้า ลักษณะการทำงานนี้หมายความว่า ในการค้นหาชุดที่เฉพาะเจาะจงมากที่สุด การจัดการสินทรัพย์ตรวจสอบเรกคอร์ดแต่ละรายการจากขวาไปซ้ายเพื่อจับคู่ (อันดับแรก **การค้า** จากนั้น **ตัวแปรชนิดงานบำรุงรักษา** จากนั้น **ชนิดงานบำรุงรักษา** จากนั้น **ประเภทของชนิดงานบำรุงรักษา** จากนั้น **ตำแหน่งที่ทำงาน** จากนั้น **สินทรัพย์** และสุดท้าย **ชนิดสินทรัพย์**)</span><span class="sxs-lookup"><span data-stu-id="44bd3-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="44bd3-126">ถ้าไม่พบการจับคู่ จะมีการใช้เรกคอร์ดข้อมูลเริ่มต้นที่ไม่มีการเลือกในฟิลด์ทั้งเจ็ดฟิลด์</span><span class="sxs-lookup"><span data-stu-id="44bd3-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="44bd3-127">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้า **เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ**</span><span class="sxs-lookup"><span data-stu-id="44bd3-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![หน้าเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ](media/08-setup-for-requests.png)
