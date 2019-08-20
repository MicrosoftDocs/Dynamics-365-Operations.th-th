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
ms.openlocfilehash: f5f1860907e3cc3c4830cc385771d5924c609ea6
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847539"
---
# <a name="maintenance-request-reports"></a><span data-ttu-id="8b613-103">รายงานคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="8b613-103">Maintenance request reports</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="8b613-104">ในการจัดการสินทรัพย์ คุณสามารถสร้างรายงานสองฉบับที่เกี่ยวข้องกับคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="8b613-104">In Asset Management, you can generate two reports that are related to maintenance requests.</span></span> <span data-ttu-id="8b613-105">รายงานหนึ่งฉบับจะแสดงรายละเอียด และรายงานฉบับอื่นจะแสดงรายการที่สามารถใช้สำหรับการวางแผนและการติดตามผลได้</span><span class="sxs-lookup"><span data-stu-id="8b613-105">One report shows details, and the other report provides a list that can be used for planning and follow-up.</span></span>

## <a name="create-a-maintenance-request-details-report"></a><span data-ttu-id="8b613-106">สร้างรายงานรายละเอียดคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="8b613-106">Create a Maintenance request details report</span></span>

<span data-ttu-id="8b613-107">รายงาน **รายละเอียดคำขอการบำรุงรักษา** จะแสดงข้อมูลต่างๆ ที่เกี่ยวข้องกับคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="8b613-107">The **Maintenance request details** report shows various information that is related to maintenance requests.</span></span>

1. <span data-ttu-id="8b613-108">เลือก **การจัดการสินทรัพย์** \> **รายงาน** \> **คำขอการบำรุงรักษา** \> **รายละเอียดคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="8b613-108">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request details**.</span></span>
2. <span data-ttu-id="8b613-109">บน FastTab **เรกคอร์ดที่จะรวม** คุณสามารถเลือกคำขอการบำรุงรักษาเฉพาะที่จะรวมอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="8b613-109">On the **Records to include** FastTab, you can select specific maintenance requests to include on the report.</span></span>
3. <span data-ttu-id="8b613-110">บน FastTab **รันในเบื้องหลัง** คุณสามารถตั้งค่าการสร้างรายงานเป็นชุดงานตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="8b613-110">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="8b613-111">เลือก **ตกลง** เพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="8b613-111">Select **OK** to generate the report.</span></span>

<span data-ttu-id="8b613-112">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้า **รายละเอียดคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="8b613-112">The following illustration shows an example of the **Maintenance request details** report.</span></span>

![รูปที่ 1](media/09-manage-maintenance-requests.png)

## <a name="create-a-maintenance-request-list-report"></a><span data-ttu-id="8b613-114">สร้างรายงานรายการคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="8b613-114">Create a Maintenance request list report</span></span>

<span data-ttu-id="8b613-115">รายงาน **รายการคำขอการบำรุงรักษา** แสดงรายการของคำขอการบำรุงรักษาทั้งหมดของชนิดคำขอเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8b613-115">The **Maintenance request list** report shows a list of all maintenance requests of the same request type.</span></span>

1. <span data-ttu-id="8b613-116">เลือก **การจัดการสินทรัพย์** \> **รายงาน** \> **คำขอการบำรุงรักษา** \> **รายการคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="8b613-116">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request list**.</span></span>
2. <span data-ttu-id="8b613-117">บน FastTab **เรกคอร์ดที่จะรวม** คุณสามารถทำการเลือกเพื่อกำหนดคำขอการบำรุงรักษาที่จะถูกรวมอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="8b613-117">On the **Records to include** FastTab, you can make selections to define which maintenance requests are included on the report.</span></span>
3. <span data-ttu-id="8b613-118">บน FastTab **รันในเบื้องหลัง** คุณสามารถตั้งค่าการสร้างรายงานเป็นชุดงานตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="8b613-118">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="8b613-119">เลือก **ตกลง** เพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="8b613-119">Select **OK** to generate the report.</span></span>

<span data-ttu-id="8b613-120">ภาพประกอบต่อไปนี้แสดงตัวอย่างของรายงาน **รายการคำขอการบำรุงรักษา** สำหรับคำขอการบำรุงรักษาที่ใช้งานอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8b613-120">The following illustration shows an example of the **Maintenance request list** report for all active maintenance requests.</span></span>

![รูปที่ 2](media/10-manage-maintenance-requests.png)
