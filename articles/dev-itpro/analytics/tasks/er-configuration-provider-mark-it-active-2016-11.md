--- 
title: "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่สำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
description: "ขั้นตอนต่อไปนี้จะอธิบายวิธีที่ผู้ใช้ถูกกำหนดให้รับบทบาทเป็นผู้ดูแลระบบหรือนักพัฒนารายงานอิเล็กทรอนิกส์ที่สามารถสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับการรายงานอิเล็กทรอนิกส์ (ER) "
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 809a1466b0f4674f503bc654175d8f94b37a6508
ms.openlocfilehash: 2dfa04f280249884af2a237807fb283059444a6c
ms.contentlocale: th-th
ms.lasthandoff: 11/02/2017

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="e991b-103">สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่สำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="e991b-103">Create a configuration provider and mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e991b-104">ขั้นตอนต่อไปนี้จะอธิบายวิธีที่ผู้ใช้ถูกกำหนดให้รับบทบาทเป็นผู้ดูแลระบบหรือนักพัฒนารายงานอิเล็กทรอนิกส์ที่สามารถสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับการรายงานอิเล็กทรอนิกส์ (ER) </span><span class="sxs-lookup"><span data-stu-id="e991b-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="e991b-105">การตั้งค่าคอนฟิก ER แต่ละครั้ง จะอ้างถึงตัวให้บริการให้เป็นผู้สร้างการตั้งค่าคอนฟิก </span><span class="sxs-lookup"><span data-stu-id="e991b-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="e991b-106">ในตัวอย่างนี้ คุณจะสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, inc ขั้นตอนเหล่านี้สามารถได้ในบริษัทอื่นใด ในฐานะตัวให้บริการการตั้งค่าคอนฟิก ER ที่ใช้ร่วมกันระหว่างบริษัททั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e991b-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="e991b-107">สร้างผู้ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="e991b-107">Create a provider</span></span>
1. <span data-ttu-id="e991b-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="e991b-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e991b-109">คลิก ผู้ให้บริการการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="e991b-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="e991b-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e991b-110">Click New.</span></span>
    * <span data-ttu-id="e991b-111">เรกคอร์ดของผู้ให้บริการมีชื่อและ URL ที่ไม่ซ้ำกัน </span><span class="sxs-lookup"><span data-stu-id="e991b-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="e991b-112">ตรวจทวนเนื้อหาของหน้านี้ และข้ามขั้นตอนนี้ถ้าเรกคอร์ดสำหรับ Litware, Inc. (http://www.litware.com) มีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="e991b-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="e991b-113">ในฟิลด์ชื่อ พิมพ์ 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="e991b-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="e991b-114">Litware, inc</span><span class="sxs-lookup"><span data-stu-id="e991b-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="e991b-115">ในฟิลด์ที่อยู่อินเทอร์เน็ต พิมพ์ 'http://www.litware.com'</span><span class="sxs-lookup"><span data-stu-id="e991b-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * <span data-ttu-id="e991b-116">http://www.litware.com</span><span class="sxs-lookup"><span data-stu-id="e991b-116">http://www.litware.com</span></span>  
6. <span data-ttu-id="e991b-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e991b-117">Click Save.</span></span>
7. <span data-ttu-id="e991b-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e991b-118">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="e991b-119">เลือกเป็นผู้ให้บริการที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="e991b-119">Select as an active provider</span></span>
1. <span data-ttu-id="e991b-120">เลือกผู้ให้บริการ Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="e991b-120">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="e991b-121">คลิก กำหนดเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="e991b-121">Click Set active.</span></span>


