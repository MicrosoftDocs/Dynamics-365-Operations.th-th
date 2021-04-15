---
title: การตั้งค่าคอนฟิกและจัดการการบันทึกฐานข้อมูล
description: คุณสามารถติดตามการเปลี่ยนแปลงไปยังตารางและฟิลด์ใน Dynamics 365 Human Resources ด้วยการบันทึกฐานข้อมูล
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d22ff9f3ce68c81f37840342c795d7d162eb027b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801346"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="60636-103">การตั้งค่าคอนฟิกและจัดการการบันทึกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="60636-104">คุณสามารถติดตามการเปลี่ยนแปลงไปยังตารางและฟิลด์ใน Dynamics 365 Human Resources ด้วยการบันทึกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="60636-105">หัวข้อนี้จะอธิบายถึงวิธีการ:</span><span class="sxs-lookup"><span data-stu-id="60636-105">This topic describes how to:</span></span>

- <span data-ttu-id="60636-106">จัดการความปลอดภัยและประสิทธิภาพสำหรับการบันทึกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="60636-107">ตั้งค่าการล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-107">Set up database logging</span></span>
- <span data-ttu-id="60636-108">ล้างข้อมูลล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="60636-109">ภาพรวมของการล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-109">Overview of database logging</span></span>

<span data-ttu-id="60636-110">การล็อกฐานข้อมูลจะติดตามการเปลี่ยนแปลงที่ระบุไปยังตารางและฟิลด์ของ Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="60636-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="60636-111">การเปลี่ยนแปลงเหล่านี้รวมถึงการแทรก การปรับปรุง หรือการลบ</span><span class="sxs-lookup"><span data-stu-id="60636-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="60636-112">การบันทึกฐานข้อมูลจัดเก็บเรกคอร์ดของการเปลี่ยนแปลงไปยังตารางหรือฟิลด์ในตารางล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="60636-113">การใช้ทางธุรกิจของการบันทึกฐานข้อมูลรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="60636-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="60636-114">การสร้างเรกคอร์ดการตรวจสอบของการเปลี่ยนแปลงไปยังตารางที่ระบุซึ่งประกอบด้วยข้อมูลที่เป็นความลับ</span><span class="sxs-lookup"><span data-stu-id="60636-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="60636-115">การติดตามธุรกรรมเดียว</span><span class="sxs-lookup"><span data-stu-id="60636-115">Tracking single transactions.</span></span> <span data-ttu-id="60636-116">การบันทึกฐานข้อมูลไม่ได้มีไว้สำหรับการติดตามธุรกรรมแบบอัตโนมัติที่รันในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="60636-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="60636-117">การรักษาความปลอดภัยสำหรับการบันทึกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-117">Security for database logging</span></span>

<span data-ttu-id="60636-118">ล็อกฐานข้อมูลอาจมีข้อมูลที่สำคัญอยู่ </span><span class="sxs-lookup"><span data-stu-id="60636-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="60636-119">จำกัดการเข้าถึงเพื่อรวมเฉพาะบทบาทความปลอดภัยที่จำเป็นต้องมีการเข้าถึงไปยังล็อกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="60636-120">การบันทึกและประสิทธิภาพการทำงานของฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-120">Database logging and performance</span></span>

<span data-ttu-id="60636-121">ในขณะที่มีค่าจากมุมมองธุรกิจ การบันทึกฐานข้อมูลอาจมีราคาสูงในการใช้และการจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="60636-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="60636-122">ผลกระทบด้านประสิทธิภาพการทำงานของการบันทึกฐานข้อมูลรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="60636-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="60636-123">ตารางล็อกฐานข้อมูลสามารถเติบโตได้อย่างรวดเร็ว และทำให้เกิดการเพิ่มขึ้นของขนาดของฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="60636-124">การเติบโตจะขึ้นอยู่กับจำนวนของข้อมูลที่บันทึกซึ่งคุณตัดสินใจที่จะเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="60636-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="60636-125">โดยค่าเริ่มต้น ตารางล็อกฐานข้อมูลจะรักษาเพียง 30 วันของข้อมูลล็อก</span><span class="sxs-lookup"><span data-stu-id="60636-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="60636-126">การบันทึกฐานข้อมูลอาจส่งผลกระทบในทางลบต่อกระบวนการอัตโนมัติที่รันเป็นเวลานาน เช่น การนำเข้าข้อมูลที่รันเป็นเวลานาน</span><span class="sxs-lookup"><span data-stu-id="60636-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="60636-127">แนวทางปฏิบัติ</span><span class="sxs-lookup"><span data-stu-id="60636-127">Best practices</span></span>

<span data-ttu-id="60636-128">เพื่อเพิ่มประสิทธิภาพการทำงาน ให้จำกัดรายการล็อกโดยการเลือกฟิลด์เฉพาะเพื่อบันทึก แทนที่จะเลือกตารางทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="60636-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="60636-129">เพื่อช่วยในการรักษาประสิทธิภาพโดยรวม การบันทึกฐานข้อมูลจะจำกัดไว้ 20 ตาราง</span><span class="sxs-lookup"><span data-stu-id="60636-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="60636-130">สามารถบันทึกได้เฉพาะการปรับปรุงสำหรับฟิลด์แต่ละฟิลด์</span><span class="sxs-lookup"><span data-stu-id="60636-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="60636-131">ตั้งค่าการล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-131">Set up database logging</span></span>

<span data-ttu-id="60636-132">คุณสามารถใช้วิซาร์ด **การบันทึกการเปลี่ยนแปลงฐานข้อมูล** เพื่อตั้งค่าการบันทึกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="60636-133">วิซาร์ดจะมีวิธีที่ยืดหยุ่นในการตั้งค่าการบันทึกสำหรับตารางหรือฟิลด์</span><span class="sxs-lookup"><span data-stu-id="60636-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="60636-134">ไปที่ **การจัดการระบบ > ลิงค์ > ฐานข้อมูล > การตั้งค่าล็อกฐานข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="60636-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="60636-135">เลือก **สร้าง** เพื่อเริ่มต้นวิซาร์ด **การบันทึกการเปลี่ยนแปลงฐานข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="60636-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="60636-136">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="60636-136">Select **Next**.</span></span> 
3. <span data-ttu-id="60636-137">บนหน้า **ตารางและฟิลด์** ของวิซาร์ด ให้เลือกตารางและฟิลด์ที่คุณต้องการเปิดใช้งานการบันทึกล็อกฐานข้อมูล และเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="60636-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="60636-138">การบันทึกล็อกฐานข้อมูลไม่พร้อมใช้งานบนตารางทั้งหมดในฐานข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="60636-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="60636-139">การเลือก **แสดงตารางทั้งหมด** ใต้รายการ จะขยายรายการของตารางและฟิลด์เพื่อแสดงตารางฐานข้อมูลทั้งหมดที่ซึ่งการบันทึกล็อกฐานข้อมูลจะพร้อมใช้งาน แต่จะเป็นชุดย่อยของรายการของตารางฐานข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="60636-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="60636-140">บนหน้า **ชนิดของการเปลี่ยนแปลง** ของวิซาร์ด ให้เลือกการดําเนินงานข้อมูลที่คุณต้องการติดตามการเปลี่ยนแปลงสำหรับแต่ละตารางและแต่ละฟิลด์ และเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="60636-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="60636-141">โปรดดูตารางข้างล่างนี้สำหรับรายละเอียดของการดําเนินงานข้อมูลที่พร้อมใช้งานสำหรับการบันทึกล็อก</span><span class="sxs-lookup"><span data-stu-id="60636-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="60636-142">บนหน้า **ทำให้เสร็จสิ้น** ให้ทบทวนการเปลี่ยนแปลงที่จะมีการดำเนินการ และเลือก **ทำให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="60636-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="60636-143">การดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="60636-143">Operation</span></span> | <span data-ttu-id="60636-144">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="60636-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="60636-145">ติดตามธุรกรรมใหม่</span><span class="sxs-lookup"><span data-stu-id="60636-145">Track new transactions</span></span> | <span data-ttu-id="60636-146">สร้างล็อกสำหรับเรกคอร์ดใหม่ที่ถูกสร้างขึ้นในตาราง</span><span class="sxs-lookup"><span data-stu-id="60636-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="60636-147">อัพเดต</span><span class="sxs-lookup"><span data-stu-id="60636-147">Update</span></span> | <span data-ttu-id="60636-148">สร้างล็อกสำหรับการอัพเดตไปยังเรกคอร์ดตาราง หรือการอัพเดตไปยังฟิลด์ที่เลือกแต่ละฟิลด์ในตาราง</span><span class="sxs-lookup"><span data-stu-id="60636-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="60636-149">ถ้าคุณเลือกที่จะบันทึกการอัพเดตสำหรับตาราง จะมีการสร้างเรกคอร์ดล็อกทุกครั้งที่มีการอัพเดตฟิลด์ของเรกคอร์ดใดๆ ในตาราง</span><span class="sxs-lookup"><span data-stu-id="60636-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="60636-150">ถ้าคุณเลือกที่จะบันทึกการอัพเดตสำหรับฟิลด์ที่ระบุ จะมีการสร้างเรกคอร์ดล็อกเฉพาะเมื่อมีการอัพเดตฟิลด์เหล่านั้นของเรกคอร์ดตารางเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="60636-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="60636-151">Delete</span><span class="sxs-lookup"><span data-stu-id="60636-151">Delete</span></span> | <span data-ttu-id="60636-152">สร้างล็อกสำหรับเรกคอร์ดที่ลบออกจากตาราง</span><span class="sxs-lookup"><span data-stu-id="60636-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="60636-153">เปลี่ยนชื่อคีย์</span><span class="sxs-lookup"><span data-stu-id="60636-153">Rename key</span></span> | <span data-ttu-id="60636-154">สร้างเรกคอร์ดล็อก เมื่อมีการเปลี่ยนชื่อคีย์ตาราง</span><span class="sxs-lookup"><span data-stu-id="60636-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="60636-155">ล้างข้อมูลล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-155">Clean up database logs</span></span>

<span data-ttu-id="60636-156">คุณสามารถลบทั้งหมดหรือบางส่วนของล็อกฐานข้อมูล โดยใช้ตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="60636-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="60636-157">เลือกล็อกทั้งหมดสำหรับตารางเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="60636-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="60636-158">เลือกชนิดเฉพาะของล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60636-158">Select specific types of database log.</span></span>
- <span data-ttu-id="60636-159">เลือกวันที่และเวลาที่ล็อกถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="60636-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="60636-160">ถ้าต้องการตั้งค่าการล้างข้อมูลล็อกฐานข้อมูล ให้ปฏิบัติตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="60636-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="60636-161">ไปที่ **การจัดการระบบ > ลิงค์ > ฐานข้อมูล > ล็อกฐานข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="60636-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="60636-162">เลือก **ล้างข้อมูลล็อก**</span><span class="sxs-lookup"><span data-stu-id="60636-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="60636-163">เลือกวิธีในการเลือกล็อกที่จะลบ โดยการป้อนตัวเลือกอย่างใดอย่างหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="60636-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="60636-164">ID ตาราง</span><span class="sxs-lookup"><span data-stu-id="60636-164">Table ID</span></span>
   - <span data-ttu-id="60636-165">ชนิดของล็อก</span><span class="sxs-lookup"><span data-stu-id="60636-165">Type of log</span></span>
   - <span data-ttu-id="60636-166">วันที่และเวลาที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="60636-166">Created date and time</span></span>

3. <span data-ttu-id="60636-167">ใช้แท็บ **การล้างข้อมูลล็อกฐานข้อมูล** เพื่อกำหนดเวลาที่จะรันงานการล้างข้อมูลล็อก</span><span class="sxs-lookup"><span data-stu-id="60636-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="60636-168">โดยค่าเริ่มต้น ล็อกฐานข้อมูลจะพร้อมใช้งานเป็นเวลา 30 วัน</span><span class="sxs-lookup"><span data-stu-id="60636-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
