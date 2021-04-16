---
title: รายงานการวิเคราะห์การแก้ไขปัญหา
description: บทความนี้อธิบายสิ่งที่ต้องทำ ถ้าการเปลี่ยนแปลงข้อมูลของลูกค้าไม่ปรากฏในพื้นที่ทำงานใด ๆ ของลูกค้า
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b500d519d61edfd20456355376e3fc81f16517a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794984"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="62da5-103">รายงานการวิเคราะห์การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="62da5-103">Troubleshoot analytic reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="62da5-104">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="62da5-104">**Issue**</span></span>

<span data-ttu-id="62da5-105">การเปลี่ยนแปลงข้อมูลของลูกค้าไม่ปรากฏขึ้นบนแท็บ **การวิเคราะห์** ของพื้นที่ทำงานใดๆ ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="62da5-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="62da5-106">**สาเหตุ**</span><span class="sxs-lookup"><span data-stu-id="62da5-106">**Cause**</span></span>

<span data-ttu-id="62da5-107">โดยค่าเริ่มต้น รายงาน Microsoft Power BI ถูกรีเฟรชทุกๆ สี่ชั่วโมง ตามกำหนดการของชุดงานการปรับใช้การวัด</span><span class="sxs-lookup"><span data-stu-id="62da5-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="62da5-108">**การแก้ปัญหา**</span><span class="sxs-lookup"><span data-stu-id="62da5-108">**Resolution**</span></span>

<span data-ttu-id="62da5-109">ปัญหานี้อาจจะเป็นแค่เรื่องของช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="62da5-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="62da5-110">ทำตามขั้นตอนเหล่านี้เพื่อเริ่มต้นชุดงาน และอัพเดตพื้นที่ทำงานการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="62da5-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="62da5-111">เปิดหน้า **ชุดงาน** ที่ **การจัดการระบบ \> ลิงค์ \> ชุดงาน \> ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="62da5-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="62da5-112">อีกทางหนึ่งคือ ใช้ค้นหา และป้อน **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="62da5-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="62da5-113">ค้นหางาน **ปรับใช้การวัด** ในรายการ</span><span class="sxs-lookup"><span data-stu-id="62da5-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="62da5-114">เลือก **แก้ไข** ที่ด้านบนของหน้า และตั้งค่าวันที่/เวลาเริ่มต้นตามกำหนดการเป็นค่าที่จะรีเฟรชการวิเคราะห์ให้ใกล้กับเวลาปัจจุบันมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="62da5-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![ชุดงาน](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]