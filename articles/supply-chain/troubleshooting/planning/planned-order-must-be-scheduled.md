---
title: แผนการใบสั่งผลิตต้องจัดตารางการผลิตก่อนที่จะสามารถยืนยันได้
description: เมื่อคุณพยายามยืนยันแผนการใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดที่ระบุว่าต้องจัดตารางการผลิตใบสั่งก่อนที่จะสามารถยืนยันได้
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294195"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="4e8bb-103">แผนการใบสั่งผลิตต้องจัดตารางการผลิตก่อนที่จะสามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="4e8bb-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="4e8bb-104">รหัสข้อผิดพลาด: SYS309802</span><span class="sxs-lookup"><span data-stu-id="4e8bb-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="4e8bb-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="4e8bb-105">Symptoms</span></span>

<span data-ttu-id="4e8bb-106">เมื่อคุณพยายามยืนยันแผนการใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4e8bb-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="4e8bb-107">ต้องจัดกำหนดการแผนการใบสั่งผลิตก่อนที่จะสามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="4e8bb-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="4e8bb-108">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="4e8bb-108">Cause</span></span>

<span data-ttu-id="4e8bb-109">วันที่เริ่มต้นและวันที่สิ้นสุดตามการจัดตารางการผลิตต้องไม่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="4e8bb-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="4e8bb-110">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="4e8bb-110">Resolution</span></span>

<span data-ttu-id="4e8bb-111">หากต้องการระบุวันที่เริ่มต้นและวันที่สิ้นสุดของแผนการใบสั่ง ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4e8bb-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="4e8bb-112">ไปที่ **การวางแผนหลัก \> การวางแผนหลัก \> แผนการใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="4e8bb-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="4e8bb-113">เปิดแผนการใบสั่งที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="4e8bb-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="4e8bb-114">บนแท็บด่วน **ทั่วไป** ในส่วน **ที่จัดตารางการผลิต** ให้ระบุวันที่ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="4e8bb-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
