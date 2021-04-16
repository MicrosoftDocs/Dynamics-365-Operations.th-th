---
title: กำหนดลำดับหมายเลข
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างลำดับหมายเลขสำหรับรหัสการเช่า และอธิบายวิธีการสร้างรหัสที่ไม่ซ้ำกันที่ใช้ในกระบวนการประเมินค่าใหม่ของดัชนี
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
ms.openlocfilehash: a0b5d622df1e5dcdf7f1322328bce7e185f8edb8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819829"
---
# <a name="assign-number-sequences"></a><span data-ttu-id="308b8-104">กำหนดลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="308b8-104">Assign number sequences</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="308b8-105">หัวข้อนี้จะอธิบายถึงวิธีการสร้างลำดับหมายเลขสำหรับรหัสการเช่า</span><span class="sxs-lookup"><span data-stu-id="308b8-105">This topic explains how to create number sequences for lease IDs.</span></span> <span data-ttu-id="308b8-106">และอธิบายวิธีการสร้างรหัสที่ไม่ซ้ำกันที่ใช้ในกระบวนการประเมินค่าใหม่ของดัชนี</span><span class="sxs-lookup"><span data-stu-id="308b8-106">It also explains how to create unique IDs that are used in the index revaluation process.</span></span>

1. <span data-ttu-id="308b8-107">ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> พารามิเตอร์การเช่าสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="308b8-107">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="308b8-108">เลือกแท็บด้านข้าง **ลำดับหมายเลข**</span><span class="sxs-lookup"><span data-stu-id="308b8-108">Select the **Number sequences** side tab.</span></span>
3. <span data-ttu-id="308b8-109">เลือก **ลำดับหมายเลข** ในแถบด้านข้าง</span><span class="sxs-lookup"><span data-stu-id="308b8-109">Select **Number sequences** in the side bar.</span></span>
4. <span data-ttu-id="308b8-110">เลือกลำดับหมายเลขสำหรับการอ้างอิง **รหัสการเช่า**</span><span class="sxs-lookup"><span data-stu-id="308b8-110">Select the number sequence for the **Lease ID** reference.</span></span> <span data-ttu-id="308b8-111">ลำดับหมายเลขนี้จะใช้ในการสร้างรหัสเฉพาะสำหรับแต่ละสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="308b8-111">This number sequence will be used to generate the unique identifier for each lease.</span></span>
5. <span data-ttu-id="308b8-112">เลือกลำดับหมายเลขสำหรับการอ้างอิง **รหัสกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="308b8-112">Select the number sequence for the **Process ID** reference.</span></span> <span data-ttu-id="308b8-113">ลำดับหมายเลขนี้จะใช้ในการสร้างรหัสเฉพาะสำหรับแต่ละการประเมินค่าใหม่ของดัชนี</span><span class="sxs-lookup"><span data-stu-id="308b8-113">This number sequence will be used to generate the unique identifier for each index revaluation process.</span></span>
6. <span data-ttu-id="308b8-114">เลือกลำดับหมายเลขสำหรับการอ้างอิง **รหัสข้อเสนอการสิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="308b8-114">Select the number sequence for the **Termination Proposal ID** reference.</span></span> <span data-ttu-id="308b8-115">ลำดับหมายเลขนี้จะใช้ในการสร้างรหัสเฉพาะสำหรับแต่ละข้อเสนอการสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="308b8-115">This number sequence will be used to generate the unique identifier for each termination proposal.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]