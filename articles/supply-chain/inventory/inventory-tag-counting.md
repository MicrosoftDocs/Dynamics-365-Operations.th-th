---
title: "การนับป้ายสินค้าคงคลัง"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับการตรวจนับแท็ก ซึ่งใช้ในการเปรียบเทียบเนื้อหาจริงของคลังสินค้าที่มีปริมาณคงคลังคงเหลือ"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c4df1973ad4ebf710e4be4dfdab6c833d16167e9
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="inventory-tag-counting"></a><span data-ttu-id="94177-103">การนับป้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="94177-103">Inventory tag counting</span></span>

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [retail name](../includes/retail-name.md)]

<span data-ttu-id="94177-104">บทความนี้แสดงข้อมูลเกี่ยวกับการตรวจนับแท็ก ซึ่งใช้ในการเปรียบเทียบเนื้อหาจริงของคลังสินค้าที่มีปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="94177-104">This article provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="94177-105">โดยการสร้างรายการในหน้า **การตรวจนับป้าย** คุณวางหมายเลขป้ายบนสินค้าแต่ละสินค้าคงคลัง เช่น ตัวเลขตั้งแต่ 1 ถึง 500</span><span class="sxs-lookup"><span data-stu-id="94177-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="94177-106">ในระหว่างการตรวจนับ คุณป้อนหมายเลขสินค้าและปริมาณบนป้ายที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="94177-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="94177-107">ป้ายนี้สามารถใช้เป็นพื้นฐานสำหรับข้อมูลนำเข้าในสมุดรายวันการตรวจนับป้าย</span><span class="sxs-lookup"><span data-stu-id="94177-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="94177-108">หลังจากที่คุณลงรายการบัญชีสมุดรายวันการตรวจนับป้าย สมุดรายวันการตรวจนับใหม่จะถูกสร้างขึ้นบนหน้า **การตรวจนับ**</span><span class="sxs-lookup"><span data-stu-id="94177-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="94177-109">สมุดรายวันใหม่จะขึ้นอยู่กับบรรทัดสมุดรายวันการตรวจนับป้ายที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="94177-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="94177-110">เมื่อต้องการตรวจนับป้ายสินค้าโดยเรียงตามมิติสินค้าคงคลังเฉพาะ เลือกมิติบนหน้า**แสดงมิติ** ซึ่งจะแสดงขึ้นเมื่อคุณสร้างสมุดรายวันการตรวจนับป้าย</span><span class="sxs-lookup"><span data-stu-id="94177-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="94177-111">ตัวอย่างเช่น ตรวจนับสินค้าในคลังสินค้าเฉพาะ เลือกกล่องกาเครื่องหมาย **คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="94177-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="94177-112">ถ้าตัวเลื่อน **ล็อคสินค้าในระหว่างการตรวจนับ** บนหน้า**พารามิเตอร์การบริหารสินค้าคงคลังและคลังสินค้า**ที่ถูกเลือก สินค้าที่ไม่ถูกอัพเดตทางกายภาพในระหว่างการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="94177-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="94177-113">อย่างไรก็ตาม สินค้าในสมุดรายวันการตรวจนับป้ายไม่ได้ล็อคอยู่ระหว่างการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="94177-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="94177-114">ธุรกรรมสินค้าคงคลังจะไม่ถูกสร้างขึ้นจนกว่าจะมีการลงรายการบัญชี และโอนย้ายไปยังสมุดรายวันการตรวจนับรายการตรวจนับป้าย</span><span class="sxs-lookup"><span data-stu-id="94177-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="94177-115">ถ้าป้ายถูกป้อนโดยการสุ่มและคุณต้องการระบุแท็กที่หายไป ให้คลิก **แท็ก** หัวคอลัมน์เพื่อเรียงลำดับบรรทัดตามแท็ก</span><span class="sxs-lookup"><span data-stu-id="94177-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

<a name="see-also"></a><span data-ttu-id="94177-116">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="94177-116">See also</span></span>
--------

[<span data-ttu-id="94177-117">การตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="94177-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)

