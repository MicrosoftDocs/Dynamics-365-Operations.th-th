---
title: สร้างกลุ่มสิทธิ์ของ POS
description: หัวข้อนี้อธิบายวิธีการสร้างกลุ่มสิทธิ์ของ POS
author: scott-tucker
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d4634ec275d3d1c2a131c4c1d61cc983e485b14
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798500"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="f8a6d-103">สร้างกลุ่มสิทธิ์ของ POS</span><span class="sxs-lookup"><span data-stu-id="f8a6d-103">Create POS permission groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8a6d-104">หัวข้อนี้อธิบายวิธีการสร้างกลุ่มสิทธิ์ของ POS</span><span class="sxs-lookup"><span data-stu-id="f8a6d-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="f8a6d-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างงานนี้คือ USRT </span><span class="sxs-lookup"><span data-stu-id="f8a6d-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="f8a6d-106">งานนี้เจาะจงสำหรับบทบาทผู้จัดการฝ่ายปฏิบัติการในเชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="f8a6d-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="f8a6d-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การขายปลีกและการค้า > พนักงาน > กลุ่มที่ได้รับสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="f8a6d-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="f8a6d-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f8a6d-108">Select **New**.</span></span>
3. <span data-ttu-id="f8a6d-109">ในฟิลด์ **รหัสกลุ่มสิทธิ์ของ POS** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f8a6d-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="f8a6d-110">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f8a6d-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f8a6d-111">เลือก **ใช่** ในฟิลด์ **ดูรายการของนาฬิกาตอกบัตร**</span><span class="sxs-lookup"><span data-stu-id="f8a6d-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="f8a6d-112">ขณะนี้คุณสามารถเปิดใช้งานหรือปิดใช้งานสิทธิ์ต่างๆ สำหรับกลุ่มสิทธิ์ของ POS ของคุณ </span><span class="sxs-lookup"><span data-stu-id="f8a6d-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="f8a6d-113">สำหรับบางสิทธิ์คุณสามารถตั้งค่าที่จะใช้เพื่อประเมินว่าผู้ใช้ POS สามารถดำเนินการได้หรือไม่ </span><span class="sxs-lookup"><span data-stu-id="f8a6d-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="f8a6d-114">คำแนะนำของงานนี้เปิดใช้งานสิทธิ์ส่วนหนึ่งที่อาจโอนให้กับพนักงานเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="f8a6d-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="f8a6d-115">เลือก **ใช่** ในฟิลด์ **อนุญาตให้สร้างใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="f8a6d-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="f8a6d-116">เลือก **ใช่** ในฟิลด์ **อนุญาตให้แก้ไขใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="f8a6d-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="f8a6d-117">เลือก **ใช่** ในฟิลด์ **อนุญาตให้ดึงข้อมูลใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="f8a6d-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="f8a6d-118">เลือก **ใช่** ในฟิลด์ **อนุญาตให้เปลี่ยนแปลงรหัสผ่าน**</span><span class="sxs-lookup"><span data-stu-id="f8a6d-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="f8a6d-119">เลือก **ใช่** ในฟิลด์ **อนุญาตให้ปิดซ่อน**</span><span class="sxs-lookup"><span data-stu-id="f8a6d-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="f8a6d-120">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f8a6d-120">Select **Save**.</span></span> <span data-ttu-id="f8a6d-121">หลังจากบันทึกการเปลี่ยนแปลงของคุณแล้ว คุณจำเป็นต้องเรียกใช้การจัดกำหนดการกระจายพนักงานเพื่อผลักดันการเปลี่ยนแปลงไปยังช่องทางการค้า</span><span class="sxs-lookup"><span data-stu-id="f8a6d-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="f8a6d-122">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > ทรัพยากรบุคคล > งาน > งาน**</span><span class="sxs-lookup"><span data-stu-id="f8a6d-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="f8a6d-123">ถัดไป เราจะกำหนดกลุ่มสิทธิ์ของ POS ให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="f8a6d-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="f8a6d-124">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f8a6d-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="f8a6d-125">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="f8a6d-125">Select **Edit**.</span></span>
15. <span data-ttu-id="f8a6d-126">ขยายส่วน **การจัดประเภทงาน**</span><span class="sxs-lookup"><span data-stu-id="f8a6d-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="f8a6d-127">ในฟิลด์สิทธิ์ของ POS ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f8a6d-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="f8a6d-128">ผู้ปฏิบัติงานทั้งหมดในตำแหน่งงานสำหรับงานนี้จะใช้การตั้งค่าของกลุ่มสิทธิ์ของ POS ยกเว้นว่าจะมีการแทนที่สิทธิ์ของ POS ของผู้ปฏิบัติงานในระดับของตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="f8a6d-128">All Workers in Positions for this Job will use this POS permission group's settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="f8a6d-129">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f8a6d-129">Select **Save**.</span></span> <span data-ttu-id="f8a6d-130">หลังจากบันทึกการเปลี่ยนแปลงของคุณแล้ว คุณจำเป็นต้องเรียกใช้การจัดกำหนดการกระจายพนักงานเพื่อผลักดันการเปลี่ยนแปลงไปยังช่องทางการค้า</span><span class="sxs-lookup"><span data-stu-id="f8a6d-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]