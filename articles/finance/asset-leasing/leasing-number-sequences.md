---
title: กำหนดลำดับหมายเลข
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างลำดับหมายเลขสำหรับรหัสการเช่า และอธิบายวิธีการสร้างรหัสที่ไม่ซ้ำกันที่ใช้ในกระบวนการประเมินค่าใหม่ของดัชนี
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
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
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 66b48723bbff7f176ef192924e8ea2b96641ba56
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4448617"
---
# <a name="assign-number-sequences"></a><span data-ttu-id="9eb60-104">กำหนดลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="9eb60-104">Assign number sequences</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9eb60-105">หัวข้อนี้จะอธิบายถึงวิธีการสร้างลำดับหมายเลขสำหรับรหัสการเช่า</span><span class="sxs-lookup"><span data-stu-id="9eb60-105">This topic explains how to create number sequences for lease IDs.</span></span> <span data-ttu-id="9eb60-106">และอธิบายวิธีการสร้างรหัสที่ไม่ซ้ำกันที่ใช้ในกระบวนการประเมินค่าใหม่ของดัชนี</span><span class="sxs-lookup"><span data-stu-id="9eb60-106">It also explains how to create unique IDs that are used in the index revaluation process.</span></span>

1. <span data-ttu-id="9eb60-107">ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> พารามิเตอร์การเช่าสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="9eb60-107">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="9eb60-108">เลือกแท็บด้านข้าง **ลำดับหมายเลข**</span><span class="sxs-lookup"><span data-stu-id="9eb60-108">Select the **Number sequences** side tab.</span></span>
3. <span data-ttu-id="9eb60-109">เลือก **ลำดับหมายเลข** ในแถบด้านข้าง</span><span class="sxs-lookup"><span data-stu-id="9eb60-109">Select **Number sequences** in the side bar.</span></span>
4. <span data-ttu-id="9eb60-110">เลือกลำดับหมายเลขสำหรับการอ้างอิง **รหัสการเช่า**</span><span class="sxs-lookup"><span data-stu-id="9eb60-110">Select the number sequence for the **Lease ID** reference.</span></span> <span data-ttu-id="9eb60-111">ลำดับหมายเลขนี้จะใช้ในการสร้างรหัสเฉพาะสำหรับแต่ละสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="9eb60-111">This number sequence will be used to generate the unique identifier for each lease.</span></span>
5. <span data-ttu-id="9eb60-112">เลือกลำดับหมายเลขสำหรับการอ้างอิง **รหัสกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="9eb60-112">Select the number sequence for the **Process ID** reference.</span></span> <span data-ttu-id="9eb60-113">ลำดับหมายเลขนี้จะใช้ในการสร้างรหัสเฉพาะสำหรับแต่ละการประเมินค่าใหม่ของดัชนี</span><span class="sxs-lookup"><span data-stu-id="9eb60-113">This number sequence will be used to generate the unique identifier for each index revaluation process.</span></span>
