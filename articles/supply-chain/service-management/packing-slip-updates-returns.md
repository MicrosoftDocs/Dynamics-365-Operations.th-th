---
title: การอัพเดตบันทึกการจัดส่งสำหรับการส่งคืนสินค้า
description: 'ก่อนที่สามารถรับสินค้าที่ส่งคืนเข้าไว้ในสินค้าคงคลังได้ ต้องอัพเดตบันทึกการจัดส่งสำหรับใบสั่งที่สินค้านั้นเป็นส่วนประกอบอยู่ '
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aba61e6acf5fb959917da9ddea94c21fe1460d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "344880"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="0c4c3-103">การอัพเดตบันทึกการจัดส่งสำหรับการส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="0c4c3-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0c4c3-104">ก่อนที่สามารถรับสินค้าที่ส่งคืนเข้าไว้ในสินค้าคงคลังได้ ต้องอัพเดตบันทึกการจัดส่งสำหรับใบสั่งที่สินค้านั้นเป็นส่วนประกอบอยู่ </span><span class="sxs-lookup"><span data-stu-id="0c4c3-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="0c4c3-105">เช่นเดียวกับที่กระบวนการอัพเดตใบแจ้งหนี้คือการอัพเดตธุรกรรมทางการเงิน กระบวนการอัพเดตบันทึกการจัดส่งคือการอัพเดตทางกายภาพของเรกคอร์ดสินค้าคงคลัง ซึ่งหมายถึงว่าได้การยืนยันการเปลี่ยนแปลงที่สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="0c4c3-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="0c4c3-106">ในกรณีของการส่งคืน มีการใช้ขั้นตอนที่กำหนดให้กับการดำเนินการโอนการครอบครองในระหว่างการอัพเดตบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0c4c3-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="0c4c3-107">การอัพเดตบันทึกการจัดส่งสามารถประมวลผลในสมุดรายวันการมาถึงของสินค้าหรือในใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="0c4c3-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="0c4c3-108">ในฐานะที่เป็นส่วนหนึ่งของการลงรายการบัญชีบันทึกการจัดส่ง คุณสามารถเชื่อมโยงหมายเลขอ้างอิงบันทึกการจัดส่งจากเอกสารการจัดส่งของลูกค้ากับรายการใบสั่งได้</span><span class="sxs-lookup"><span data-stu-id="0c4c3-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="0c4c3-109">ความสัมพันธ์นี้ไม่จำเป็น และใช้สำหรับการอ้างอิงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0c4c3-109">This association is optional and for reference only.</span></span> <span data-ttu-id="0c4c3-110">จะไม่สร้างการอัพเดตทางธุรกรรมใดๆ</span><span class="sxs-lookup"><span data-stu-id="0c4c3-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="0c4c3-111">ถ้าสินค้าที่ส่งคืนมาถึงไม่ครบตามจำนวนทั้งหมดที่คาดไว้ คุณควรรวมเฉพาะปริมาณที่ได้รับแล้วในการอัพเดตบันทึกการจัดส่งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0c4c3-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="0c4c3-112">ให้ปล่อยสินค้าส่วนที่เหลือไว้ในใบสั่ง จนกว่าส่วนที่เหลือของการจัดส่งคืนจะมาถึง</span><span class="sxs-lookup"><span data-stu-id="0c4c3-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="0c4c3-113">ถ้าสินค้าถูกส่งคืนจากฝ่ายตรวจสอบกลับไปยังแผนกจัดส่งและรับสินค้า เช่น เมื่อผู้ตรวจสอบสินค้าอย่างละเอียดไม่ทราบว่าจะจัดเก็บสินค้าไว้ที่ใดในสินค้าคงคลัง ต้องมีการอัพเดตบันทึกการจัดส่งที่สอดคล้องกันเพื่อให้ลงทะเบียนได้อย่างถูกต้อง และดำเนินการตามรหัสการโอนการครอบครองที่ระบุไว้ ตามผลการตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="0c4c3-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="0c4c3-114">เมื่อคุณอัพเดตบันทึกการจัดส่งสำหรับสินค้าที่ส่งคืนที่จะมาจากข้อตกลงการขาย ข้อผูกมัดเกี่ยวกับข้อตกลงการขายสำหรับสินค้าจะมีการอัพเดตโดยอัตโนมัติ เพื่อสะท้อนการเปลี่ยนแปลงในปริมาณหรือยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="0c4c3-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="0c4c3-115">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="0c4c3-115">See also</span></span>

[<span data-ttu-id="0c4c3-116">ทำการอัพเดตใบแจ้งหนี้สำหรับการส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="0c4c3-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  


