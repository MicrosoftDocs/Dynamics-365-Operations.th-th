---
title: จำนวนของสมุดบัญชีต่อสมุดรายวัน
description: หัวข้อนี้จะอธิบายความสัมพันธ์ระหว่างสมุดรายวันและสมุดบัญชีสินทรัพย์เมื่อคุณสร้างข้อเสนอการซื้อสินทรัพย์ถาวรหรือการคิดค่าเสื่อมราคาโดยใช้ชุดงาน คุณสามารถกำหนดจำนวนสูงสุดของสมุดบัญชีที่จะรวมสำหรับการซื้อสินทรัพย์แต่ละรายการและสำหรับการคิดค่าเสื่อมราคา
author: moaamer
manager: Ann Beebe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d4ba98cefdc0b555eedfaa56b6a3ca4870b5de93
ms.sourcegitcommit: 65f9e2584c0530b1a71655aae09101691726b47f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "4650686"
---
# <a name="number-of-books-per-journal"></a><span data-ttu-id="36f3d-104">จำนวนของสมุดบัญชีต่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="36f3d-104">Number of books per journal</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36f3d-105">หัวข้อนี้จะอธิบายความสัมพันธ์ระหว่างสมุดรายวันและสมุดบัญชีสินทรัพย์เมื่อคุณสร้างข้อเสนอการซื้อสินทรัพย์ถาวรหรือการคิดค่าเสื่อมราคาโดยใช้ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="36f3d-105">This topic describes the relationship between journals and asset books when you create a fixed asset acquisition or depreciation proposal through a batch job.</span></span> <span data-ttu-id="36f3d-106">คุณสามารถกำหนดจำนวนสูงสุดของสมุดบัญชีที่จะรวมสำหรับการซื้อสินทรัพย์แต่ละรายการและสำหรับการคิดค่าเสื่อมราคาโดยใช้ฟิลด์ในส่วน **จำนวนของสมุดบัญชีต่อสมุดรายวัน** บนแท็บ **ทั่วไป** ของหน้า **พารามิเตอร์สินทรัพย์ถาวร** (**สินทรัพย์ถาวร \> การตั้งค่า \> พารามิเตอร์สินทรัพย์ถาวร**)</span><span class="sxs-lookup"><span data-stu-id="36f3d-106">You can define the maximum number of books that are included for each acquisition and for depreciation by using the fields in the **Number of books per journal** section on the **General** tab of the **Fixed assets parameters** page (**Fixed assets \> Setup \> Fixed assets parameters**).</span></span> <span data-ttu-id="36f3d-107">ฟิลด์เหล่านี้ช่วยให้คุณสามารถกระจายจำนวนของสมุดบัญชีสินทรัพย์สำหรับสมุดรายวันการซื้อสินทรัพย์และสมุดรายวันค่าเสื่อมราคาได้</span><span class="sxs-lookup"><span data-stu-id="36f3d-107">These fields let you distribute the number of asset books per acquisition journal and depreciation journal.</span></span>

<span data-ttu-id="36f3d-108">สำหรับข้อเสนอการซื้อสินทรัพย์ ค่าเริ่มต้นคืออย่างน้อย 10,000 เล่ม</span><span class="sxs-lookup"><span data-stu-id="36f3d-108">For an acquisition proposal, the default value is at least 10,000 books.</span></span> <span data-ttu-id="36f3d-109">สำหรับข้อเสนอค่าเสื่อมราคา ค่าเริ่มต้นคืออย่างน้อย 2,000 เล่ม</span><span class="sxs-lookup"><span data-stu-id="36f3d-109">For a depreciation proposal, the default value is at least 2,000 books.</span></span>

<span data-ttu-id="36f3d-110">ตัวอย่างเช่น ถ้ามีสินทรัพย์ถาวร 4,000 และสองเล่มมีความสัมพันธ์กับสินทรัพย์แต่ละรายการ หนึ่งสมุดบัญชีจะมีการลงรายการบัญชีสมุดรายวันที่เลเยอร์ปัจจุบัน และสมุดบัญชีอื่น ๆ จะถูกลงรายการบัญชีไปที่เลเยอร์ภาษี</span><span class="sxs-lookup"><span data-stu-id="36f3d-110">For example, if there are 4,000 fixed assets, and two books are associated with each asset, one book will be posted to the current layer, and the other book will be posted to the tax layer.</span></span> <span data-ttu-id="36f3d-111">ถ้าคุณได้รับสินทรัพย์ถาวร 4,000 เล่ม ผ่านการประมวลผลชุดงาน ชุดงานที่สร้างสมุดรายวันการซื้อสินทรัพย์ถาวรหนึ่งรายการจะประกอบด้วยสมุดบัญชีสินทรัพย์ 4,000 เล่ม</span><span class="sxs-lookup"><span data-stu-id="36f3d-111">If you acquire 4,000 fixed assets through batch processing, the batch job that creates one fixed asset acquisition journal will contain 4,000 asset books.</span></span>

> [!NOTE]
> <span data-ttu-id="36f3d-112">สมุดรายวันที่สร้างขึ้นจะยังคงถูกใช้จนกว่าชุดงานจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="36f3d-112">The journal that is created will continue to be used until the batch job is completed.</span></span>
>
> <span data-ttu-id="36f3d-113">หนังสือที่สืบทอดมาจะไม่รวมอยู่ในจำนวนสูงสุดของสมุดบัญชีต่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="36f3d-113">The derived books aren't included in the maximum number of books per journal.</span></span>

<span data-ttu-id="36f3d-114">คุณสามารถใช้การประมวลผลชุดงานเพื่อรันการคิดค่าเสื่อมราคาสำหรับชุดสินทรัพย์ที่ซื้อมาเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="36f3d-114">You can use  batch processing to run depreciation for the same set of acquired assets.</span></span> <span data-ttu-id="36f3d-115">ตัวอย่างเช่น ชุดงานสร้างสมุดรายวันค่าเสื่อมราคาสองเล่ม ซึ่งประกอบด้วยสมุดบัญชีสินทรัพย์ 2,000 เล่ม</span><span class="sxs-lookup"><span data-stu-id="36f3d-115">For example, a batch job creates two depreciation journals, each of which consists of 2,000 asset books.</span></span> <span data-ttu-id="36f3d-116">สมุดรายวันแรกจะมีสมุดบัญชีที่สัมพันธ์กับสินทรัพย์ถาวรที่มีหมายเลข 1 ถึง 2,000</span><span class="sxs-lookup"><span data-stu-id="36f3d-116">The first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,000.</span></span> <span data-ttu-id="36f3d-117">สมุดรายวันที่สองจะมีสมุดบัญชีที่สัมพันธ์กับสินทรัพย์ถาวรที่มีหมายเลข 2,001 ถึง 4,000</span><span class="sxs-lookup"><span data-stu-id="36f3d-117">The second journal will then contain books that are associated with the fixed assets that are numbered 2,001 through 4,000.</span></span>

<span data-ttu-id="36f3d-118">งานการประมวลผลชุดงานไม่รวมสมุดบัญชีที่ปิด</span><span class="sxs-lookup"><span data-stu-id="36f3d-118">The batch processing job excludes closed books.</span></span> <span data-ttu-id="36f3d-119">ตัวอย่างเช่น ในชุดงานสำหรับการคิดค่าเสื่อมราคา 10 สมุดบัญชีแรกของ 2,000 เล่มปิดแล้ว</span><span class="sxs-lookup"><span data-stu-id="36f3d-119">For example, in a batch job for depreciation, 10 of the first 2,000 books are closed.</span></span> <span data-ttu-id="36f3d-120">ในกรณีนี้ สมุดรายวันแรกจะมีสมุดบัญชีที่สัมพันธ์กับสินทรัพย์ถาวรที่มีหมายเลข 1 ถึง 2,011</span><span class="sxs-lookup"><span data-stu-id="36f3d-120">In this case, the first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,011.</span></span> <span data-ttu-id="36f3d-121">สมุดรายวันที่สองจะมีสมุดบัญชีที่สัมพันธ์กับสินทรัพย์ถาวรที่มีหมายเลข 2,012 ถึง 4,000</span><span class="sxs-lookup"><span data-stu-id="36f3d-121">The second journal will then contain books that are associated with the fixed assets that are numbered 2,012 through 4,000.</span></span>

<span data-ttu-id="36f3d-122">ขีดจำกัดจำนวนของสมุดบัญชีมีการใช้ถ้าไม่มีรหัสสินทรัพย์ที่ซ้ำกันในสมุดรายวันเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="36f3d-122">The limit on the number of books is applied if duplicate asset IDs don't exist in the same journal.</span></span> <span data-ttu-id="36f3d-123">อย่างไรก็ตาม ถ้ารหัสสินทรัพย์เหมือนกับรหัสสมุดบัญชี หมายเลขจะสามารถเกินจำนวนของสมุดบัญชีต่อสมุดรายวันเพื่อรักษารหัสสินทรัพย์ในสมุดรายวันเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="36f3d-123">However, if the asset ID is the same as the book ID, the number of books per journal can be exceeded to keep the asset ID in the same journal.</span></span>

<span data-ttu-id="36f3d-124">ตัวอย่างเช่น มีรหัสสินทรัพย์ถาวร 5,001 เล่ม สามเล่มเชื่อมโยงกับรหัสสินทรัพย์ถาวรแต่ละรหัส และมีการลงรายการบัญชีสมุดบัญชีสินทรัพย์แต่ละรายการในชั้นของการลงรายการบัญชีเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="36f3d-124">For example, there are 5,001 fixed asset IDs, three books are associated with each fixed asset ID, and each asset book is posted to the same posting layer.</span></span> <span data-ttu-id="36f3d-125">คุณเรียกใช้การคิดค่าเสื่อมราคาเป็นเวลาสามเดือนติดต่อกันโดยไม่มีสรุป</span><span class="sxs-lookup"><span data-stu-id="36f3d-125">You run depreciation for three consecutive months, without summarization.</span></span> <span data-ttu-id="36f3d-126">สมุดรายวันค่าเสื่อมราคาจะถูกสร้างขึ้นโดยผ่านชุดงาน และระบบจะสร้างสมุดรายวันเจ็ดเล่มที่มีรหัสสินทรัพย์ถาวร 667 เล่มและสามเล่มสำหรับรหัสสินทรัพย์ถาวรแต่ละรหัส</span><span class="sxs-lookup"><span data-stu-id="36f3d-126">The depreciation journal will be created through a batch job, and the system will create seven journals that have 667 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="36f3d-127">ผลที่ได้จะเป็น 2,001 เล่ม</span><span class="sxs-lookup"><span data-stu-id="36f3d-127">The result will be 2,001 books.</span></span> <span data-ttu-id="36f3d-128">ดังนั้น ในสามเดือน จะมีบรรทัดสมุดรายวัน 6,003 บรรทัดเพื่อรักษารหัสสินทรัพย์เดียวกันในสมุดรายวันเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="36f3d-128">Therefore, in three months, there will be 6,003 journal lines to maintain the same asset IDs in the same journal.</span></span> <span data-ttu-id="36f3d-129">นอกจากนี้ ระบบจะสร้างสมุดรายวันหนึ่งเล่มที่มีรหัสสินทรัพย์ถาวร 332 และสามเล่มสำหรับรหัสสินทรัพย์ถาวรแต่ละรหัส</span><span class="sxs-lookup"><span data-stu-id="36f3d-129">The system will also create one journal that has 332 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="36f3d-130">ในสามเดือน จะมี 2,988 บรรทัด</span><span class="sxs-lookup"><span data-stu-id="36f3d-130">In three months, there will be 2,988 lines.</span></span>
