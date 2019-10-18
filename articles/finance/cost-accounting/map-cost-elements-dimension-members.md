---
title: แม็ปสมาชิกมิติองค์ประกอบต้นทุนไปยังชุดทั่วไปของมิติ
description: การแม็ปสมาชิกมิติองค์ประกอบต้นทุกที่แตกต่างกันกับชุดทั่วไปของสมาชิกมิติองค์ประกอบต้นทุน จะเป็นการผสานข้อมูลลงในรูปแบบทั่วไปสำหรับวัตถุประสงค์ในการวิเคราะห์
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: deb9b5aab9cd69270c78d4e1ea0e2a6cac6ac370
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180159"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="02560-103">แม็ปสมาชิกมิติองค์ประกอบต้นทุนไปยังชุดทั่วไปของมิติ</span><span class="sxs-lookup"><span data-stu-id="02560-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02560-104">การแม็ปสมาชิกมิติองค์ประกอบต้นทุกที่แตกต่างกันกับชุดทั่วไปของสมาชิกมิติองค์ประกอบต้นทุน จะเป็นการผสานข้อมูลลงในรูปแบบทั่วไปสำหรับวัตถุประสงค์ในการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="02560-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="02560-105">ถ้าคุณเป็นบริษัทสากลและเป็นไปตามข้อกำหนดในการลงบัญชีตามกฎหมาย คุณสามารถใช้ผังบัญชีหลายรายการได้</span><span class="sxs-lookup"><span data-stu-id="02560-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="02560-106">เมื่อคุณนำเข้าสมาชิกมิติองค์ประกอบต้นทุนจากผังบัญชีอื่น คุณอาจมีการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="02560-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="02560-107">อย่างไรก็ตาม บัญชีเหล่านี้อาจมีลักษณะเดียวกัน และคุณอาจต้องการวิเคราะห์ และปันส่วนต้นทุนสำหรับบัญชีเหล่านั้นโดยใช้รูปแบบทั่วไป</span><span class="sxs-lookup"><span data-stu-id="02560-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="02560-108">แม็ปสมาชิกมิติองค์ประกอบต้นทุนไปยังรูปแบบทั่วไป</span><span class="sxs-lookup"><span data-stu-id="02560-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="02560-109">ตัวอย่างต่อไปนี้แสดงวิธีที่คุณซึ่งเป็นผู้ควบคุมต้นทุนสามารถสร้างมิติองค์ประกอบต้นทุนใหม่ในการลงบัญชีต้นทุนที่แม็ปสมาชิกมิติองค์ประกอบต้นทุนจากโครงสร้างผังบัญชีของสหรัฐอเมริกาและโครงสร้างผังบัญชีของฝรั่งเศสไปยังชุดทั่วไปของสมาชิกมิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="02560-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="02560-110">จากนั้นคุณสามารถใช้ชุดทั่วไปของสมาชิกมิติองค์ประกอบต้นทุนในการวิเคราะห์ข้อมูลต้นทุนจากนิติบุคคลสองรายในบัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="02560-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="02560-111">ต้นทาง: ผังบัญชีของสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="02560-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="02560-112">ต้นทาง: ผังบัญชีของฝรั่งเศส</span><span class="sxs-lookup"><span data-stu-id="02560-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="02560-113">ชุดทั่วไปใหม่ของสมาชิกมิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="02560-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="02560-114">สมาชิกมิติองค์ประกอบต้นทุนที่นำเข้าจากผังบัญชีของสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="02560-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="02560-115">สมาชิกมิติองค์ประกอบต้นทุนที่นำเข้าจากผังบัญชีของฝรั่งเศส</span><span class="sxs-lookup"><span data-stu-id="02560-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="02560-116">การแม็ปสมาชิกมิติองค์ประกอบต้นทุนของสหรัฐอเมริกาและฝรั่งเศสไปยังชุดทั่วไป</span><span class="sxs-lookup"><span data-stu-id="02560-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="02560-117">5001: การขาย</span><span class="sxs-lookup"><span data-stu-id="02560-117">5001: Sales</span></span>                                                           | <span data-ttu-id="02560-118">5001: การขายและการโฆษณา</span><span class="sxs-lookup"><span data-stu-id="02560-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="02560-119">5000: การขายและการโฆษณา</span><span class="sxs-lookup"><span data-stu-id="02560-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="02560-120">5030: การโฆษณา</span><span class="sxs-lookup"><span data-stu-id="02560-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="02560-121">6390: การซื้อสินค้าคงคลัง\*</span><span class="sxs-lookup"><span data-stu-id="02560-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="02560-122">7000: ค่าใช้จ่ายในการทำความสะอาด</span><span class="sxs-lookup"><span data-stu-id="02560-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="02560-123">7001: ค่าใช้จ่ายในการทำความสะอาด</span><span class="sxs-lookup"><span data-stu-id="02560-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="02560-124">7001: ค่าใช้จ่ายในการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="02560-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="02560-125">7001: ค่าใช้จ่ายในการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="02560-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="02560-126">\*สมาชิกมิติองค์ประกอบต้นทุนของฝรั่งเศสของการซื้อสินค้าคงคลังยังไม่ได้ถูกแม็ป</span><span class="sxs-lookup"><span data-stu-id="02560-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="02560-127">การแปลงสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="02560-127">Currency conversion</span></span>
<span data-ttu-id="02560-128">ผังบัญชีต่างๆ ที่คุณใช้อาจถูกตั้งค่าให้ใช้สกุลเงินที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="02560-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="02560-129">ในกรณีนี้ ตรวจสอบให้แน่ใจว่าได้ระบุการแปลงสกุลเงิน เพื่อให้ข้อมูลต้นทุนมีการประมวลผลโดยใช้สกุลเงินที่ถูกต้อง ตามที่กำหนดไว้ในบัญชีแยกประเภทการบัญชีต้นทุนที่มีการใช้สมาชิกมิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="02560-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="02560-130">ในตัวอย่างก่อนหน้านี้ ถ้ามีการใช้ดอลลาร์สหรัฐฯ (USD) ในบัญชีแยกประเภทการบัญชีต้นทุน คุณต้องสร้างการแปลงสกุลเงินจาก USD เป็นยูโร (EUR) เพื่อประมวลผลธุรกรรมสำหรับสมาชิกมิติองค์ประกอบต้นทุนที่มีการแม็ป</span><span class="sxs-lookup"><span data-stu-id="02560-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="02560-131">อัพเดตการแม็ปได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="02560-131">Update mappings at any time</span></span>
<span data-ttu-id="02560-132">คุณสามารถอัพเดตคำนิยามการแม็ปสำหรับมิติองค์ประกอบต้นทุนได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="02560-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="02560-133">เนื่องจากการแม็ปไม่มีวันที่มีผลบังคับ การเปลี่ยนแปลงจะถูกนำมาใช้ในครั้งถัดไปที่คุณประมวลผลธุรกรรมต้นทุน หรือรันการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="02560-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>



