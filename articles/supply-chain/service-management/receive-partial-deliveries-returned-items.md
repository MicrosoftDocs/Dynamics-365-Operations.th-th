---
title: รับการจัดส่งบางส่วนของสินค้าส่งคืน
description: 'การจัดส่งเป็นบางส่วนมีการกำหนดในรูปแบบของบรรทัดใบสั่งส่งคืนสินค้า ไม่ใช่การจัดส่งของใบสั่งส่งคืนสินค้า '
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
ms.openlocfilehash: e2b7bfad1e0d80675848353d4118960d44f2dc01
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570330"
---
# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="3e342-103">รับการจัดส่งบางส่วนของสินค้าส่งคืน</span><span class="sxs-lookup"><span data-stu-id="3e342-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3e342-104">การจัดส่งเป็นบางส่วนมีการกำหนดในรูปแบบของบรรทัดใบสั่งส่งคืนสินค้า ไม่ใช่การจัดส่งของใบสั่งส่งคืนสินค้า </span><span class="sxs-lookup"><span data-stu-id="3e342-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="3e342-105">นี่หมายความว่า ถ้าคุณได้รับปริมาณสินค้าทั้งหมดซึ่งถูกบ่งชี้ไว้ในรายการใบสั่งส่งคืนสินค้าหนึ่งรายการ แต่คุณไม่ได้รับสินค้าจากรายการอื่นในใบสั่งส่งคืนสินค้า การจัดส่งนี้ไม่ใช่การจัดส่งเป็นบางส่วน</span><span class="sxs-lookup"><span data-stu-id="3e342-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="3e342-106">อย่างไรก็ตาม ถ้ารายการใบสั่งส่งคืนสินค้าต้องการสินค้าเฉพาะ 10 หน่วยให้ถูกส่งคืน แต่คุณได้รับสินค้านั้นเพียงสี่รายการ ถือเป็นการจัดส่งบางส่วน</span><span class="sxs-lookup"><span data-stu-id="3e342-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="3e342-107">ถ้าการจัดส่งคืนมีสินค้าน้อยกว่าปริมาณทั้งหมดของบรรทัดใบสั่งส่งคืนสินค้า คุณสามารถตั้งค่าการจัดส่งเพิ่มเติมและรอให้ส่วนที่เหลือของปริมาณที่ส่งคืนมาถึง หรือคุณสามารถลงทะเบียนและลงรายการบัญชีปริมาณบางส่วนก็ได้</span><span class="sxs-lookup"><span data-stu-id="3e342-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="3e342-108">การลงทะเบียนและลงรายการบัญชีปริมาณบางส่วน</span><span class="sxs-lookup"><span data-stu-id="3e342-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="3e342-109">หลังจากที่คุณเลือกใบสั่งส่งคืนสำหรับการมาถึงในฟอร์ม **ภาพรวมการมาถึง - คลังสินค้า: %1 ท่าเรือ: %2 ชื่อสมุดรายวัน: %3** คลิก **เริ่มต้นการมาถึง** เพื่อสร้างสมุดรายวันการมาถึง จากนั้น คลิก **สมุดรายวัน** \> **แสดงการมาถึงจากใบรับ** เพื่อเปิดฟอร์ม **สมุดรายวันสถานที่**</span><span class="sxs-lookup"><span data-stu-id="3e342-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="3e342-110">เลือกรายการของสมุดรายวันที่คุณต้องการทำงานด้วย และจากนั้นคลิก **รายการ** เพื่อเปิดแบบฟอร์ม **รายการสมุดรายวัน, สถานที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="3e342-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="3e342-111">เลือกรายการของหมายเลขสินค้า ซึ่งสินค้าได้มาถึงเพียงบางส่วนเท่านั้น แล้วคลิก **ฟังก์ชัน** \> **แบ่ง** เพื่อเปิดแบบฟอร์ม **แบ่ง**</span><span class="sxs-lookup"><span data-stu-id="3e342-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="3e342-112">ในฟิลด์ **แบ่งปริมาณ** ให้ป้อนปริมาณสำหรับจำนวนทั้งหมดของสินค้าที่ได้รับ แล้วคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3e342-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="3e342-113">บนแบบฟอร์ม **รายการสมุดรายวัน, สถานที่เก็บ** ให้เลือกรายการสำหรับปริมาณของสินค้าที่มาถึงแล้ว แล้วคลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="3e342-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="3e342-114">คุณสามารถลงรายการบัญชีรายการสำหรับปริมาณสินค้าเพิ่มเติม หลังจากที่สินค้ามาถึงได้</span><span class="sxs-lookup"><span data-stu-id="3e342-114">You can post the line for the additional quantity after the items have arrived.</span></span>




