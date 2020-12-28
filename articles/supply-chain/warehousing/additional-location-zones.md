---
title: โซนเวลาของสถานที่เพิ่มเติม
description: หัวข้อนี้แสดงภาพรวมของโซนเวลาของสถานที่ใหม่ที่มีการเพิ่มลงใน Microsoft Dynamics 365 Supply Chain Management
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 6cf81939989b8faffcda51bbbd5bc6b27aec7eea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4438849"
---
# <a name="additional-location-zones"></a><span data-ttu-id="c47dd-103">โซนเวลาของสถานที่เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c47dd-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c47dd-104">ฟิลด์โซนเวลาใหม่สามฟิลด์พร้อมใช้งานใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c47dd-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c47dd-105">ผู้จัดการคลังสินค้าสามารถใช้เพื่อกำหนดองค์กรหรือโครงร่างของคลังสินค้าเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c47dd-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="c47dd-106">สามารถตั้งฟิลด์โซนเวลาใหม่ด้วยตนเอง หรือโดยใช้วิซาร์ด **การตั้งค่าสถานที่**</span><span class="sxs-lookup"><span data-stu-id="c47dd-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="c47dd-107">สามารถใช้ได้ในการสอบถามหรือการกรองข้อมูลที่ใช้ตารางสถานที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="c47dd-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="c47dd-108">ไม่จำเป็นต้องมีการตั้งค่าเพิ่มเติมสำหรับการใช้ฟิลด์โซนเวลา</span><span class="sxs-lookup"><span data-stu-id="c47dd-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="c47dd-109">เปิดคุณลักษณะโซนเวลาสถานที่เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c47dd-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="c47dd-110">ก่อนที่คุณจะสามารถใช้คุณลักษณะ *โซนเวลาสถานที่เพิ่มเติม* จะต้องมีการเปิดอยู่ในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="c47dd-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="c47dd-111">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="c47dd-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="c47dd-112">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c47dd-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c47dd-113">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="c47dd-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c47dd-114">**ชื่อคุณลักษณะ:** *โซนเวลาสถานที่เพิ่มเติม*</span><span class="sxs-lookup"><span data-stu-id="c47dd-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="c47dd-115">ใช้โซนเวลาสถานที่</span><span class="sxs-lookup"><span data-stu-id="c47dd-115">Use location zones</span></span>

1. <span data-ttu-id="c47dd-116">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> วิซาร์ดการตั้งค่าสถานที่**</span><span class="sxs-lookup"><span data-stu-id="c47dd-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="c47dd-117">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c47dd-117">Set the following values:</span></span>

    - <span data-ttu-id="c47dd-118">ในฟิลด์  **คลังสินค้า** เลือก _62_</span><span class="sxs-lookup"><span data-stu-id="c47dd-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="c47dd-119">ในฟิลด์ **รหัสโซน** ให้เลือก _FLOOR_</span><span class="sxs-lookup"><span data-stu-id="c47dd-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="c47dd-120">ในฟิลด์ **โซนเวลาเพิ่มเติม 1** ให้เลือก _PICKZONE1_</span><span class="sxs-lookup"><span data-stu-id="c47dd-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="c47dd-121">ในฟิลด์ **โซนเวลาเพิ่มเติม 2** ให้เลือก _WEBSHOP1_</span><span class="sxs-lookup"><span data-stu-id="c47dd-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="c47dd-122">ในฟิลด์ **รหัสโพรไฟล์สถานที่** ให้เลือก _FLOOR_</span><span class="sxs-lookup"><span data-stu-id="c47dd-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="c47dd-123">เลือกรายการ **ชั้น**</span><span class="sxs-lookup"><span data-stu-id="c47dd-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="c47dd-124">ในฟิลด์ **จากหมายเลข** ให้ป้อน _1_</span><span class="sxs-lookup"><span data-stu-id="c47dd-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="c47dd-125">ในฟิลด์ **ไปยังหมายเลข** ให้ป้อน _3_</span><span class="sxs-lookup"><span data-stu-id="c47dd-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="c47dd-126">เลือกรายการ **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="c47dd-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="c47dd-127">ในฟิลด์ **จากหมายเลข** ให้ป้อน _1_</span><span class="sxs-lookup"><span data-stu-id="c47dd-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="c47dd-128">ในฟิลด์ **ไปยังหมายเลข** ให้ป้อน _5_</span><span class="sxs-lookup"><span data-stu-id="c47dd-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="c47dd-129">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c47dd-129">Select **Create**.</span></span>
8. <span data-ttu-id="c47dd-130">คุณได้รับข้อความแจ้งว่ามีการเพิ่มสถานที่ตั้งใหม่แล้ว</span><span class="sxs-lookup"><span data-stu-id="c47dd-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="c47dd-131">เลือกปุ่ม **แสดงข้อความ** เพื่อดูข้อความ</span><span class="sxs-lookup"><span data-stu-id="c47dd-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="c47dd-132">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> สถานที่**</span><span class="sxs-lookup"><span data-stu-id="c47dd-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="c47dd-133">สถานที่ใหม่จะปรากฏในรายการและฟิลด์โซนเวลาทั้งหมดจะพร้อมใช้งาน (นั่นคือฟิลด์โซนเวลาที่มีอยู่และฟิลด์โซนเวลาเพิ่มเติมใหม่)</span><span class="sxs-lookup"><span data-stu-id="c47dd-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
