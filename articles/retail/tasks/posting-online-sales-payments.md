---
title: การลงรายการบัญชีการขายออนไลน์และการชำระเงิน
description: 'กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อการคำนวณใบสั่งขายและการชำระเงินสำหรับธุรกรรมของร้านค้าออนไลน์ '
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "353505"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="69f82-103">การลงรายการบัญชีการขายออนไลน์และการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="69f82-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="69f82-104">กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อการคำนวณใบสั่งขายและการชำระเงินสำหรับธุรกรรมของร้านค้าออนไลน์ </span><span class="sxs-lookup"><span data-stu-id="69f82-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="69f82-105">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="69f82-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="69f82-106">ไปยังพื้นที่ทำงานทั้งหมด > การเงินของร้านค้าปลีก </span><span class="sxs-lookup"><span data-stu-id="69f82-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="69f82-107">คลิกซิงโครไนส์ใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="69f82-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="69f82-108">ในฟิลด์ลำดับชั้นขององค์กร ให้เลือก 'ร้านค้าปลีกโดยเรียงตามภูมิภาค'</span><span class="sxs-lookup"><span data-stu-id="69f82-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="69f82-109">เลือกอย่างใดอย่างหนึ่งระหว่างร้านค้าออนไลน์ หรือเลือกโหนด ถ้าคุณต้องการสร้างชุดงานสำหรับกลุ่มร้านค้า</span><span class="sxs-lookup"><span data-stu-id="69f82-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="69f82-110">คลิกลูกศรเพื่อเพิ่มสิ่งที่คุณเลือก </span><span class="sxs-lookup"><span data-stu-id="69f82-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="69f82-111">คลิกรันในแท็บเบื้องหลัง </span><span class="sxs-lookup"><span data-stu-id="69f82-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="69f82-112">เลือกหรือไม่เลือกกล่องกาเครื่องหมายการประมวลผลชุดงาน</span><span class="sxs-lookup"><span data-stu-id="69f82-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="69f82-113">คลิกการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="69f82-113">Click Recurrence.</span></span>
7. <span data-ttu-id="69f82-114">เลือกตัวเลือกไม่มีวันที่สิ้นสุด </span><span class="sxs-lookup"><span data-stu-id="69f82-114">Select the No end date option.</span></span>
8. <span data-ttu-id="69f82-115">ในฟิลด์ตรวจนับ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="69f82-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="69f82-116">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="69f82-116">Click OK.</span></span>
10. <span data-ttu-id="69f82-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="69f82-117">Click OK.</span></span>

