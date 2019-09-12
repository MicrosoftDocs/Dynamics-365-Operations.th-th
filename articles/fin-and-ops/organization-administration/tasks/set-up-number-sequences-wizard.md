---
title: ตั้งค่าลำดับหมายเลขโดยใช้วิซาร์ด
description: หัวข้อนี้อธิบายวิธีการตั้งค่าลำดับหมายเลขที่จำเป็นทั้งหมดพร้อมกันโดยใช้วิซาร์ด
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f97c4cd6cdb117ebdd67a155478bb6f8d1703541
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867402"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="91ea3-103">ตั้งค่าลำดับหมายเลขโดยใช้วิซาร์ด</span><span class="sxs-lookup"><span data-stu-id="91ea3-103">Set up number sequences using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91ea3-104">ลำดับหมายเลขถูกใช้ในการสร้างรหัสที่สามารถอ่านได้ รหัสเฉพาะสำหรับเร็กคอร์ดข้อมูลหลักและเรกคอร์ดธุรกรรมที่ต้องการ </span><span class="sxs-lookup"><span data-stu-id="91ea3-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="91ea3-105">ข้อมูลหลักหรือเรกคอร์ดธุรกรรมที่จำเป็นต้องมีตัวระบุจะอ้างเป็นการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="91ea3-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="91ea3-106">ก่อนที่คุณจะสามารถสร้างเรกคอร์ดใหม่สำหรับการอ้างอิง คุณต้องตั้งค่าลำดับหมายเลขและเชื่อมโยงกับการอ้างอิงนั้น </span><span class="sxs-lookup"><span data-stu-id="91ea3-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="91ea3-107">หัวข้อนี้อธิบายวิธีการตั้งค่าลำดับหมายเลขที่จำเป็นทั้งหมดพร้อมกันโดยใช้วิซาร์ด</span><span class="sxs-lookup"><span data-stu-id="91ea3-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="91ea3-108">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="91ea3-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="91ea3-109">ไปที่ **การนำทาง > โมดูล > การจัดการองค์กร > ลำดับหมายเลข > ลำดับหมายเลข**</span><span class="sxs-lookup"><span data-stu-id="91ea3-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="91ea3-110">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="91ea3-110">Select **Generate**.</span></span>
3. <span data-ttu-id="91ea3-111">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="91ea3-111">Select **Next**.</span></span>

   - <span data-ttu-id="91ea3-112">บนหน้านี้คุณจะสามารถแก้ไขรหัสประจำตัว ค่าต่ำสุดและค่าสูงสุดได้</span><span class="sxs-lookup"><span data-stu-id="91ea3-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="91ea3-113">นอกจากนี้คุณยังสามารถระบุได้ว่าลำดับหมายเลขต้องต่อเนื่องกันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="91ea3-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="91ea3-114">อย่าเลือกตัวเลือก **ต่อเนื่อง** ถ้าคุณต้องปันส่วนหมายเลขล่วงหน้าสำหรับลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="91ea3-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="91ea3-115">เมื่อต้องการเพิ่มเซ็กเมนต์ขอบเขตไปยังรูปแบบของลำดับหมายเลข ให้เลือกรูปแบบในรายการ และจากนั้น เลือก **รวมขอบเขตในรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="91ea3-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="91ea3-116">ในการลบเซ็กเมนต์ขอบเขตออกจากรูปแบบของลำดับหมายเลข ให้เลือกรูปแบบในรายการ และจากนั้น เลือก **ลบขอบเขตออกจากรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="91ea3-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="91ea3-117">ในการแยกลำดับหมายเลขออกจากการสร้างโดยอัตโนมัติ ให้เลือกลำดับหมายเลขในรายการ และจากนั้น เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="91ea3-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="91ea3-118">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="91ea3-118">Select **Next**.</span></span>
5. <span data-ttu-id="91ea3-119">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="91ea3-119">Select **Finish**.</span></span>

