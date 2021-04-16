---
title: กำหนดเวอร์ชัน BOM
description: ในระหว่างการกระจายความต้องการ ถ้าสินค้ามีชนิดใบสั่งเริ่มต้นของการผลิต กลไกจัดการการวางแผนจะหารุ่น BOM ที่ถูกต้องตามไซต์
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4fd5f28d0ee85c267ea6a86a1452fbacc824620
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833628"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="3973a-103">กำหนดเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="3973a-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3973a-104">ในระหว่างการกระจายความต้องการ ถ้าสินค้ามีชนิดใบสั่งเริ่มต้นของการผลิต กลไกจัดการการวางแผนจะหารุ่น BOM ที่ถูกต้องตามไซต์</span><span class="sxs-lookup"><span data-stu-id="3973a-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="3973a-105">มิติไซต์จะทราบเสมอ และระบุในธุรกรรมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="3973a-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="3973a-106">กระบวนการต่อไปนี้จะใช้เพื่อกำหนดรุ่น BOM ที่จะใช้:</span><span class="sxs-lookup"><span data-stu-id="3973a-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="3973a-107">ถ้ามีรุ่น BOMที่กำหนดสำหรับสินค้าที่ไซต์ความต้องการ BOM เฉพาะไซต์จะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="3973a-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="3973a-108">ถ้าไม่มีรุ่น BOM เฉพาะไซต์ที่กำหนดสำหรับสินค้าที่ไซต์ความต้องการ BOM ทั่วไปจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="3973a-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="3973a-109">BOM ทั่วไปไม่ได้ระบุไซต์ และสามารถใช้ได้กับหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="3973a-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="3973a-110">ถ้ามี BOM ทั่วไป ก็จะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="3973a-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="3973a-111">ถ้าไม่มีรุ่น BOM ทั่วไปที่จะใช้ การกระจายความต้องการจะหยุดที่จุดนี้</span><span class="sxs-lookup"><span data-stu-id="3973a-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="3973a-112">BOM เวอร์ชันที่ถูกต้อง ไม่ว่าจะเป็นแบบเฉพาะไซต์หรือทั่วไป ต้องมีลักษณะตรงตามเงื่อนไขเกี่ยวกับวันที่และปริมาณที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="3973a-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]