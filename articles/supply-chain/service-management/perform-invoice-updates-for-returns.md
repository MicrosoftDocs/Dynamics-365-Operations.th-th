---
title: ทำการอัพเดตใบแจ้งหนี้สำหรับการส่งคืนสินค้า
description: ฟังก์ชันนี้สนับสนุนกระบวนการทางธุรกิจขององค์กรซึ่งเลือกที่จะออกใบแจ้งหนี้ใบสั่งส่งคืนสินค้าและใบสั่งขายพร้อมกัน และดำเนินการโดยบุคคลเดียวกัน
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec803aaa2f750c43a1865c9536730b275e6ef1d4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202157"
---
# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="9aa89-103">ทำการอัพเดตใบแจ้งหนี้สำหรับการส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="9aa89-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9aa89-104">ใบสั่งส่งคืนสินค้าคือ ใบสั่งขายชนิดหนึ่งซึ่งมีการทำเครื่องหมายเป็นสินค้าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="9aa89-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="9aa89-105">ดังนั้น หน้ารายการ **ใบสั่งขายทั้งหมด** จะถูกใช้ในการสร้างใบแจ้งหนี้สำหรับใบสั่งส่งคืนสินค้า แทนแบบฟอร์ม **ใบสั่งส่งคืนสินค้า**</span><span class="sxs-lookup"><span data-stu-id="9aa89-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="9aa89-106">ฟังก์ชันนี้สนับสนุนกระบวนการทางธุรกิจขององค์กรซึ่งเลือกที่จะออกใบแจ้งหนี้ใบสั่งส่งคืนสินค้าและใบสั่งขายพร้อมกัน และดำเนินการโดยบุคคลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="9aa89-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="9aa89-107">เนื่องจากใบแจ้งหนี้สำหรับสินค้าที่ส่งคืนใช้สำหรับยอดเงินค่าลบ ซึ่งเรียกว่าใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="9aa89-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="9aa89-108">เมื่อคุณตั้งค่าการอัพเดตใบแจ้งหนี้เป็นการประมวลผลชุดงาน ใบสั่งขายของชนิด **ใบสั่งที่ส่งคืน** ต้องมีสถานะของรายการการส่งคืนเป็น **ได้รับแล้ว** ซึ่งบ่งชี้ว่ามีการอัพเดตบันทึกการจัดส่งของใบสั่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="9aa89-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="9aa89-109">ลงรายการบัญชีใบสำหรับใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="9aa89-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="9aa89-110">คลิก **บัญชีลูกหนี้** \> **ทั่วไป** \> **ใบสั่งขาย** \> **ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="9aa89-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="9aa89-111">เลือกใบสั่งขายสำหรับ **ใบสั่งส่งคืน** ที่จะแสดงในฟิลด์ **ชนิดใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="9aa89-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="9aa89-112">ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบแจ้งหนี้** ในกลุ่ม **สร้าง** ให้คลิก **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="9aa89-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="9aa89-113">บนแท็บ **พารามิเตอร์** เลือกกล่องกาเครื่องหมาย **การลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="9aa89-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="9aa89-114">ทบทวนข้อมูลในแบบฟอร์มและดำเนินการเปลี่ยนแปลงใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="9aa89-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="9aa89-115">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="9aa89-115">Click **OK**.</span></span> <span data-ttu-id="9aa89-116">ลงรายการบัญชีใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="9aa89-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="9aa89-117">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="9aa89-117">See also</span></span>

[<span data-ttu-id="9aa89-118">การอัพเดตบันทึกการจัดส่งสำหรับการส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="9aa89-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  


