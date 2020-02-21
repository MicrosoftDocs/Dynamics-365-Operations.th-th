---
title: ตั้งค่าคอนฟิกและดำเนินการแลกเปลี่ยนในใบสั่งส่งคืนสินค้า
description: หัวข้อนี้อธิบายวิธีตั้งค่าคอนฟิกการแลกเปลี่ยนเมื่อมีการส่งคืนสินค้าใน Dynamics 365 Commerce
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6d7688e78a375bc262b1156c5439c0fff7cd1f0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004446"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="3c121-103">ตั้งค่าคอนฟิกและดำเนินการแลกเปลี่ยนในใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="3c121-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3c121-104">ใน Dynamics 365 Commerce รุ่นก่อนหน้านี้ การส่งคืนสินค้าตามใบสั่งของลูกค้าจะได้รับการดำเนินการโดยใช้เอกสารใบสั่งส่งคืนสินค้าในศูนย์ควบคุม</span><span class="sxs-lookup"><span data-stu-id="3c121-104">In previous versions of Dynamics 365 Commerce, returns against customer orders were processed by using the return order document in Headquarters.</span></span> <span data-ttu-id="3c121-105">อย่างไรก็ดี เราสามารถใช้เอกสารใบสั่งส่งคืนสินค้าเพื่อประมวลผลเฉพาะผลิตภัณฑ์ที่จะส่งคืนได้</span><span class="sxs-lookup"><span data-stu-id="3c121-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="3c121-106">ผลิตภัณฑ์ที่ส่งคืนจะบ่งชี้โดยปริมาณติดลบในรายการใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="3c121-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="3c121-107">ในทางกลับกัน การขายจะบ่งชี้โดยปริมาณที่เป็นบวก</span><span class="sxs-lookup"><span data-stu-id="3c121-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="3c121-108">อย่างไรก็ดี เอกสารใบสั่งส่งคืนสินค้าจะไม่รองรับปริมาณที่เป็นบวก</span><span class="sxs-lookup"><span data-stu-id="3c121-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="3c121-109">ด้วยข้อจำกัดนี้เอง แอปรุ่นก่อนหน้านี้จึงไม่รองรับสถานการณ์ที่ทำการแลกเปลี่ยนผลิตภัณฑ์โดยใช้เอกสารใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="3c121-109">Because of this limitation, previous versions of the app didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="3c121-110">อย่างไรก็ตาม มีการเพิ่มฟังก์ชันเพื่อรองรับสถานการณ์ที่ทำการแลกเปลี่ยนผลิตภัณฑ์ในใบสั่งส่งคืนสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="3c121-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="3c121-111">ขณะนี้ Commerce จึงใช้เอกสารใบสั่งขายแทนเอกสารใบสั่งส่งคืนสินค้าเพื่อประมวลผลธุรกรรมชนิดนี้</span><span class="sxs-lookup"><span data-stu-id="3c121-111">Commerce now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a><span data-ttu-id="3c121-112">ตั้งค่าคอนฟิก Commerce ให้สนับสนุนการแลกเปลี่ยนในใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="3c121-112">Configure Commerce to support exchanges on return orders</span></span>

<span data-ttu-id="3c121-113">ดำเนินการตามขั้นตอนเหล่านี้เพื่อตั้งค่าคอนฟิกระบบให้สนับสนุนการแลกเปลี่ยนในใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="3c121-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="3c121-114">ไปที่ **การขายปลีกและการค้า \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์การค้า**</span><span class="sxs-lookup"><span data-stu-id="3c121-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="3c121-115">บนแท็บด่วน **ใบสั่งของลูกค้า** ตั้งค่าตัวเลือก **ประมวลผลใบสั่งส่งคืนสินค้าเป็นใบสั่งขาย** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="3c121-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="3c121-116">รันงาน **กำหนดการการกระจายการตั้งค่าคอนฟิกส่วนกลาง** (**1110**)</span><span class="sxs-lookup"><span data-stu-id="3c121-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="3c121-117">ทำการแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="3c121-117">Make an exchange</span></span>

<span data-ttu-id="3c121-118">หลังจากตั้งค่าคอนฟิกระบบตามที่อธิบายไว้ในส่วนก่อนหน้าแล้ว ผู้ใช้การขายหน้าร้าน (POS) จะยังคงเลือกใบสั่งขายหรือใบแจ้งหนี้การขายเพื่อประมวลผลการส่งคืนเหมือนกับในแอปรุ่นก่อนหน้าได้</span><span class="sxs-lookup"><span data-stu-id="3c121-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of the app.</span></span> <span data-ttu-id="3c121-119">อย่างไรก็ดี หลังจากเพิ่มสินค้ารับคืนไปยังรถเข็นแล้ว ผู้ใช้จะสามารถเพิ่มรายการขายใหม่ไปยังรถเข็นได้</span><span class="sxs-lookup"><span data-stu-id="3c121-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="3c121-120">สำหรับรายการขายใหม่เหล่านี้ ผู้ใช้ต้องกำหนดแอตทริบิวต์ทั้งหมดที่จะเป็นเพื่อประมวลผลรายการใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3c121-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="3c121-121">แอททริบิวต์เหล่านี้รวมถึงวิธีการจัดส่งและสถานที่สำหรับการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="3c121-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="3c121-122">การชำระเงินที่ครบกำหนดชำระสำหรับธุรกรรมจะเป็นเงินสุทธิของรายการใบสั่งส่งคืนสินค้าและรายการใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3c121-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="3c121-123">เมื่อมีการชำระเงินสำหรับธุรกรรมดังกล่าวแล้ว ใบสั่งส่งคืนสินค้าจะได้รับการลงรายการบัญชีเป็นเอกสารใบสั่งขายในศูนย์ควบคุม และระบบจะออกใบแจ้งหนี้ให้กับรายการส่งคืนทันที</span><span class="sxs-lookup"><span data-stu-id="3c121-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="3c121-124">เพื่อให้เห็นภาพยอดเงินต่างๆ สำหรับรถเข็นอย่างชัดเจนยิ่งขึ้น จึงมีการเพิ่มฟิลด์ยอดเงินใหม่ไปยังรถเข็น</span><span class="sxs-lookup"><span data-stu-id="3c121-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="3c121-125">คุณสามารถใช้ตัวออกแบบหน้าจอเพื่อทำให้ฟิลด์ใหม่เหล่านี้พร้อมใช้งานในอินเทอร์เฟสผู้ใช้ POS (UI)</span><span class="sxs-lookup"><span data-stu-id="3c121-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="3c121-126">**ใช้ยอดเงินฝากแล้ว** – ยอดเงินในการฝากเงินที่ใช้กับธุรกรรมเมื่อผู้ใช้เบิกสินค้าตามใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3c121-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="3c121-127">หากไม่มีการแทนที่เงินฝากและมีการตั้งค่าคอนฟิกเงินฝากที่ 10 เปอร์เซ็นต์ ยอดเงินในฟิลด์นี้จะเท่ากับ 90 เปอร์เซ็นต์ของยอดเงินรวมของใบสั่งลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3c121-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="3c121-128">**ดำเนินการกับยอดเงิน** – ยอดเงินรวมของรายการที่มีการตั้งค่าวิธีการจัดส่งเป็น **ดำเนินการ** เมื่อสร้างหรือแก้ไขใบสั่งของลูกค้าหรือในระหว่างการแลกเปลี่ยนใบสั่งลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3c121-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="3c121-129">ยอดเงินในฟิลด์นี้จะรวมภาษีและค่าธรรมเนียมไว้</span><span class="sxs-lookup"><span data-stu-id="3c121-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="3c121-130">**ยอดส่งคืน** – ยอดเงินรวมสำหรับรายการที่มีปริมาณติดลบในระหว่างการแลกเปลี่ยนใบสั่งลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3c121-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="3c121-131">ยอดเงินในฟิลด์นี้จะรวมภาษีและค่าธรรมเนียมไว้</span><span class="sxs-lookup"><span data-stu-id="3c121-131">The amount in this field includes taxes and charges.</span></span>
