---
title: สร้างบัญชีแยกประเภทการบัญชีต้นทุน
description: บัญชีแยกประเภทการบัญชีต้นทุนแสดงถึงหน่วยการรายงานโดยรวม
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9878a03181ccb1eb9e31edefae345cee84b40c5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "310219"
---
# <a name="create-a-cost-accounting-ledger"></a><span data-ttu-id="3640d-103">สร้างบัญชีแยกประเภทการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3640d-103">Create a cost accounting ledger</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3640d-104">บัญชีแยกประเภทการบัญชีต้นทุนแสดงถึงหน่วยการรายงานโดยรวม</span><span class="sxs-lookup"><span data-stu-id="3640d-104">A cost accounting ledger represents the overall reporting unit.</span></span> <span data-ttu-id="3640d-105">ซึ่งกำหนดโดยมิติองค์ประกอบต้นทุน มิติทางสถิติ ปฏิทินทางการเงิน และสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="3640d-105">It is defined by a cost element dimension, statistical dimension, fiscal calendar, and currency.</span></span> <span data-ttu-id="3640d-106">ซึ่งไม่ตรงกับแนวคิดของนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="3640d-106">It is agnostic to the concept of legal entities.</span></span> <span data-ttu-id="3640d-107">นิติบุคคลและข้อมูลของนิติบุคคลสามารถเชื่อมโยงกับบัญชีแยกประเภทการบัญชีต้นทุนหลายบัญชี</span><span class="sxs-lookup"><span data-stu-id="3640d-107">A legal entity and its data can be associated with many cost accounting ledgers.</span></span> <span data-ttu-id="3640d-108">การบันทึกข้อมูลนี้ใช้บริษัทข้อมูลสาธิต USP2</span><span class="sxs-lookup"><span data-stu-id="3640d-108">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="3640d-109">ไปที่ บัญชีต้นทุน > การตั้งค่าบัญชีแยกประเภท > บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3640d-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="3640d-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3640d-110">Click New.</span></span>
3. <span data-ttu-id="3640d-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="3640d-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="3640d-112">ในฟิลด์มิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3640d-112">In the Cost element dimension field, enter or select a value.</span></span>
5. <span data-ttu-id="3640d-113">ในฟิลด์ปฏิทินทางการเงิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3640d-113">In the Fiscal calendar field, enter or select a value.</span></span>
6. <span data-ttu-id="3640d-114">ในฟิลด์สกุลเงินทางบัญชี ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3640d-114">In the Accounting currency field, enter or select a value.</span></span>
7. <span data-ttu-id="3640d-115">ในฟิลด์ชนิดอัตราแลกเปลี่ยน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3640d-115">In the Exchange rate type field, enter or select a value.</span></span>
8. <span data-ttu-id="3640d-116">ในฟิลด์มิติทางสถิติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3640d-116">In the Statistical dimension field, enter or select a value.</span></span>
9. <span data-ttu-id="3640d-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3640d-117">Click Save.</span></span>

