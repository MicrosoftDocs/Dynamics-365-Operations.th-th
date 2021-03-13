---
title: ตั้งค่าฟังก์ชันการล็อกออนแบบขยายสำหรับ MPOS และ Cloud POS
description: หัวข้อนี้ครอบคลุมตัวเลือกของคุณสำหรับการตั้งค่าการเข้าสู่ระบบแบบขยายสำหรับ Cloud POS และ Retail Modern POS (MPOS)
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 16835d9e7402c42f852b058150ba8da2b4da3d8b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009860"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a><span data-ttu-id="e4673-103">ตั้งค่าฟังก์ชันการล็อกออนแบบขยายสำหรับ MPOS และ Cloud POS</span><span class="sxs-lookup"><span data-stu-id="e4673-103">Set up extended logon functionality for MPOS and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4673-104">หัวข้อนี้ครอบคลุมตัวเลือกของคุณสำหรับการตั้งค่าการเข้าสู่ระบบแบบขยายสำหรับ Cloud POS และ Retail Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="e4673-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

## <a name="setting-up-extended-logon"></a><span data-ttu-id="e4673-105">การตั้งค่าการเข้าสู่ระบบแบบขยาย</span><span class="sxs-lookup"><span data-stu-id="e4673-105">Setting up extended logon</span></span>

<span data-ttu-id="e4673-106">คุณสามารถค้นหาการตั้งค่าสำหรับตัวพรางบาร์โค้ดที่ **Retail และ Commerce** &gt; **การตั้งค่าช่องทาง** &gt; **การตั้งค่า POS** &gt; **โพรไฟล์ POS** &gt; **โพรไฟล์ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="e4673-106">You can find the setup for bar code masks at **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="e4673-107">FastTab **ฟังก์ชัน** รวมตัวเลือกต่อไปนี้ที่เกี่ยวข้องกับการล็อกออนแบบขยาย</span><span class="sxs-lookup"><span data-stu-id="e4673-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="e4673-108">ล็อกออนบาร์โค้ดพนักงาน</span><span class="sxs-lookup"><span data-stu-id="e4673-108">Staff bar code logon</span></span>

<span data-ttu-id="e4673-109">เมื่อมีการเปิดใช้งานตัวเลือก **ล็อกออนบาร์โค้ดพนักงาน** ผู้ปฏิบัติงานที่ได้กำหนดการล็อกออนแบบขยายให้กับข้อมูลประจำตัวการขายหน้าร้าน (POS) สามารถล็อกออนได้โดยใช้บาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="e4673-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="e4673-110">การล็อกออนด้วยบาร์โค้ดของพนักงานต้องใช้รหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="e4673-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="e4673-111">เมื่อมีการเปิดใช้งานตัวเลือก **การล็อกออนด้วยบาร์โค้ดของพนักงานต้องใช้รหัสผ่าน** การล็อกออนด้วยบาร์โค้ดของพนักงานจะเลือกเฉพาะผู้ปฏิบัติงานที่ถูกกำหนดให้กับการล็อกออนแบบขยายที่จะมีการแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="e4673-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="e4673-112">ผู้ปฏิบัติงานยังต้องป้อนรหัสผ่านเมื่อเปิดใช้งานตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="e4673-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="e4673-113">ล็อกออนบัตรพนักงาน</span><span class="sxs-lookup"><span data-stu-id="e4673-113">Staff card logon</span></span>

<span data-ttu-id="e4673-114">เมื่อมีการเปิดใช้งานตัวเลือก **ล็อกออนด้วยบัตรพนักงาน** ผู้ปฏิบัติงานที่ได้กำหนดการล็อกออนแบบขยายให้กับข้อมูลประจำตัวการขายหน้าร้าน (POS) สามารถล็อกออนได้โดยใช้แถบแม่เหล็ก</span><span class="sxs-lookup"><span data-stu-id="e4673-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="e4673-115">การล็อกออนด้วยบัตรพนักงานต้องใช้รหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="e4673-115">Staff card logon requires password</span></span>

<span data-ttu-id="e4673-116">เมื่อมีการเปิดใช้งานตัวเลือก **การล็อกออนด้วยบัตรของพนักงานต้องใช้รหัสผ่าน** การล็อกออนด้วยบัตรของพนักงานจะเลือกเฉพาะผู้ปฏิบัติงานที่ถูกกำหนดให้กับการล็อกออนแบบขยายที่จะมีการแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="e4673-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="e4673-117">ผู้ปฏิบัติงานยังต้องป้อนรหัสผ่านเมื่อเปิดใช้งานตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="e4673-117">Workers must still enter their password when this option is enabled.</span></span>

## <a name="assigning-an-extended-logon"></a><span data-ttu-id="e4673-118">การกำหนดการล็อกออนแบบขยาย</span><span class="sxs-lookup"><span data-stu-id="e4673-118">Assigning an extended logon</span></span>

<span data-ttu-id="e4673-119">โดยค่าเริ่มต้น เฉพาะผู้จัดการเท่านั้นสามารถกำหนดการล็อกออนแบบขยายให้กับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="e4673-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="e4673-120">เมื่อต้องการกำหนดการล็อกออนแบบขยาย ให้ไปที่ **การล็อกออนเพิ่มเติม** ใน POS</span><span class="sxs-lookup"><span data-stu-id="e4673-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="e4673-121">จากนั้นค้นหาผู้ปฏิบัติงานโดยการป้อนรหัสผู้ปฏิบัติงานของเขาหรือเธอในฟิลด์การค้นหา</span><span class="sxs-lookup"><span data-stu-id="e4673-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="e4673-122">เลือกผู้ปฏิบัติงาน แล้วคลิก **มอบหมาย**</span><span class="sxs-lookup"><span data-stu-id="e4673-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="e4673-123">ในหน้าถัดไป ให้รูดหรือสแกนการล็อกออนแบบขยายเพื่อมอบหมายให้กับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="e4673-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="e4673-124">ถ้ารูดหรือการสแกนถูกอ่านเสร็จเรียบร้อย ปุ่ม **ตกลง** จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e4673-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="e4673-125">คลิก **ตกลง** เพื่อบันทึกการล็อกออนแบบขยายสำหรับผู้ปฏิบัติงานที่นั้น</span><span class="sxs-lookup"><span data-stu-id="e4673-125">Click **OK** to save the extended logon for that worker.</span></span>

## <a name="deleting-an-extended-logon"></a><span data-ttu-id="e4673-126">การลบการล็อกออนแบบขยาย</span><span class="sxs-lookup"><span data-stu-id="e4673-126">Deleting an extended logon</span></span>

<span data-ttu-id="e4673-127">เมื่อต้องการลบการล็อกออนแบบขยายที่กำหนดให้กับผู้ปฏิบัติงาน ให้ค้นหาผู้ปฏิบัติงานโดยใช้การดำเนินงาน **การล็อกออนเพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="e4673-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="e4673-128">เลือกผู้ปฏิบัติงาน แล้วคลิก **ยกเลิกการมอบหมาย**</span><span class="sxs-lookup"><span data-stu-id="e4673-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="e4673-129">ข้อมูลประจำตัวการล็อกออนแบบขยายทั้งหมดที่เชื่อมโยงกับผู้ปฏิบัติงานที่จะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="e4673-129">All extended logon credentials that are associated with that worker are removed.</span></span>

## <a name="extending-extended-logon"></a><span data-ttu-id="e4673-130">การล็อกออนแบบขยายเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e4673-130">Extending extended logon</span></span>

<span data-ttu-id="e4673-131">บริการการล็อกออนสามารถถูกขยายเพื่อสนับสนุนอุปกรณ์การล็อกออนแบบขยายเพิ่มเติมเช่น เครื่องสแกนฝ่ามือ</span><span class="sxs-lookup"><span data-stu-id="e4673-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="e4673-132">สำหรับข้อมูลเพิ่มเติม ให้ดูที่เอกสารความสามารถในการขยาย POS</span><span class="sxs-lookup"><span data-stu-id="e4673-132">For more information, see the POS extensibility documentation.</span></span>

## <a name="using-extended-logon"></a><span data-ttu-id="e4673-133">การใช้การล็อกออนแบบขยาย</span><span class="sxs-lookup"><span data-stu-id="e4673-133">Using extended logon</span></span>

<span data-ttu-id="e4673-134">เมื่อมีการตั้งค่าคอนฟิกการล็อกออนแบบขยาย และผู้ปฏิบัติงานได้รับมอบหมายบาร์โค้ดหรือแถบแม่เหล็ก ผู้ปฏิบัติงานเพียงต้องรูดหรือสแกนบัตรของเขาหรือเธอขณะที่มีการแสดงหน้าการล็อกออน POS</span><span class="sxs-lookup"><span data-stu-id="e4673-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="e4673-135">ถ้าต้องใช้รหัสผ่านด้วยก่อนที่จะสามารถดำเนินการล็อกออนได้ ผู้ปฏิบัติงานจะถูกเตือนให้ใส่รหัสผ่านของเขาหรือเธอ</span><span class="sxs-lookup"><span data-stu-id="e4673-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>
