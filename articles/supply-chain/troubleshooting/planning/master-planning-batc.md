---
title: คุณไม่สามารถกรองสินค้าการวางแผนหลักตามมูลค่ากลุ่มความครอบคลุมที่เกี่ยวข้องของสินค้า
description: คุณไม่สามารถกรองสินค้าการวางแผนหลักตามมูลค่ากลุ่มความครอบคลุมที่เกี่ยวข้องของสินค้า
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049493"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="da9d8-103">คุณไม่สามารถกรองสินค้าการวางแผนหลักตามมูลค่ากลุ่มความครอบคลุมที่เกี่ยวข้องของสินค้า</span><span class="sxs-lookup"><span data-stu-id="da9d8-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="da9d8-104">หมายเลข KB: 4612572</span><span class="sxs-lookup"><span data-stu-id="da9d8-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="da9d8-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="da9d8-105">Symptoms</span></span>

<span data-ttu-id="da9d8-106">คุณต้องการกรองข้อมูลสินค้าที่จะรวมอยู่ในชุดงานการวางแผนหลัก ตามค่าของเรกคอร์ดที่เกี่ยวข้องจากตารางความครอบคลุมสินค้า</span><span class="sxs-lookup"><span data-stu-id="da9d8-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="da9d8-107">(ตัวอย่างเช่น คุณต้องการกรองข้อมูลสินค้าตามค่า **ผู้จัดจำหน่าย** และ/หรือ **กลุ่มความครอบคลุม**)</span><span class="sxs-lookup"><span data-stu-id="da9d8-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="da9d8-108">การตั้งค่าตัวกรองข้อมูลเพื่อชุดงานช่วยให้คุณสามารถสร้างตัวเชื่อมจากตาราง **สินค้า** ไปยังตาราง **ความครอบคลุมสินค้า** แล้วระบุค่าฟิลด์จากตารางความครอบคลุมสินค้าในการสอบถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="da9d8-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="da9d8-109">อย่างไรก็ตาม หลังจากที่คุณตั้งค่านี้เสร็จสมบูรณ์แล้ว ระบบจะยังคงสร้างแผนการใบสั่งขึ้นเพื่อความครอบคลุมสินค้าทั้งหมด ไม่ใช่เฉพาะกับสินค้าที่ตรงกับค่าฟิลด์ที่ระบุจากตารางความครอบคลุมสินค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="da9d8-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="da9d8-110">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="da9d8-110">Resolution</span></span>

<span data-ttu-id="da9d8-111">ตัวกรองชุดงานสามารถกรองข้อมูลได้เฉพาะบนสินค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="da9d8-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="da9d8-112">ถึงแม้ว่าคุณจะสามารถเพิ่มตัวเชื่อมเข้าในตาราง **ความครอบคลุมสินค้าได้** การตั้งค่าตัวกรองที่คุณตั้งให้กับตารางนั้นจะไม่มีผลต่อเอาท์พุทการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="da9d8-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="da9d8-113">เมื่อรันไทม์ ระบบจะรันการวางแผนให้กับกลุ่มความครอบคลุมทั้งหมด และการเปลี่ยนแปลงทั้งหมดที่สินค้าที่มีการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="da9d8-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="da9d8-114">หลังจากรวมสินค้าในการรันแล้ว กลุ่มความครอบคลุมใดๆ ที่รวมอยู่ในตัวกรองสินค้าจะไม่มีผลต่อเอาพุตการวางแผน</span><span class="sxs-lookup"><span data-stu-id="da9d8-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
