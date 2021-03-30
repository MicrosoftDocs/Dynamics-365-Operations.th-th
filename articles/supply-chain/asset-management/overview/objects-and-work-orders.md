---
title: สินทรัพย์และใบสั่งงาน
description: หัวข้อนี้จะอธิบายสินทรัพย์และใบสั่งงานในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6fd5aa8914437fb77ea25ec229c94cfb0bb12def
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253073"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="5bfae-103">สินทรัพย์และใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5bfae-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5bfae-104">หัวข้อนี้จะอธิบายสินทรัพย์และใบสั่งงานในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="5bfae-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="5bfae-105">สินทรัพย์และใบสั่งงานเป็นส่วนกลางของการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="5bfae-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="5bfae-106">*สินทรัพย์* เป็นชิ้นส่วนเครื่องจักรหรือเครื่องจักรที่ต้องการการบำรุงรักษาและบริการอย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="5bfae-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="5bfae-107">สินทรัพย์สามารถสร้างขึ้นได้ในโครงสร้างตามลำดับชั้น และสามารถเกี่ยวข้องกับตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="5bfae-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="5bfae-108">สามารถวางแผนงานการบำรุงรักษาได้ที่ทุกระดับในโครงสร้างสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="5bfae-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="5bfae-109">ข้อมูลต่างๆ เช่น ข้อมูลผลิตภัณฑ์ และรายละเอียดสินทรัพย์ และแผนการบำรุงรักษาที่จำเป็น จะถูกตั้งค่าไว้ในสินทรัพย์แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="5bfae-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="5bfae-110">ภาพประกอบต่อไปนี้แสดงภาพรวมของข้อมูลสินทรัพย์และสังกัดของสินทรัพย์สำหรับชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="5bfae-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="5bfae-111">ข้อความสีแดงจะใช้สำหรับตัวอย่างที่แสดงการสืบทอดและการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="5bfae-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![แผนภาพที่แสดงข้อมูลสินทรัพย์ที่เกี่ยวข้องกับชนิดงาน](media/05-overview-image.png)

<span data-ttu-id="5bfae-113">ใบสั่งงานทุกรายการมีชนิดใบสั่งงาน เช่น การบำรุงรักษาเชิงป้องกัน การบำรุงรักษาเชิงแก้ไข หรือการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="5bfae-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="5bfae-114">ใบสั่งงานประกอบด้วยงานในใบสั่งงานหนึ่งงานขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="5bfae-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="5bfae-115">งานในใบสั่งงานทุกงานจะกำหนดงานที่ต้องดำเนินการในสินทรัพย์และชนิดงานที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="5bfae-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="5bfae-116">ตัวอย่างของชนิดงานที่เกี่ยวข้อง ได้แก่ 10,000 กม. 50,000 กม. การซ่อมใหญ่ 1 ปี และการตรวจสอบความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5bfae-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="5bfae-117">ใบสั่งงานหนึ่งใบสามารถเกี่ยวข้องกับสินทรัพย์หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="5bfae-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="5bfae-118">ภาพประกอบต่อไปนี้จะแสดงภาพรวมของข้อมูลสำคัญในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5bfae-118">The following illustration shows an overview of the key data in a work order.</span></span>

![แผนภาพที่แสดงข้อมูลหลักในใบสั่งงาน](media/06-overview-image.png)

<span data-ttu-id="5bfae-120">ใบสั่งงานสามารถเกี่ยวข้องกับใบสั่งงานอื่น และชนิดงานสามารถประกอบด้วยงานที่ประสบความสำเร็จที่สร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5bfae-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="5bfae-121">โดยทั่วไป จะไม่มีการอ้างอิงระหว่างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5bfae-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="5bfae-122">ดังนั้น จึงสามารถเปลี่ยนแปลงสถานะของวงจรการใช้ของใบสั่งงานได้ และสามารถจัดกำหนดการอย่างเป็นอิสระจากกันได้</span><span class="sxs-lookup"><span data-stu-id="5bfae-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="5bfae-123">สามารถสร้างใบสั่งงานได้หลายวิธีที่เกี่ยวข้องกับการซ่อมแซม การป้องกัน หรือการบำรุงรักษาแบบเชิงรุก</span><span class="sxs-lookup"><span data-stu-id="5bfae-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="5bfae-124">นอกจากนี้ คุณยังสามารถสร้างใบสั่งงานด้วยตนเองได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="5bfae-124">You can also create work orders manually.</span></span> <span data-ttu-id="5bfae-125">ภาพประกอบต่อไปนี้แสดงภาพรวมของกระบวนการสำหรับการสร้างใบสั่งงานโดยอัตโนมัติหรือด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="5bfae-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![แผนภาพที่แสดงการสร้างใบสั่งงานโดยอัตโนมัติหรือด้วยตนเอง](media/07-overview-image.png)

<span data-ttu-id="5bfae-127">ต้องดำเนินการหลายขั้นตอนให้เสร็จสมบูรณ์ เมื่อคุณต้องการจัดกำหนดการและรันงานบำรุงรักษาในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5bfae-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="5bfae-128">ภาพประกอบต่อไปนี้จะแสดงภาพรวมของการประมวลผลของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5bfae-128">The following illustration shows an overview of the processing for a work order.</span></span>

![แผนภาพที่แสดงภาพรวมของการประมวลผลใบสั่งงาน](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="5bfae-130">โดยทั่วไป เมื่อคุณทำงานใน Dynamics 365 Supply Chain Management และโมดูล **การจัดการสินทรัพย์** คุณเลือก **สร้าง** เพื่อสร้างเรกคอร์ดใหม่ คุณเลือก **แก้ไข** เพื่อปรับปรุงเรกคอร์ดที่มีอยู่ และคุณเลือก **บันทึก** เพื่อบันทึกข้อมูลใหม่หรือที่แก้ไข</span><span class="sxs-lookup"><span data-stu-id="5bfae-130">In general, when you work in Dynamics 365 Supply Chain Management and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]