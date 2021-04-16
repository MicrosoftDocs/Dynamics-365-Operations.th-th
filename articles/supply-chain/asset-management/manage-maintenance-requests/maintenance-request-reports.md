---
title: รายงานคำขอการบำรุงรักษา
description: หัวข้อนี้อธิบายวิธีการสร้างรายงานคำขอการบำรุงรักษาในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0057d1a2dc00cef2474bc77b76af0d2e2b783d0c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839666"
---
# <a name="maintenance-request-reports"></a><span data-ttu-id="c1671-103">รายงานคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c1671-103">Maintenance request reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c1671-104">ในการจัดการสินทรัพย์ คุณสามารถสร้างรายงานสองฉบับที่เกี่ยวข้องกับคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c1671-104">In Asset Management, you can generate two reports that are related to maintenance requests.</span></span> <span data-ttu-id="c1671-105">รายงานหนึ่งฉบับจะแสดงรายละเอียด และรายงานฉบับอื่นจะแสดงรายการที่สามารถใช้สำหรับการวางแผนและการติดตามผลได้</span><span class="sxs-lookup"><span data-stu-id="c1671-105">One report shows details, and the other report provides a list that can be used for planning and follow-up.</span></span>

## <a name="create-a-maintenance-request-details-report"></a><span data-ttu-id="c1671-106">สร้างรายงานรายละเอียดคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c1671-106">Create a Maintenance request details report</span></span>

<span data-ttu-id="c1671-107">รายงาน **รายละเอียดคำขอการบำรุงรักษา** จะแสดงข้อมูลต่างๆ ที่เกี่ยวข้องกับคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c1671-107">The **Maintenance request details** report shows various information that is related to maintenance requests.</span></span>

1. <span data-ttu-id="c1671-108">เลือก **การจัดการสินทรัพย์** \> **รายงาน** \> **คำขอการบำรุงรักษา** \> **รายละเอียดคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="c1671-108">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request details**.</span></span>
2. <span data-ttu-id="c1671-109">บน FastTab **เรกคอร์ดที่จะรวม** คุณสามารถเลือกคำขอการบำรุงรักษาเฉพาะที่จะรวมอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="c1671-109">On the **Records to include** FastTab, you can select specific maintenance requests to include on the report.</span></span>
3. <span data-ttu-id="c1671-110">บน FastTab **รันในเบื้องหลัง** คุณสามารถตั้งค่าการสร้างรายงานเป็นชุดงานตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="c1671-110">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="c1671-111">เลือก **ตกลง** เพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="c1671-111">Select **OK** to generate the report.</span></span>

<span data-ttu-id="c1671-112">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้า **รายละเอียดคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="c1671-112">The following illustration shows an example of the **Maintenance request details** report.</span></span>

![รายงานรายละเอียดคำขอการบำรุงรักษา](media/09-manage-maintenance-requests.png)

## <a name="create-a-maintenance-request-list-report"></a><span data-ttu-id="c1671-114">สร้างรายงานรายการคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c1671-114">Create a Maintenance request list report</span></span>

<span data-ttu-id="c1671-115">รายงาน **รายการคำขอการบำรุงรักษา** แสดงรายการของคำขอการบำรุงรักษาทั้งหมดของชนิดคำขอเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c1671-115">The **Maintenance request list** report shows a list of all maintenance requests of the same request type.</span></span>

1. <span data-ttu-id="c1671-116">เลือก **การจัดการสินทรัพย์** \> **รายงาน** \> **คำขอการบำรุงรักษา** \> **รายการคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="c1671-116">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request list**.</span></span>
2. <span data-ttu-id="c1671-117">บน FastTab **เรกคอร์ดที่จะรวม** คุณสามารถทำการเลือกเพื่อกำหนดคำขอการบำรุงรักษาที่จะถูกรวมอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="c1671-117">On the **Records to include** FastTab, you can make selections to define which maintenance requests are included on the report.</span></span>
3. <span data-ttu-id="c1671-118">บน FastTab **รันในเบื้องหลัง** คุณสามารถตั้งค่าการสร้างรายงานเป็นชุดงานตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="c1671-118">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="c1671-119">เลือก **ตกลง** เพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="c1671-119">Select **OK** to generate the report.</span></span>

<span data-ttu-id="c1671-120">ภาพประกอบต่อไปนี้แสดงตัวอย่างของรายงาน **รายการคำขอการบำรุงรักษา** สำหรับคำขอการบำรุงรักษาที่ใช้งานอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c1671-120">The following illustration shows an example of the **Maintenance request list** report for all active maintenance requests.</span></span>

![รายงานรายการคำขอการบำรุงรักษา](media/10-manage-maintenance-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]