---
title: แก้ไขการจองสินค้าในการจัดการคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการจองในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828117"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="21828-103">แก้ไขการจองสินค้าในการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="21828-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21828-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการจองในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="21828-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="21828-105">สำหรับหัวข้อที่เกี่ยวกับชุดงานและการลงทะเบียนหมายเลขลำดับประจำสินค้า ดูที่ [แก้ไขปัญหาชุดงานคลังสินค้าและลำดับชั้นการจองหมายเลขลำดับประจำสินค้า](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md)</span><span class="sxs-lookup"><span data-stu-id="21828-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="21828-106">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ไม่สามารถลบการจองได้เนื่องจากมีงานที่สร้างขึ้นซึ่งอาศัยการจอง"</span><span class="sxs-lookup"><span data-stu-id="21828-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="21828-107">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="21828-107">Issue description</span></span>

<span data-ttu-id="21828-108">คุณไม่สามารถยกเลิกการจองสินค้าคงคลังในรายการขายได้ เนื่องจากมีงานที่เปิดอยู่กับรายการ</span><span class="sxs-lookup"><span data-stu-id="21828-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="21828-109">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="21828-109">Issue resolution</span></span>

<span data-ttu-id="21828-110">ตรวจสอบว่างานกลุ่มการบรรจุเปิดอยู่เพื่อนำสินค้าจากสถานีบรรจุไปยังที่ตั้งอื่น (เช่น *Baydoor*)</span><span class="sxs-lookup"><span data-stu-id="21828-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="21828-111">ตรวจทานเรกคอร์ดในหน้า **ล็อกประวัติการสร้างงาน** และ **รายละเอียดงาน** เพื่อตรวจสอบว่ามีการจองสินค้าคงคลังทางกายภาพอย่างไร แล้วทำให้เสร็จสมบูรณ์หรือลบงานเพื่อเพิ่มความสะดวกในการจอง</span><span class="sxs-lookup"><span data-stu-id="21828-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="21828-112">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ปริมาณสินค้าคงคลัง -%1 ไม่สามารถอัพเดตได้เนื่องจากมีรายการความเคลื่อนไหวของสินค้าคงคลังไม่เพียงพอสำหรับสินค้า %2...."</span><span class="sxs-lookup"><span data-stu-id="21828-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="21828-113">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="21828-113">Issue description</span></span>

<span data-ttu-id="21828-114">ปัญหานี้อาจเกิดขึ้นได้ถ้าระบบไม่สามารถอัพเดตปริมาณสินค้าคงคลังได้ เนื่องจากมีรายการความเคลื่อนไหวของสินค้าคงคลังที่มีมิติที่ระบุอยู่ไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="21828-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="21828-115">นี่เป็นข้อความแบบเต็มของข้อความแสดงข้อผิดพลาดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="21828-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="21828-116">ปริมาณสินค้าคงคลัง -%1 ไม่สามารถอัพเดตได้เนื่องจากมีรายการความเคลื่อนไหวของสินค้าคงคลังที่ไม่เพียงพอสำหรับสินค้า %2 ที่มีขนาดมิติ=%3 สี=%4 เพิ่ม=%5 ไซต์=%6 คลังสินค้า=%7 ที่ตั้ง=%8 สถานะของสินค้าคงคลัง=พร้อมใช้งาน ป้ายทะเบียน=%9 หมายเลขชุดงาน=%10 สำหรับรหัสการอ้างอิง %11 บนรหัสล็อต %12</span><span class="sxs-lookup"><span data-stu-id="21828-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="21828-117">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="21828-117">Issue resolution</span></span>

<span data-ttu-id="21828-118">ตรวจสอบให้แน่ใจว่าไม่มีรายการความเคลื่อนไหวของสินค้าคงคลังที่มีการจองปริมาณทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="21828-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="21828-119">ตัวอย่างเช่น ธุรกรรมเหล่านี้อาจเปิดใบสั่งตรวจสอบคุณภาพ เรกคอร์ดการบล็อคสินค้าคงคลัง หรือใบสั่งเอาพุต</span><span class="sxs-lookup"><span data-stu-id="21828-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="21828-120">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ปริมาณคงคลังคงเหลือที่มีอยู่จริง... ไม่สามารถจองได้เนื่องจากมีเพียง 0.00 เท่านั้นที่พร้อมใช้งานในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="21828-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="21828-121">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="21828-121">Issue description</span></span>

<span data-ttu-id="21828-122">ปัญหานี้อาจเกิดขึ้นได้ถ้าระบบไม่สามารถอัพเดตปริมาณสินค้าคงคลังได้ เนื่องจากมีรายการความเคลื่อนไหวของสินค้าคงคลังที่มีมิติที่ระบุอยู่ไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="21828-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="21828-123">นี่เป็นข้อความแบบเต็มของข้อความแสดงข้อผิดพลาดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="21828-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="21828-124">ไซต์คงคลังคงเหลือที่มีอยู่จริง=%1คลังสินค้า=%2 สถานะของสินค้าคงคลัง = พร้อมใช้งานหมายเลขชุดงาน=%3 เจ้าของ=%4: %5 ไม่สามารถจองได้เนื่องจากมีเฉพาะ๐.๐๐เท่านั้นที่พร้อมใช้งานในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="21828-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="21828-125">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="21828-125">Issue resolution</span></span>

<span data-ttu-id="21828-126">ปัญหานี้อาจเกิดจากการเปิดงาน</span><span class="sxs-lookup"><span data-stu-id="21828-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="21828-127">ทำงานให้เสร็จสมบูรณ์หรือได้รับโดยไม่มีการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="21828-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="21828-128">ตรวจสอบให้แน่ใจว่าไม่มีรายการความเคลื่อนไหวของสินค้าคงคลังที่มีการจองปริมาณทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="21828-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="21828-129">ตัวอย่างเช่น ธุรกรรมเหล่านี้อาจเปิดใบสั่งตรวจสอบคุณภาพ เรกคอร์ดการบล็อคสินค้าคงคลัง หรือใบสั่งเอาพุต</span><span class="sxs-lookup"><span data-stu-id="21828-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
