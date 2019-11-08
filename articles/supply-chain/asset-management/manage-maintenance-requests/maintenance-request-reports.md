---
title: รายงานคำขอการบำรุงรักษา
description: หัวข้อนี้อธิบายวิธีการสร้างรายงานคำขอการบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0734416eccf149330b390cce897d2c254f6c698b
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571633"
---
# <a name="maintenance-request-reports"></a><span data-ttu-id="03da4-103">รายงานคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="03da4-103">Maintenance request reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="03da4-104">ในการจัดการสินทรัพย์ คุณสามารถสร้างรายงานสองฉบับที่เกี่ยวข้องกับคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="03da4-104">In Asset Management, you can generate two reports that are related to maintenance requests.</span></span> <span data-ttu-id="03da4-105">รายงานหนึ่งฉบับจะแสดงรายละเอียด และรายงานฉบับอื่นจะแสดงรายการที่สามารถใช้สำหรับการวางแผนและการติดตามผลได้</span><span class="sxs-lookup"><span data-stu-id="03da4-105">One report shows details, and the other report provides a list that can be used for planning and follow-up.</span></span>

## <a name="create-a-maintenance-request-details-report"></a><span data-ttu-id="03da4-106">สร้างรายงานรายละเอียดคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="03da4-106">Create a Maintenance request details report</span></span>

<span data-ttu-id="03da4-107">รายงาน **รายละเอียดคำขอการบำรุงรักษา** จะแสดงข้อมูลต่างๆ ที่เกี่ยวข้องกับคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="03da4-107">The **Maintenance request details** report shows various information that is related to maintenance requests.</span></span>

1. <span data-ttu-id="03da4-108">เลือก **การจัดการสินทรัพย์** \> **รายงาน** \> **คำขอการบำรุงรักษา** \> **รายละเอียดคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="03da4-108">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request details**.</span></span>
2. <span data-ttu-id="03da4-109">บน FastTab **เรกคอร์ดที่จะรวม** คุณสามารถเลือกคำขอการบำรุงรักษาเฉพาะที่จะรวมอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="03da4-109">On the **Records to include** FastTab, you can select specific maintenance requests to include on the report.</span></span>
3. <span data-ttu-id="03da4-110">บน FastTab **รันในเบื้องหลัง** คุณสามารถตั้งค่าการสร้างรายงานเป็นชุดงานตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="03da4-110">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="03da4-111">เลือก **ตกลง** เพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="03da4-111">Select **OK** to generate the report.</span></span>

<span data-ttu-id="03da4-112">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้า **รายละเอียดคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="03da4-112">The following illustration shows an example of the **Maintenance request details** report.</span></span>

![รายงานรายละเอียดคำขอการบำรุงรักษา](media/09-manage-maintenance-requests.png)

## <a name="create-a-maintenance-request-list-report"></a><span data-ttu-id="03da4-114">สร้างรายงานรายการคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="03da4-114">Create a Maintenance request list report</span></span>

<span data-ttu-id="03da4-115">รายงาน **รายการคำขอการบำรุงรักษา** แสดงรายการของคำขอการบำรุงรักษาทั้งหมดของชนิดคำขอเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="03da4-115">The **Maintenance request list** report shows a list of all maintenance requests of the same request type.</span></span>

1. <span data-ttu-id="03da4-116">เลือก **การจัดการสินทรัพย์** \> **รายงาน** \> **คำขอการบำรุงรักษา** \> **รายการคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="03da4-116">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request list**.</span></span>
2. <span data-ttu-id="03da4-117">บน FastTab **เรกคอร์ดที่จะรวม** คุณสามารถทำการเลือกเพื่อกำหนดคำขอการบำรุงรักษาที่จะถูกรวมอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="03da4-117">On the **Records to include** FastTab, you can make selections to define which maintenance requests are included on the report.</span></span>
3. <span data-ttu-id="03da4-118">บน FastTab **รันในเบื้องหลัง** คุณสามารถตั้งค่าการสร้างรายงานเป็นชุดงานตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="03da4-118">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="03da4-119">เลือก **ตกลง** เพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="03da4-119">Select **OK** to generate the report.</span></span>

<span data-ttu-id="03da4-120">ภาพประกอบต่อไปนี้แสดงตัวอย่างของรายงาน **รายการคำขอการบำรุงรักษา** สำหรับคำขอการบำรุงรักษาที่ใช้งานอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="03da4-120">The following illustration shows an example of the **Maintenance request list** report for all active maintenance requests.</span></span>

![รายงานรายการคำขอการบำรุงรักษา](media/10-manage-maintenance-requests.png)
