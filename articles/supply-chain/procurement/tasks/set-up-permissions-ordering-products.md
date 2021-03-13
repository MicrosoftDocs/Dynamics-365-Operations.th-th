---
title: ตั้งค่าสิทธิ์สำหรับการสั่งซื้อผลิตภัณฑ์ในนามของผู้อื่น
description: หัวข้อนี้อธิบายวิธีการให้สิทธิ์ผู้ปฏิบัติงานในการจัดเตรียมใบขอซื้อในนามของผู้ปฏิบัติงานอื่นๆ
author: RichardLuan
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 585f5c6cf83ad93b649e3f36e0d486a037915cd4
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017303"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="173fc-103">ตั้งค่าสิทธิ์สำหรับการสั่งซื้อผลิตภัณฑ์ในนามของผู้อื่น</span><span class="sxs-lookup"><span data-stu-id="173fc-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="173fc-104">หัวข้อนี้อธิบายวิธีการให้สิทธิ์ผู้ปฏิบัติงานในการจัดเตรียมใบขอซื้อในนามของผู้ปฏิบัติงานอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="173fc-104">This topic explains how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="173fc-105">กล่าวคือ "ผู้จัดเตรียม" ใบขอซื้อสามารถสร้างใบขอซื้อสำหรับ "ผู้ขอ" อื่น</span><span class="sxs-lookup"><span data-stu-id="173fc-105">In other words, a purchase requisition "preparer" can create a requisition for another "requester."</span></span> <span data-ttu-id="173fc-106">กระบวนงานนี้ยังแสดงวิธีการให้สิทธิ์ผู้ปฏิบัติงานในการสั่งซื้อสินค้าและบริการในนิติบุคคลหรือหน่วยปฏิบัติงานอื่น </span><span class="sxs-lookup"><span data-stu-id="173fc-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="173fc-107">โดยทั่วไปงานเหล่านี้จะดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="173fc-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="173fc-108">คุณสามารถใช้กระบวนงานนี้ในข้อมูลสำหรับบริษัทสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="173fc-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="173fc-109">ให้สิทธิ์ในการป้อนใบขอซื้อในนามของผู้ปฏิบัติงานอื่น</span><span class="sxs-lookup"><span data-stu-id="173fc-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="173fc-110">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดซื้อและการจัดหา > การตั้งค่า > นโยบาย > สิทธิ์สำหรับใบขอซื้อ**</span><span class="sxs-lookup"><span data-stu-id="173fc-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchase requisition permissions**.</span></span> <span data-ttu-id="173fc-111">ตรวจสอบให้แน่ใจว่าฟิลด์ **มุมมองปัจจุบัน** ถูกกำหนดเป็น **โดยผู้จัดเตรียม**</span><span class="sxs-lookup"><span data-stu-id="173fc-111">Make sure that the **Current view** field is set to **By preparer**.</span></span> <span data-ttu-id="173fc-112">รายการในบานหน้าต่างด้านซ้ายแสดงบุคคลที่ได้รับสิทธิ์ในการจัดเตรียมใบขอซื้อในนามของบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="173fc-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="173fc-113">เลือกบุคคลที่จะให้สิทธิ์แก่ (ผู้จัดเตรียม)</span><span class="sxs-lookup"><span data-stu-id="173fc-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="173fc-114">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="173fc-114">Select **Add**.</span></span>
4. <span data-ttu-id="173fc-115">ค้นหาและเลือกบุคคลที่จะเพิ่มเป็นผู้ขอ</span><span class="sxs-lookup"><span data-stu-id="173fc-115">Find and select the person to add as a requester.</span></span>
    - <span data-ttu-id="173fc-116">ผู้ขอคือบุคคลที่ผู้จัดเตรียมสามารถสร้างใบขอซื้อในนามนั้นได้</span><span class="sxs-lookup"><span data-stu-id="173fc-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    - <span data-ttu-id="173fc-117">ในฟิลด์ **การตรวจสอบ** เลือก **เฉพาะ** ถ้าผู้จัดเตรียมควรจะสามารถสร้างใบขอซื้อในนามของผู้ปฏิบัติงานที่เลือกได้</span><span class="sxs-lookup"><span data-stu-id="173fc-117">In the **Authorization** field, select **Specific** if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="173fc-118">เลือก **การรายงาน** ถ้าผู้จัดเตรียมควรจะสามารถสร้างใบขอซื้อในนามของผู้ปฏิบัติงานทั้งหมดที่รายงานถึงที่ผู้ปฏิบัติงานนั้นด้วย</span><span class="sxs-lookup"><span data-stu-id="173fc-118">Select **Reporting** if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="173fc-119">ในฟิลด์ **มีผลบังคับใช้** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="173fc-119">In the **Effective** field, enter a date.</span></span>
6. <span data-ttu-id="173fc-120">ในฟิลด์ **การหมดอายุ** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="173fc-120">In the **Expiration** field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="173fc-121">ดูผู้จัดเตรียมที่มีสิทธิ์ในการสร้างใบขอซื้อสำหรับผู้ปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="173fc-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="173fc-122">ในฟิลด์ **มุมมองปัจจุบัน** เลือก **โดยผู้ขอ**</span><span class="sxs-lookup"><span data-stu-id="173fc-122">In the **Current view** field, select **By requester**.</span></span> <span data-ttu-id="173fc-123">มุมมองนี้แสดงรายการของผู้จัดเตรียมที่ได้รับสิทธิ์ในการสร้างใบขอซื้อในนามของผู้ปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="173fc-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="173fc-124">ใช้ตัวกรองข้อมูลอย่างรวดเร็วในการค้นหาผู้ปฏิบัติงานที่คุณเพิ่งเพิ่มเข้ามาเป็นผู้ขอ</span><span class="sxs-lookup"><span data-stu-id="173fc-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="173fc-125">เลือกผู้ขอ</span><span class="sxs-lookup"><span data-stu-id="173fc-125">Select the requester.</span></span> <span data-ttu-id="173fc-126">รายการผู้จัดเตรียมแสดงผู้ที่มีสิทธิ์ในการสั่งซื้อสินค้าในนามของผู้ขอที่เลือกไว้ในบานหน้าต่างด้านซ้าย </span><span class="sxs-lookup"><span data-stu-id="173fc-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>  <span data-ttu-id="173fc-127">คุณสามารถเพิ่มผู้จัดเตรียมเพิ่มเติมที่นี่</span><span class="sxs-lookup"><span data-stu-id="173fc-127">You can add additional preparers here.</span></span> <span data-ttu-id="173fc-128">มุมมองนี้ให้คุณสามารถให้สิทธิ์ผู้ขอในการสร้างใบขอซื้อในนิติบุคคลและหน่วยปฏิบัติงานที่ไม่ได้เป็นนิติบุคคลหรือหน่วยปฏิบัติงานหลักของบุคคลนั้น</span><span class="sxs-lookup"><span data-stu-id="173fc-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  

