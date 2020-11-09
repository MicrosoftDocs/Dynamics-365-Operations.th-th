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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: f2602902bfdc201a3dfcd233b802a479b2630005
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997205"
---
# <a name="access-to-finance-and-tax-reference-data"></a><span data-ttu-id="73504-103">การเข้าถึงข้อมูลอ้างอิงทางการเงินและภาษี</span><span class="sxs-lookup"><span data-stu-id="73504-103">Access to finance and tax reference data</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="73504-104">ธุรกิจทุกแห่งจะทำงานร่วมกับชุดข้อมูลทางการเงินพื้นฐาน เช่น ปีปฏิทินทางการเงิน สกุลเงินที่ธุรกิจมีการทำธุรกรรม บัญชีที่เงินที่จะรันธุรกิจเข้ามาหรือออกไป อัตราภาษี และการชำระเงินผ่านธนาคาร</span><span class="sxs-lookup"><span data-stu-id="73504-104">Every business works with a basic set of financial data, such as the fiscal calendar year, the currency that business is transacted in, the accounts that the money to run the business comes in to or goes out of, tax rates, and remittance.</span></span> <span data-ttu-id="73504-105">ข้อมูลนี้มีอยู่ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="73504-105">This data resides in Finance and Operations apps.</span></span> <span data-ttu-id="73504-106">อย่างไรก็ตาม มีการแสดงต่อ Common Data Service เพื่อให้แอปที่เป็นแบบโมเดลใน Microsoft Dynamics 365 สามารถมีแหล่งข้อมูลเดียวสำหรับการเงินและภาษี</span><span class="sxs-lookup"><span data-stu-id="73504-106">However, it's exposed to Common Data Service so that model-driven apps in Microsoft Dynamics 365 can have a single source for finance and tax data.</span></span> <span data-ttu-id="73504-107">ด้วยวิธีนี้ ข้อมูลนี้มีความสม่ำเสมอระหว่างระบบนิเวศของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="73504-107">In this way, data is uniform across the business ecosystem.</span></span> 

<span data-ttu-id="73504-108">มีการรวมข้อมูลการเงินและภาษีโดยใช้การแม็ปต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="73504-108">Finance and tax data is integrated by using the following mappings:</span></span>

+ [<span data-ttu-id="73504-109">บัญชีแยกประเภทแบบรวม</span><span class="sxs-lookup"><span data-stu-id="73504-109">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="73504-110">ข้อมูลหลักของภาษีแบบรวม</span><span class="sxs-lookup"><span data-stu-id="73504-110">Integrated tax master</span></span>](tax-mapping.md)
