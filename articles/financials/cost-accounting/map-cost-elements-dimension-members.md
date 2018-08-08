---
title: "แม็ปสมาชิกมิติองค์ประกอบต้นทุนไปยังชุดทั่วไปของมิติ"
description: "การแม็ปสมาชิกมิติองค์ประกอบต้นทุกที่แตกต่างกันกับชุดทั่วไปของสมาชิกมิติองค์ประกอบต้นทุน จะเป็นการผสานข้อมูลลงในรูปแบบทั่วไปสำหรับวัตถุประสงค์ในการวิเคราะห์"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e5c9387d74443ec6ca5dc70ad923b67f962181dc
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="797e4-103">แม็ปสมาชิกมิติองค์ประกอบต้นทุนไปยังชุดทั่วไปของมิติ</span><span class="sxs-lookup"><span data-stu-id="797e4-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="797e4-104">การแม็ปสมาชิกมิติองค์ประกอบต้นทุกที่แตกต่างกันกับชุดทั่วไปของสมาชิกมิติองค์ประกอบต้นทุน จะเป็นการผสานข้อมูลลงในรูปแบบทั่วไปสำหรับวัตถุประสงค์ในการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="797e4-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="797e4-105">ถ้าคุณเป็นบริษัทสากลและเป็นไปตามข้อกำหนดในการลงบัญชีตามกฎหมาย คุณสามารถใช้ผังบัญชีหลายรายการได้</span><span class="sxs-lookup"><span data-stu-id="797e4-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="797e4-106">เมื่อคุณนำเข้าสมาชิกมิติองค์ประกอบต้นทุนจากผังบัญชีอื่น คุณอาจมีการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="797e4-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="797e4-107">อย่างไรก็ตาม บัญชีเหล่านี้อาจมีลักษณะเดียวกัน และคุณอาจต้องการวิเคราะห์ และปันส่วนต้นทุนสำหรับบัญชีเหล่านั้นโดยใช้รูปแบบทั่วไป</span><span class="sxs-lookup"><span data-stu-id="797e4-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="797e4-108">แม็ปสมาชิกมิติองค์ประกอบต้นทุนไปยังรูปแบบทั่วไป</span><span class="sxs-lookup"><span data-stu-id="797e4-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="797e4-109">ตัวอย่างต่อไปนี้แสดงวิธีที่คุณซึ่งเป็นผู้ควบคุมต้นทุนสามารถสร้างมิติองค์ประกอบต้นทุนใหม่ในการลงบัญชีต้นทุนที่แม็ปสมาชิกมิติองค์ประกอบต้นทุนจากโครงสร้างผังบัญชีของสหรัฐอเมริกาและโครงสร้างผังบัญชีของฝรั่งเศสไปยังชุดทั่วไปของสมาชิกมิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="797e4-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="797e4-110">จากนั้นคุณสามารถใช้ชุดทั่วไปของสมาชิกมิติองค์ประกอบต้นทุนในการวิเคราะห์ข้อมูลต้นทุนจากนิติบุคคลสองรายในบัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="797e4-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="797e4-111">ต้นทาง: ผังบัญชีของสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="797e4-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="797e4-112">ต้นทาง: ผังบัญชีของฝรั่งเศส</span><span class="sxs-lookup"><span data-stu-id="797e4-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="797e4-113">ชุดทั่วไปใหม่ของสมาชิกมิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="797e4-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="797e4-114">สมาชิกมิติองค์ประกอบต้นทุนที่นำเข้าจากผังบัญชีของสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="797e4-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="797e4-115">สมาชิกมิติองค์ประกอบต้นทุนที่นำเข้าจากผังบัญชีของฝรั่งเศส</span><span class="sxs-lookup"><span data-stu-id="797e4-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="797e4-116">การแม็ปสมาชิกมิติองค์ประกอบต้นทุนของสหรัฐอเมริกาและฝรั่งเศสไปยังชุดทั่วไป</span><span class="sxs-lookup"><span data-stu-id="797e4-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="797e4-117">5001: การขาย</span><span class="sxs-lookup"><span data-stu-id="797e4-117">5001: Sales</span></span>                                                           | <span data-ttu-id="797e4-118">5001: การขายและการโฆษณา</span><span class="sxs-lookup"><span data-stu-id="797e4-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="797e4-119">5000: การขายและการโฆษณา</span><span class="sxs-lookup"><span data-stu-id="797e4-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="797e4-120">5030: การโฆษณา</span><span class="sxs-lookup"><span data-stu-id="797e4-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="797e4-121">6390: การซื้อสินค้าคงคลัง\*</span><span class="sxs-lookup"><span data-stu-id="797e4-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="797e4-122">7000: ค่าใช้จ่ายในการทำความสะอาด</span><span class="sxs-lookup"><span data-stu-id="797e4-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="797e4-123">7001: ค่าใช้จ่ายในการทำความสะอาด</span><span class="sxs-lookup"><span data-stu-id="797e4-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="797e4-124">7001: ค่าใช้จ่ายในการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="797e4-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="797e4-125">7001: ค่าใช้จ่ายในการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="797e4-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="797e4-126">\*สมาชิกมิติองค์ประกอบต้นทุนของฝรั่งเศสของการซื้อสินค้าคงคลังยังไม่ได้ถูกแม็ป</span><span class="sxs-lookup"><span data-stu-id="797e4-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="797e4-127">การแปลงสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="797e4-127">Currency conversion</span></span>
<span data-ttu-id="797e4-128">ผังบัญชีต่างๆ ที่คุณใช้อาจถูกตั้งค่าให้ใช้สกุลเงินที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="797e4-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="797e4-129">ในกรณีนี้ ตรวจสอบให้แน่ใจว่าได้ระบุการแปลงสกุลเงิน เพื่อให้ข้อมูลต้นทุนมีการประมวลผลโดยใช้สกุลเงินที่ถูกต้อง ตามที่กำหนดไว้ในบัญชีแยกประเภทการบัญชีต้นทุนที่มีการใช้สมาชิกมิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="797e4-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="797e4-130">ในตัวอย่างก่อนหน้านี้ ถ้ามีการใช้ดอลลาร์สหรัฐฯ (USD) ในบัญชีแยกประเภทการบัญชีต้นทุน คุณต้องสร้างการแปลงสกุลเงินจาก USD เป็นยูโร (EUR) เพื่อประมวลผลธุรกรรมสำหรับสมาชิกมิติองค์ประกอบต้นทุนที่มีการแม็ป</span><span class="sxs-lookup"><span data-stu-id="797e4-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="797e4-131">อัพเดตการแม็ปได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="797e4-131">Update mappings at any time</span></span>
<span data-ttu-id="797e4-132">คุณสามารถอัพเดตคำนิยามการแม็ปสำหรับมิติองค์ประกอบต้นทุนได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="797e4-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="797e4-133">เนื่องจากการแม็ปไม่มีวันที่มีผลบังคับ การเปลี่ยนแปลงจะถูกนำมาใช้ในครั้งถัดไปที่คุณประมวลผลธุรกรรมต้นทุน หรือรันการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="797e4-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>




