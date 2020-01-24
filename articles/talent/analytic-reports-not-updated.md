---
title: ไม่มีการอัพเดตรายงานการวิเคราะห์
description: หัวข้อนี้อธิบายสิ่งที่ต้องทำ ถ้าการเปลี่ยนแปลงข้อมูลของลูกค้าไม่ปรากฏในพื้นที่ทำงานใดๆ ของลูกค้า
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fc2e6259a8f9d17dc0f7652f207acfa53da76a8d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898584"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="b41c9-103">ไม่มีการอัพเดตรายงานการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="b41c9-103">Analytic reports are not updated</span></span>

<span data-ttu-id="b41c9-104">**ออก**</span><span class="sxs-lookup"><span data-stu-id="b41c9-104">**Issue**</span></span>

<span data-ttu-id="b41c9-105">การเปลี่ยนแปลงข้อมูลของลูกค้าไม่ปรากฏขึ้นบนแท็บ **การวิเคราะห์** ของพื้นที่ทำงานใดๆ ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b41c9-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="b41c9-106">**สาเหตุ**</span><span class="sxs-lookup"><span data-stu-id="b41c9-106">**Cause**</span></span>

<span data-ttu-id="b41c9-107">โดยค่าเริ่มต้น รายงาน Microsoft Power BI ถูกรีเฟรชทุกๆ สี่ชั่วโมง ตามกำหนดการของชุดงานการปรับใช้การวัด</span><span class="sxs-lookup"><span data-stu-id="b41c9-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="b41c9-108">**การแก้ปัญหา**</span><span class="sxs-lookup"><span data-stu-id="b41c9-108">**Resolution**</span></span>

<span data-ttu-id="b41c9-109">ปัญหานี้อาจจะเป็นแค่เรื่องของช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="b41c9-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="b41c9-110">ทำตามขั้นตอนเหล่านี้เพื่อเริ่มต้นชุดงาน และอัพเดตพื้นที่ทำงานการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="b41c9-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="b41c9-111">เปิดหน้า **ชุดงาน** ที่ **การจัดการระบบ \> ลิงค์ \> ชุดงาน \> ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="b41c9-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="b41c9-112">อีกทางหนึ่งคือ ใช้ค้นหา และป้อน **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="b41c9-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="b41c9-113">ค้นหางาน **ปรับใช้การวัด** ในรายการ</span><span class="sxs-lookup"><span data-stu-id="b41c9-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="b41c9-114">เลือก **แก้ไข** ที่ด้านบนของหน้า และตั้งค่าวันที่/เวลาเริ่มต้นตามกำหนดการเป็นค่าที่จะรีเฟรชการวิเคราะห์ให้ใกล้กับเวลาปัจจุบันมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="b41c9-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![ชุดงาน](media/batch-jobs.png)
