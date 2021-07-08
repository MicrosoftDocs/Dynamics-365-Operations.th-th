---
title: ใบรับสินค้าที่ยกเลิกจะไม่อัปเดตสถานะธุรกรรมเป็น ลงทะเบียนแล้ว
description: หลังจากที่คุณยกเลิกใบรับสินค้าสินค้าขาเข้าแล้ว ระบบจะอัปเดตสถานะรายการความเคลื่อนไหวของสินค้าคงคลังจาก ได้รับแล้ว เป็น สั่งแล้ว โดยอัตโนมัติ
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294189"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="f4c86-103">ใบรับสินค้าที่ยกเลิกจะไม่อัปเดตสถานะธุรกรรมเป็น ลงทะเบียนแล้ว</span><span class="sxs-lookup"><span data-stu-id="f4c86-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="f4c86-104">อาการ</span><span class="sxs-lookup"><span data-stu-id="f4c86-104">Symptoms</span></span>

<span data-ttu-id="f4c86-105">หลังจากที่คุณเรียกใช้การดำเนินการ **ยกเลิกใบรับสินค้าสินค้าขาเข้า** ระบบจะอัปเดตสถานะรายการความเคลื่อนไหวของธุรกรรมสินค้าคงคลังจาก *ได้รับแล้ว* เป็น *สั่งแล้ว* โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f4c86-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="f4c86-106">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="f4c86-106">Resolution</span></span>

<span data-ttu-id="f4c86-107">เมื่อบันทึกการจัดส่งถูกยกเลิกสำหรับสินค้าขาออก สถานะของรายการความเคลื่อนไหวของสินค้าคงคลังจะยังคงเป็น *เบิกสินค้าแล้ว*</span><span class="sxs-lookup"><span data-stu-id="f4c86-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="f4c86-108">อย่างไรก็ตาม เมื่อใบรับสินค้าจากสินค้าขาเข้าถูกยกเลิก สถานะของรายการความเคลื่อนไหวของสินค้าคงคลังจะไม่ได้รับการคืนค่าเป็น *ลงทะเบียนแล้ว*</span><span class="sxs-lookup"><span data-stu-id="f4c86-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="f4c86-109">ดังนั้นหลังจากที่ใบรับสินค้าจากจํานวนงานในคลังถูกยกเลิก พนักงานคลังสินค้าต้องลงทะเบียนปริมาณสินค้าอีกครั้งให้กับจํานวนสินค้าในคลัง</span><span class="sxs-lookup"><span data-stu-id="f4c86-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="f4c86-110">สำหรับข้อมูลเพิ่มเติม ให้ดู [ลงทะเบียนปริมาณสินค้าที่มาถึงในสินค้าขาเข้า](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving)</span><span class="sxs-lookup"><span data-stu-id="f4c86-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
