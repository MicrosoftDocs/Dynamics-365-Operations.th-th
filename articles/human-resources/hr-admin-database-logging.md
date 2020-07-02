---
title: การตั้งค่าคอนฟิกและจัดการการบันทึกฐานข้อมูล
description: คุณสามารถติดตามการเปลี่ยนแปลงไปยังตารางและฟิลด์ใน Dynamics 365 Human Resources ด้วยการบันทึกฐานข้อมูล
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443601"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="492df-103">การตั้งค่าคอนฟิกและจัดการการบันทึกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-103">Configure and manage database logging</span></span>

<span data-ttu-id="492df-104">คุณสามารถติดตามการเปลี่ยนแปลงไปยังตารางและฟิลด์ใน Dynamics 365 Human Resources ด้วยการบันทึกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="492df-105">หัวข้อนี้จะอธิบายถึงวิธีการ:</span><span class="sxs-lookup"><span data-stu-id="492df-105">This topic describes how to:</span></span>

- <span data-ttu-id="492df-106">จัดการความปลอดภัยและประสิทธิภาพสำหรับการบันทึกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="492df-107">ตั้งค่าการล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-107">Set up database logging</span></span>
- <span data-ttu-id="492df-108">ล้างข้อมูลล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="492df-109">ภาพรวมของการล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-109">Overview of database logging</span></span>

<span data-ttu-id="492df-110">การล็อกฐานข้อมูลจะติดตามการเปลี่ยนแปลงที่ระบุไปยังตารางและฟิลด์ของ Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="492df-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="492df-111">การเปลี่ยนแปลงเหล่านี้รวมถึงการแทรก การปรับปรุง หรือการลบ</span><span class="sxs-lookup"><span data-stu-id="492df-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="492df-112">การบันทึกฐานข้อมูลจัดเก็บเรกคอร์ดของการเปลี่ยนแปลงไปยังตารางหรือฟิลด์ในตารางล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="492df-113">การใช้ทางธุรกิจของการบันทึกฐานข้อมูลรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="492df-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="492df-114">การสร้างเรกคอร์ดการตรวจสอบของการเปลี่ยนแปลงไปยังตารางที่ระบุซึ่งประกอบด้วยข้อมูลที่เป็นความลับ</span><span class="sxs-lookup"><span data-stu-id="492df-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="492df-115">การติดตามธุรกรรมเดียว</span><span class="sxs-lookup"><span data-stu-id="492df-115">Tracking single transactions.</span></span> <span data-ttu-id="492df-116">การบันทึกฐานข้อมูลไม่ได้มีไว้สำหรับการติดตามธุรกรรมแบบอัตโนมัติที่รันในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="492df-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="492df-117">การรักษาความปลอดภัยสำหรับการบันทึกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-117">Security for database logging</span></span>

<span data-ttu-id="492df-118">ล็อกฐานข้อมูลอาจมีข้อมูลที่สำคัญอยู่ </span><span class="sxs-lookup"><span data-stu-id="492df-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="492df-119">จำกัดการเข้าถึงเพื่อรวมเฉพาะบทบาทความปลอดภัยที่จำเป็นต้องมีการเข้าถึงไปยังล็อกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="492df-120">การบันทึกและประสิทธิภาพการทำงานของฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-120">Database logging and performance</span></span>

<span data-ttu-id="492df-121">ในขณะที่มีค่าจากมุมมองธุรกิจ การบันทึกฐานข้อมูลอาจมีราคาสูงในการใช้และการจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="492df-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="492df-122">ผลกระทบด้านประสิทธิภาพการทำงานของการบันทึกฐานข้อมูลรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="492df-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="492df-123">ตารางล็อกฐานข้อมูลสามารถเติบโตได้อย่างรวดเร็ว และทำให้เกิดการเพิ่มขึ้นของขนาดของฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="492df-124">การเติบโตจะขึ้นอยู่กับจำนวนของข้อมูลที่บันทึกซึ่งคุณตัดสินใจที่จะเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="492df-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="492df-125">โดยค่าเริ่มต้น ตารางล็อกฐานข้อมูลจะรักษาเพียง 30 วันของข้อมูลล็อก</span><span class="sxs-lookup"><span data-stu-id="492df-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="492df-126">การบันทึกฐานข้อมูลอาจส่งผลกระทบในทางลบต่อกระบวนการอัตโนมัติที่รันเป็นเวลานาน เช่น การนำเข้าข้อมูลที่รันเป็นเวลานาน</span><span class="sxs-lookup"><span data-stu-id="492df-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="492df-127">แนวทางปฏิบัติ</span><span class="sxs-lookup"><span data-stu-id="492df-127">Best practices</span></span>

<span data-ttu-id="492df-128">เพื่อเพิ่มประสิทธิภาพการทำงาน ให้จำกัดรายการล็อกโดยการเลือกฟิลด์เฉพาะเพื่อบันทึก แทนที่จะเลือกตารางทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="492df-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="492df-129">เพื่อช่วยในการรักษาประสิทธิภาพโดยรวม การบันทึกฐานข้อมูลจะจำกัดไว้ 20 ตาราง</span><span class="sxs-lookup"><span data-stu-id="492df-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="492df-130">สามารถบันทึกได้เฉพาะการปรับปรุงสำหรับฟิลด์แต่ละฟิลด์</span><span class="sxs-lookup"><span data-stu-id="492df-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="492df-131">ตั้งค่าการล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-131">Set up database logging</span></span>

<span data-ttu-id="492df-132">คุณสามารถใช้วิซาร์ด **การบันทึกการเปลี่ยนแปลงฐานข้อมูล** เพื่อตั้งค่าการบันทึกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="492df-133">วิซาร์ดจะมีวิธีที่ยืดหยุ่นในการตั้งค่าการบันทึกสำหรับตารางหรือฟิลด์</span><span class="sxs-lookup"><span data-stu-id="492df-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="492df-134">ไปที่ **การจัดการระบบ > ลิงค์ > ฐานข้อมูล > การตั้งค่าล็อกฐานข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="492df-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="492df-135">เลือก **สร้าง** เพื่อเริ่มต้นวิซาร์ด **การบันทึกการเปลี่ยนแปลงฐานข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="492df-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="492df-136">ดำเนินการตามวิซาร์ดให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="492df-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="492df-137">ล้างข้อมูลล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-137">Clean up database logs</span></span>

<span data-ttu-id="492df-138">คุณสามารถลบทั้งหมดหรือบางส่วนของล็อกฐานข้อมูล โดยใช้ตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="492df-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="492df-139">เลือกล็อกทั้งหมดสำหรับตารางเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="492df-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="492df-140">เลือกชนิดเฉพาะของล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="492df-140">Select specific types of database log.</span></span>
- <span data-ttu-id="492df-141">เลือกวันที่และเวลาที่ล็อกถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="492df-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="492df-142">ถ้าต้องการตั้งค่าการล้างข้อมูลล็อกฐานข้อมูล ให้ปฏิบัติตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="492df-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="492df-143">ไปที่ **การจัดการระบบ > ลิงค์ > ฐานข้อมูล > ล็อกฐานข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="492df-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="492df-144">เลือก **ล้างข้อมูลล็อก**</span><span class="sxs-lookup"><span data-stu-id="492df-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="492df-145">เลือกวิธีในการเลือกล็อกที่จะลบ โดยการป้อนตัวเลือกอย่างใดอย่างหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="492df-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="492df-146">ID ตาราง</span><span class="sxs-lookup"><span data-stu-id="492df-146">Table ID</span></span>
   - <span data-ttu-id="492df-147">ชนิดของล็อก</span><span class="sxs-lookup"><span data-stu-id="492df-147">Type of log</span></span>
   - <span data-ttu-id="492df-148">วันที่และเวลาที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="492df-148">Created date and time</span></span>

3. <span data-ttu-id="492df-149">ใช้แท็บ **การล้างข้อมูลล็อกฐานข้อมูล** เพื่อกำหนดเวลาที่จะรันงานการล้างข้อมูลล็อก</span><span class="sxs-lookup"><span data-stu-id="492df-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="492df-150">โดยค่าเริ่มต้น ล็อกฐานข้อมูลจะพร้อมใช้งานเป็นเวลา 30 วัน</span><span class="sxs-lookup"><span data-stu-id="492df-150">By default, database logs are available for 30 days.</span></span>
