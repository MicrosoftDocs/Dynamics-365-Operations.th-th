--- 
title: "สร้างบัญชีแยกประเภทการบัญชีต้นทุน"
description: "บัญชีแยกประเภทการบัญชีต้นทุนแสดงถึงหน่วยการรายงานโดยรวม"
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ba8562f01ef440dd98db242550ee0e60db7acfc5
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-cost-accounting-ledger"></a><span data-ttu-id="3d254-103">สร้างบัญชีแยกประเภทการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3d254-103">Create a cost accounting ledger</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d254-104">บัญชีแยกประเภทการบัญชีต้นทุนแสดงถึงหน่วยการรายงานโดยรวม</span><span class="sxs-lookup"><span data-stu-id="3d254-104">A cost accounting ledger represents the overall reporting unit.</span></span> <span data-ttu-id="3d254-105">ซึ่งกำหนดโดยมิติองค์ประกอบต้นทุน มิติทางสถิติ ปฏิทินทางการเงิน และสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="3d254-105">It is defined by a cost element dimension, statistical dimension, fiscal calendar, and currency.</span></span> <span data-ttu-id="3d254-106">ซึ่งไม่ตรงกับแนวคิดของนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="3d254-106">It is agnostic to the concept of legal entities.</span></span> <span data-ttu-id="3d254-107">นิติบุคคลและข้อมูลของนิติบุคคลสามารถเชื่อมโยงกับบัญชีแยกประเภทการบัญชีต้นทุนหลายบัญชี</span><span class="sxs-lookup"><span data-stu-id="3d254-107">A legal entity and its data can be associated with many cost accounting ledgers.</span></span> <span data-ttu-id="3d254-108">การบันทึกข้อมูลนี้ใช้บริษัทข้อมูลสาธิต USP2</span><span class="sxs-lookup"><span data-stu-id="3d254-108">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="3d254-109">ไปที่ บัญชีต้นทุน > การตั้งค่าบัญชีแยกประเภท > บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3d254-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="3d254-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3d254-110">Click New.</span></span>
3. <span data-ttu-id="3d254-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="3d254-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="3d254-112">ในฟิลด์มิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3d254-112">In the Cost element dimension field, enter or select a value.</span></span>
5. <span data-ttu-id="3d254-113">ในฟิลด์ปฏิทินทางการเงิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3d254-113">In the Fiscal calendar field, enter or select a value.</span></span>
6. <span data-ttu-id="3d254-114">ในฟิลด์สกุลเงินทางบัญชี ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3d254-114">In the Accounting currency field, enter or select a value.</span></span>
7. <span data-ttu-id="3d254-115">ในฟิลด์ชนิดอัตราแลกเปลี่ยน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3d254-115">In the Exchange rate type field, enter or select a value.</span></span>
8. <span data-ttu-id="3d254-116">ในฟิลด์มิติทางสถิติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3d254-116">In the Statistical dimension field, enter or select a value.</span></span>
9. <span data-ttu-id="3d254-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3d254-117">Click Save.</span></span>


