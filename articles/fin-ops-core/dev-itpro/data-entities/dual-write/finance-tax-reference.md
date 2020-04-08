---
title: การเข้าถึงข้อมูลอ้างอิงทางการเงินและภาษี
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับการเข้าถึงข้อมูลอ้างอิงทางการเงินและภาษี
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 50f906d62ad6f1e0b79c9c1bb6fcd373ba350c98
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172609"
---
# <a name="access-to-finance-and-tax-reference-data"></a><span data-ttu-id="0f936-103">การเข้าถึงข้อมูลอ้างอิงทางการเงินและภาษี</span><span class="sxs-lookup"><span data-stu-id="0f936-103">Access to finance and tax reference data</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="0f936-104">ธุรกิจทุกแห่งจะทำงานร่วมกับชุดข้อมูลทางการเงินพื้นฐาน เช่น ปีปฏิทินทางการเงิน สกุลเงินที่ธุรกิจมีการทำธุรกรรม บัญชีที่เงินที่จะรันธุรกิจเข้ามาหรือออกไป อัตราภาษี และการชำระเงินผ่านธนาคาร</span><span class="sxs-lookup"><span data-stu-id="0f936-104">Every business works with a basic set of financial data, such as the fiscal calendar year, the currency that business is transacted in, the accounts that the money to run the business comes in to or goes out of, tax rates, and remittance.</span></span> <span data-ttu-id="0f936-105">ข้อมูลนี้มีอยู่ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0f936-105">This data resides in Finance and Operations apps.</span></span> <span data-ttu-id="0f936-106">อย่างไรก็ตาม มีการแสดงต่อ Common Data Service เพื่อให้แอปที่เป็นแบบโมเดลใน Microsoft Dynamics 365 สามารถมีแหล่งข้อมูลเดียวสำหรับการเงินและภาษี</span><span class="sxs-lookup"><span data-stu-id="0f936-106">However, it's exposed to Common Data Service so that model-driven apps in Microsoft Dynamics 365 can have a single source for finance and tax data.</span></span> <span data-ttu-id="0f936-107">ด้วยวิธีนี้ ข้อมูลนี้มีความสม่ำเสมอระหว่างระบบนิเวศของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="0f936-107">In this way, data is uniform across the business ecosystem.</span></span> 

<span data-ttu-id="0f936-108">มีการรวมข้อมูลการเงินและภาษีโดยใช้การแม็ปต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0f936-108">Finance and tax data is integrated by using the following mappings:</span></span>

+ [<span data-ttu-id="0f936-109">บัญชีแยกประเภทแบบรวม</span><span class="sxs-lookup"><span data-stu-id="0f936-109">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="0f936-110">ข้อมูลหลักของภาษีแบบรวม</span><span class="sxs-lookup"><span data-stu-id="0f936-110">Integrated tax master</span></span>](tax-mapping.md)
