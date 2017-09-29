---
title: "การปรับปรุงมูลค่าต้นทุนปริมาณคงคลังคงเหลือ"
description: "ใช้หน้าการปรับปรุงปริมาณสินค้าคงคลังคงเหลือเพื่อปรับปรุงมูลค่าต้นทุนของปริมาณสินค้าคงคลังคงเหลือหลังจากกระบวนการปิดบัญชีสินค้าคงคลังได้ถูกรัน"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fb74ddfbc46047251a1f96512891bfbdca8e0389
ms.openlocfilehash: 2b4a27465908b5ffe19e91cb7ad0d29bce49505a
ms.contentlocale: th-th
ms.lasthandoff: 08/15/2017

---

# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="7ae70-103">การปรับปรุงมูลค่าต้นทุนปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="7ae70-103">Adjust on-hand inventory cost values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7ae70-104">ใช้หน้าการปรับปรุงปริมาณสินค้าคงคลังคงเหลือเพื่อปรับปรุงมูลค่าต้นทุนของปริมาณสินค้าคงคลังคงเหลือหลังจากกระบวนการปิดบัญชีสินค้าคงคลังได้ถูกรัน</span><span class="sxs-lookup"><span data-stu-id="7ae70-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="7ae70-105">คุณสามารถใช้หน้า **การปรับปรุงปริมาณสินค้าคงคลังคงเหลือ** เพื่อปรับปรุงมูลค่าต้นทุนของปริมาณสินค้าคงคลังคงเหลือหลังจากกระบวนการปิดบัญชีสินค้าคงคลังได้ถูกรัน</span><span class="sxs-lookup"><span data-stu-id="7ae70-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="7ae70-106">**หมายเหตุ:** เพื่อเปิดหน้า  **การปรับปรุงปริมาณสินค้าคงคลังคงเหลือ** บนหน้า **การปิดและการปรับปรุง** เลือกเรกคอร์ดของกระบวนการปิดบัญชีสินค้าคงคลังที่เสร็จสิ้นแล้ว และจากนั้นคลิก **การปรับปรุง** &gt; **ปริมาณคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="7ae70-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="7ae70-107">**ตัวอย่าง:** คุณมีธุรกรรมต่อไปนี้ในเดือนกุมภาพันธ์:</span><span class="sxs-lookup"><span data-stu-id="7ae70-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="7ae70-108">1 กุมภาพันธ์: ใบเสร็จรับเงินสินค้าคงคลังในปริมาณเท่ากับ 2 หน่วย ในราคาต้นทุน USD 10.00</span><span class="sxs-lookup"><span data-stu-id="7ae70-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="7ae70-109">5 กุมภาพันธ์: ใบเสร็จรับเงินสินค้าคงคลังในปริมาณเท่ากับ 1 หน่วย ในราคาต้นทุน USD 13.00</span><span class="sxs-lookup"><span data-stu-id="7ae70-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="7ae70-110">19 กุมภาพันธ์: นำสินค้าคงคลังทางการเงินออกใช้ในปริมาณ 1 หน่วย ที่ต้นทุนเฉลี่ยต่อเนื่อง USD 11.00</span><span class="sxs-lookup"><span data-stu-id="7ae70-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="7ae70-111">สินค้านี้มีการตั้งค่าโดยใช้แบบจำลองสินค้าคงคลังแบบเข้าก่อนออกก่อน (FIFO) และมีการปิดบัญชีสินค้าคงคลัง ณ วันที่ 28 กุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="7ae70-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="7ae70-112">ธุรกรรมการออกใช้ทางการเงินมูลค่า USD 11.00 จะถูกจับคู่กับใบเสร็จรับเงินลงวันที่ 1 กุมภาพันธ์ และจะมีการปรับปรุง USD 1.00</span><span class="sxs-lookup"><span data-stu-id="7ae70-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="7ae70-113">การรับสินค้าคงคลังต่อไปนี้จะมีปริมาณสินค้าคงคลังที่เปิดไว้:</span><span class="sxs-lookup"><span data-stu-id="7ae70-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="7ae70-114">1 กุมภาพันธ์: ปริมาณ 1 หน่วย ที่ต้นทุน USD 10.00</span><span class="sxs-lookup"><span data-stu-id="7ae70-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="7ae70-115">5 กุมภาพันธ์: ปริมาณ 1 หน่วย ที่ต้นทุน USD 13.00</span><span class="sxs-lookup"><span data-stu-id="7ae70-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="7ae70-116">ในการตั้งค่าต้นทุนของสินค้าทั้งสองนี้เป็น USD 15.00 ให้ใช้ตัวเลือกการปรับปรุงคงเหลือเพื่อปรับปรุงปริมาณคงเหลือที่เปิด ณ รอบระยะเวลาการปิดบัญชีสินค้าคงคลังล่าสุด</span><span class="sxs-lookup"><span data-stu-id="7ae70-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="7ae70-117">**หมายเหตุ:** วันที่ลงรายการบัญชีของธุรกรรมการปรับปรุงคงเหลือจะเป็นวันที่ปิดบัญชีสินค้าคงคลังล่าสุด</span><span class="sxs-lookup"><span data-stu-id="7ae70-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="7ae70-118">วันที่นี้ไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="7ae70-118">This date can't be modified.</span></span>

