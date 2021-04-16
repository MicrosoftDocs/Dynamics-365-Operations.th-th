---
title: สร้างรายการสมุดรายวันรายเดือนในชุดงาน
description: หัวข้อนี้จะอธิบายเกี่ยวกับวิธีการสร้างรายการสมุดรายวันในชุดงานเพื่อช่วยเพิ่มประสิทธิภาพเมื่อมีการบันทึกค่าใช้จ่ายในการเช่ารายเดือน
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 664001dd6e9da449dec65750da53d58bd27438b4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816039"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="a7b4d-103">สร้างรายการสมุดรายวันรายเดือนในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="a7b4d-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7b4d-104">หัวข้อนี้จะอธิบายเกี่ยวกับวิธีการสร้างรายการสมุดรายวันในชุดงานเพื่อช่วยเพิ่มประสิทธิภาพเมื่อมีการบันทึกค่าใช้จ่ายในการเช่ารายเดือน</span><span class="sxs-lookup"><span data-stu-id="a7b4d-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="a7b4d-105">การประมวลผลชุดงานสามารถใช้ในการสร้างรายการสมุดรายวันจากหลายกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="a7b4d-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="a7b4d-106">รายการสมุดรายวันเหล่านี้อาจรวมถึงการชำระค่าเช่า การตัดบัญชีหนี้สิน การตัดบัญชีสิทธิ์การใช้สินทรัพย์ (ROU) และค่าใช้จ่ายในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="a7b4d-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="a7b4d-107">นอกจากนี้คุณยังสามารถใช้การประมวลผลชุดงานเพื่อทำการรับรู้สัญญาเช่าหลายสัญญาในเวลาเดียวกัน หรือเพื่อสร้างการปรับปรุงการเปลี่ยนแปลงสำหรับสัญญาเช่าหลายสัญญาในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="a7b4d-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="a7b4d-108">เมื่อต้องการตั้งค่าชุดงาน หรือเพื่อประมวลผลใบแจ้งหนี้การชำระเงิน ค่าเสื่อมราคา หรือดอกเบี้ยสำหรับสัญญาเช่าต่าง ๆ ให้ไปที่ **การเช่าสินทรัพย์ \> ประจำงวด \> การสร้างสมุดรายวันชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="a7b4d-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="a7b4d-109">ในกล่องโต้ตอบที่ปรากฏขึ้น คุณสามารถเลือกกำหนดการที่ควรสร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a7b4d-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="a7b4d-110">นอกจากนี้คุณยังสามารถระบุได้ว่าควรรันกระบวนการชุดงานสำหรับเอนทิตีเฉพาะ กลุ่มสัญญาเช่า หรือสมุดบัญชีสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="a7b4d-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="a7b4d-111">ธุรกรรมลำดับต่อมา เช่น กำหนดการตัดบัญชีหนี้สิน การชำระเงิน ค่าเสื่อมราคา และค่าใช้จ่าย จะถูกลงรายการบัญชีเฉพาะหลังจากที่มีการลงรายการบัญชีการรับรู้ครั้งเริ่มต้นสำหรับสัญญาเช่าที่ตรงกันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a7b4d-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="a7b4d-112">รายการสมุดรายวันจะถูกสร้างขึ้น แต่จะไม่มีการลงรายการบัญชีดังกล่าวจนกว่าคุณจะเลือกคำสั่ง **รัน**</span><span class="sxs-lookup"><span data-stu-id="a7b4d-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]