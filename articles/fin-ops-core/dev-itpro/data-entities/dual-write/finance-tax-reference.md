---
title: การเข้าถึงข้อมูลอ้างอิงทางการเงินและภาษี
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับการเข้าถึงข้อมูลอ้างอิงทางการเงินและภาษี
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e704e093181ee9b8e712f33746b5434b5ea5dc4e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748628"
---
# <a name="access-to-finance-and-tax-reference-data"></a><span data-ttu-id="535b0-103">การเข้าถึงข้อมูลอ้างอิงทางการเงินและภาษี</span><span class="sxs-lookup"><span data-stu-id="535b0-103">Access to finance and tax reference data</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="535b0-104">ธุรกิจทุกแห่งจะทำงานร่วมกับชุดข้อมูลทางการเงินพื้นฐาน เช่น ปีปฏิทินทางการเงิน สกุลเงินที่ธุรกิจมีการทำธุรกรรม บัญชีที่เงินที่จะรันธุรกิจเข้ามาหรือออกไป อัตราภาษี และการชำระเงินผ่านธนาคาร</span><span class="sxs-lookup"><span data-stu-id="535b0-104">Every business works with a basic set of financial data, such as the fiscal calendar year, the currency that business is transacted in, the accounts that the money to run the business comes in to or goes out of, tax rates, and remittance.</span></span> <span data-ttu-id="535b0-105">ข้อมูลนี้มีอยู่ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="535b0-105">This data resides in Finance and Operations apps.</span></span> <span data-ttu-id="535b0-106">อย่างไรก็ตาม มีการแสดงต่อ Dataverse เพื่อให้แอปที่เป็นแบบโมเดลใน Microsoft Dynamics 365 สามารถมีแหล่งข้อมูลเดียวสำหรับการเงินและภาษี</span><span class="sxs-lookup"><span data-stu-id="535b0-106">However, it's exposed to Dataverse so that model-driven apps in Microsoft Dynamics 365 can have a single source for finance and tax data.</span></span> <span data-ttu-id="535b0-107">ด้วยวิธีนี้ ข้อมูลนี้มีความสม่ำเสมอระหว่างระบบนิเวศของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="535b0-107">In this way, data is uniform across the business ecosystem.</span></span> 

<span data-ttu-id="535b0-108">มีการรวมข้อมูลการเงินและภาษีโดยใช้การแม็ปต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="535b0-108">Finance and tax data is integrated by using the following mappings:</span></span>

+ [<span data-ttu-id="535b0-109">บัญชีแยกประเภทแบบรวม</span><span class="sxs-lookup"><span data-stu-id="535b0-109">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="535b0-110">ข้อมูลหลักของภาษีแบบรวม</span><span class="sxs-lookup"><span data-stu-id="535b0-110">Integrated tax master</span></span>](tax-mapping.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]