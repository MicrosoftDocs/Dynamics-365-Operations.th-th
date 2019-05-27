---
title: การนำสินค้าที่ส่งคืนไปตรวจสอบอย่างละเอียด
description: นำสินค้าที่ส่งคืนไปตรวจสอบอย่างละเอียด
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82d94e055326e598113822b8d7c4852b7dcb0c4e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565522"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="d7445-103">การนำสินค้าที่ส่งคืนไปตรวจสอบอย่างละเอียด</span><span class="sxs-lookup"><span data-stu-id="d7445-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="d7445-104">คลิก **การบริหารสินค้าคงคลังt** \> **งานประจำงวด** \> **การจัดการคุณภาพ** \> **ใบสั่งตรวจสอบสินค้า**</span><span class="sxs-lookup"><span data-stu-id="d7445-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="d7445-105">ค้นหาบรรทัดใบสั่งที่สอดคล้องกับสินค้าที่ส่งคืน ซึ่งคุณกำลังตรวจสอบอย่างละเอียด</span><span class="sxs-lookup"><span data-stu-id="d7445-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="d7445-106">ใบสั่งตรวจสอบสินค้าสามารถเชื่อมโยงกับหมายเลขสินค้าได้เพียงหมายเลขเดียวเท่านั้น </span><span class="sxs-lookup"><span data-stu-id="d7445-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="d7445-107">ถ้ามีการส่งคืนสินค้า 10 รายการที่มีหมายเลขสินค้าแตกต่างกันในการจัดส่งคืนครั้งเดียว และถูกส่งไปตรวจสอบ ระบบจะสร้างใบสั่งตรวจสอบสินค้าสำหรับสินค้าแต่ละรายการขึ้น 10 ใบ</span><span class="sxs-lookup"><span data-stu-id="d7445-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="d7445-108">หลังจากการตรวจสอบสินค้า ให้ทำการเลือกในฟิลด์ **รหัสการโอนการครอบครอง** เพื่อบ่งชี้ว่าควรจะทำอะไรกับสินค้า และควรจะจัดการธุรกรรมการเงินที่เกี่ยวข้องอย่างไร</span><span class="sxs-lookup"><span data-stu-id="d7445-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="d7445-109">ตัวอย่างเช่น การส่งคืนสินค้าไปที่สต็อกและคืนเงินให้แก่ลูกค้า การกำจัดสินค้าเป็นเศษซากและส่งสินค้าใหม่ไปเปลี่ยนให้ลูกค้า หรือการส่งคืนสินค้ากลับไปให้ลูกค้าโดยไม่ลดหนี้</span><span class="sxs-lookup"><span data-stu-id="d7445-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="d7445-110">ถ้าสินค้าที่ส่งคืนหลายรายการในชุดหมายเลขสินค้าเดียวกัน ไม่สามารถถูกกำหนดให้กับรหัสการโอนการครอบครองเดียวกันได้ คุณต้องแบ่งใบสั่งตรวจสอบสินค้า (<STRONG>ฟังก์ชัน</STRONG> &gt; <STRONG>แบ่ง</STRONG>) เพื่อกำหนดรหัสการโอนการครอบครองที่แตกต่างกันให้กับชุดสินค้าย่อยแต่ละชุด</span><span class="sxs-lookup"><span data-stu-id="d7445-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="d7445-111">เมื่อคุณตรวจสอบอย่างละเอียดเสร็จแล้ว ให้คลิก **รายงานเมื่อเสร็จสมบูรณ์** เพื่อนำออกใช้สินค้าที่ส่งคืน และสร้างรายการสมุดรายวันการมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="d7445-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="d7445-112">จากนั้นบุคลากรหรือแผนกที่ได้รับสินค้าจะประมวลผลสมุดรายวันสำหรับสินค้าที่จะส่งคืนไปยังสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="d7445-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="d7445-113">หรือ</span><span class="sxs-lookup"><span data-stu-id="d7445-113">–or–</span></span>
    
    <span data-ttu-id="d7445-114">สิ้นสุดใบสั่งตรวจสอบสินค้า และย้ายสินค้ากลับเข้าในสินค้าคงคลังโดยตรง โดยใช้หนึ่งในฟังก์ชัน **สินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="d7445-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="d7445-115">ปิดแบบฟอร์มเพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="d7445-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7445-116">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="d7445-116">See also</span></span>

[<span data-ttu-id="d7445-117">การระบุวิธีการตัดจำหน่ายสินค้าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="d7445-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  


