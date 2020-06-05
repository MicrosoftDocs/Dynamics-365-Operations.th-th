---
title: ค่าใช้จ่ายระหว่างบริษัท
description: ผู้ปฏิบัติงานที่มีการว่าจ้างจากนิติบุคคลหนึ่งในองค์กรอาจทำงานสำหรับนิติบุคคลอื่นในองค์กรเดียวกัน ในสถานการณ์นี้ คุณสามารถใช้ลักษณะการทำงานของค่าใช้จ่ายระหว่างบริษัทในการกำหนดค่าใช้จ่ายของผู้ปฏิบัติงานให้กับนิติบุคคลซึ่งมีการดำเนินงาน
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390895"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="505a1-104">ค่าใช้จ่ายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="505a1-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="505a1-105">ผู้ปฏิบัติงานที่มีการว่าจ้างจากนิติบุคคลหนึ่งในองค์กรอาจทำงานสำหรับนิติบุคคลอื่นในองค์กรเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="505a1-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="505a1-106">ในสถานการณ์นี้ คุณสามารถใช้ลักษณะการทำงานของค่าใช้จ่ายระหว่างบริษัทในการกำหนดค่าใช้จ่ายของผู้ปฏิบัติงานให้กับนิติบุคคลซึ่งมีการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="505a1-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="505a1-107">นิติบุคคลที่จ้างผู้ปฏิบัติงานเรียกว่านิติบุคคลที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="505a1-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="505a1-108">นิติบุคคลที่ผู้ปฏิบัติงานก่อค่าใช้จ่ายให้เรียกว่านิติบุคคลที่ขอยืม</span><span class="sxs-lookup"><span data-stu-id="505a1-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="505a1-109">ก่อนที่ผู้ปฏิบัติงานจะสามารถสร้างและส่งค่าใช้จ่ายสำหรับงานที่ดำเนินการสำหรับนิติบุคคลอื่น ในนิติบุคคลที่ให้ยืม ในหน้า **พารามิเตอร์การจัดการค่าใช้จ่าย** เลือกตัวเลือก **อนุญาตรายการค่าใช้จ่ายระหว่างบริษัท**</span><span class="sxs-lookup"><span data-stu-id="505a1-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="505a1-110">การลงรายการบัญชีภาษีสำหรับค่าใช้จ่ายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="505a1-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="505a1-111">ถ้าคุณต้องการใช้กลุ่มภาษีที่สัมพันธ์กับนิติบุคคลที่ให้กู้ยืม (ต้นทาง) แทนที่จะใช้นิติบุคคลที่กู้ยืม (ปลายทาง) ในรายงานค่าใช้จ่ายของคุณ คุณจะต้องตั้งค่าคอนฟิกนี้ในการตั้งค่าภาษีการขายสำหรับบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="505a1-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="505a1-112">เมื่อมีการตั้งค่าพารามิเตอร์บัญชีแยกประเภททั่วไป **นิติบุคคลสำหรับการลงรายการบัญชีภาษีระหว่างบริษัท** ตั้งค่าเป็น **ต้นทาง** และ **ใช้กฎภาษีสำหรับภาษีขาย** ตั้งค่าเป็น **ไม่มี** จะมีการใช้ชุดภาษีสำหรับนิติบุคคลที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="505a1-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="505a1-113">เมื่อมีการตั้งค่าพารามิเตอร์เป็น **ปลายทาง** จะมีการใช้ชุดภาษีสำหรับนิติบุคคลที่ขอยืม</span><span class="sxs-lookup"><span data-stu-id="505a1-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="505a1-114">สำหรับนิติบุคคลในสหรัฐอเมริกา เมื่อมีการตั้งค่าพารามิเตอร์เป็น **ต้นทาง** ฟิลด์ **ลูกหนี้ภาษีขาย** ต้องมีการตั้งค่าคอนฟิกในหน้า **กลุ่มการลงรายการบัญชีแยกประเภท** ใหม่</span><span class="sxs-lookup"><span data-stu-id="505a1-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="505a1-115">กลไกการลงบัญชีจะใช้ข้อมูลจากฟิลด์นี้สำหรับรายการบัญชีที่เกี่ยวข้องกับภาษี</span><span class="sxs-lookup"><span data-stu-id="505a1-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="505a1-116">ลักษณะการทำงานไม่สอดคล้องกันสำหรับรายการค่าใช้จ่ายที่ลงรายการบัญชีโดยมีหรือไม่มีโครงการ</span><span class="sxs-lookup"><span data-stu-id="505a1-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
