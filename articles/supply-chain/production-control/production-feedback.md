---
title: "ผลป้อนกลับของการผลิต"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับผลป้อนกลับการผลิต ซึ่งให้ผลป้อนกลับเกี่ยวกับงานการผลิตของผู้ปฏิบัติงาน บทรวมรายละเอียดเกี่ยวกับวิธีการต่างๆ ที่สามารถปรับปรุงผลป้อนกลับของการผลิต"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1086852bd5193d70e9bde69d349a8d787deee094
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="production-feedback"></a><span data-ttu-id="77851-104">ผลป้อนกลับของการผลิต</span><span class="sxs-lookup"><span data-stu-id="77851-104">Production feedback</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="77851-105">บทความนี้แสดงข้อมูลเกี่ยวกับผลป้อนกลับการผลิต ซึ่งให้ผลป้อนกลับเกี่ยวกับงานการผลิตของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="77851-105">This article provides information about production feedback, which gives workers feedback about production jobs.</span></span> <span data-ttu-id="77851-106">บทรวมรายละเอียดเกี่ยวกับวิธีการต่างๆ ที่สามารถปรับปรุงผลป้อนกลับของการผลิต</span><span class="sxs-lookup"><span data-stu-id="77851-106">The article includes information about the various ways that production feedback can be updated.</span></span>

<span data-ttu-id="77851-107">ผลป้อนกลับของการผลิตให้ผลป้อนกลับของผู้ปฏิบัติงานเกี่ยวกับงานการผลิต</span><span class="sxs-lookup"><span data-stu-id="77851-107">Production feedback gives workers feedback about production jobs.</span></span> <span data-ttu-id="77851-108">บันทึกเวลาและปริมาณการใช้วัสดุในใบสั่งผลิต ปริมาณการดำเนินงาน และสถานะ และข้อผิดพลาดที่ทำให้งานหรือการดำเนินงานล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="77851-108">It records time and material consumption on production orders, operation quantities and status, and errors that cause a job or operation to fail.</span></span> <span data-ttu-id="77851-109">ผลป้อนกลับของการผลิตสามารถอัพเดทในสมุดรายวันที่เกี่ยวข้องกับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="77851-109">Production feedback can be updated in journals that are related to production orders.</span></span> <span data-ttu-id="77851-110">บัตร **งานการผลิต** และ **บัตรกระบวนการผลิต** สมุดรายวันถูกใช้เพื่อรายงานเวลาและปริมาณสำหรับแต่ละงานหรือการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="77851-110">The **Production job card** and **Production route card** journals are used to report time and quantities per job or operation.</span></span> <span data-ttu-id="77851-111">สำหรับการรายงานเกี่ยวกับงานหรือการดำเนินงานสุดท้าย ปริมาณสินค้าในสินค้าสำเร็จรูปสามารถรายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="77851-111">For reporting about the last job or operation, quantities on the finished product can be reported as finished.</span></span> <span data-ttu-id="77851-112">ผลป้อนกลับของการผลิตสามารถอัพเดทบนหน้า **เทอร์มินัลบัตรงาน** และหน้า **อุปกรณ์บัตรงาน**</span><span class="sxs-lookup"><span data-stu-id="77851-112">Production feedback can also be updated on the **Job card terminal** and **Job card device** pages.</span></span> <span data-ttu-id="77851-113">หน้าเหล่านี้เปิดใช้งานผลป้อนกลับการผลิตจะถูกอัพเดตในการผลิตและเป็นส่วนหนึ่งของฟังก์ชันการดำเนินการผลิตในโมดูล **ควบคุมการผลิต**</span><span class="sxs-lookup"><span data-stu-id="77851-113">These pages enable production feedback to be updated on the shop floor and are part of the manufacturing execution functionality in the **Production control** module.</span></span> <span data-ttu-id="77851-114">หน้า**เทอร์มินอลบัตรงาน** มีอินเทอร์เฟสผู้ใช้ที่สามารถจัดโครงแบบที่แสดงรายการของงานที่นำออกใช้ในใบสั่งที่จัดระดับความสำคัญสำหรับพื้นที่งานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="77851-114">The **Job card terminal** page has a configurable user interface that shows a list of the released jobs in a prioritized order for a selected work area.</span></span> <span data-ttu-id="77851-115">ยังมีตัวเลือกขั้นสูง เช่น งานการรวมกลุ่มงานและทีมงาน</span><span class="sxs-lookup"><span data-stu-id="77851-115">It also offers advanced options such as job bundling and team work.</span></span> <span data-ttu-id="77851-116">หน้า **อุปกรณ์บัตรงาน** มีอินเทอร์เฟสผู้ใช้ที่สัมผัสอย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="77851-116">The **Job card device** page has a touch-optimized user interface.</span></span> <span data-ttu-id="77851-117">ผลป้อนกลับของการผลิตในทั้งสองหน้าถูกอัพเดทจากสมุดรายวันการผลิต</span><span class="sxs-lookup"><span data-stu-id="77851-117">Production feedback on both pages is updated from the production journals.</span></span>




