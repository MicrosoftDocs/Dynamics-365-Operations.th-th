---
title: สินค้าไม่สามารถมี BOM หรือสูตร
description: เมื่อคุณพยายามยืนยันใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดระหว่างการตรวจสอบความถูกต้องของสินค้า ระบุว่าสินค้าไม่สามารถมีสูตรการผลิต (BOM) หรือสูตร
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294191"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="3c601-104">สินค้าไม่สามารถมี BOM หรือสูตร</span><span class="sxs-lookup"><span data-stu-id="3c601-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="3c601-105">รหัสข้อผิดพลาด: PRO2614</span><span class="sxs-lookup"><span data-stu-id="3c601-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="3c601-106">อาการ</span><span class="sxs-lookup"><span data-stu-id="3c601-106">Symptoms</span></span>

<span data-ttu-id="3c601-107">เมื่อคุณพยายามยืนยันใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดระหว่างการตรวจสอบความถูกต้องของสินค้าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3c601-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="3c601-108">สินค้าไม่สามารถมี BOM หรือสูตร</span><span class="sxs-lookup"><span data-stu-id="3c601-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="3c601-109">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="3c601-109">Resolution</span></span>

<span data-ttu-id="3c601-110">สินค้าที่มีสูตรการผลิต (BOM) หรือสูตรต้องเป็นชนิด *การวางแผนสินค้า* *BOM* หรือ *สูตร*</span><span class="sxs-lookup"><span data-stu-id="3c601-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="3c601-111">เมื่อต้องการเปลี่ยนชนิดของสินค้า ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="3c601-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="3c601-112">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="3c601-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="3c601-113">เปิดผลิตภัณฑ์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3c601-113">Open the relevant product.</span></span>
1. <span data-ttu-id="3c601-114">บนแท็บด่วน **วิศวกรรม** ตั้งค่าฟิลด์ **ชนิดผลิตภัณฑ์** เป็น *การวางแผนสินค้า* *BOM* หรือ *สูตร*</span><span class="sxs-lookup"><span data-stu-id="3c601-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>
