---
title: แก้ไขปัญหาการดำเนินงานคลังสินค้าขาออก
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการดำเนินงานคลังสินค้าขาออกใน Microsoft Dynamics 365 Supply Chain Management
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 919b6f433db47f24adc9a474942557a1467d1f71
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828189"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="7af02-103">แก้ไขปัญหาการดำเนินงานคลังสินค้าขาออก</span><span class="sxs-lookup"><span data-stu-id="7af02-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7af02-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการดำเนินงานคลังสินค้าขาออกใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7af02-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="7af02-105">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ใบสั่งขายไม่สามารถนำออกใช้ได้"</span><span class="sxs-lookup"><span data-stu-id="7af02-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7af02-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="7af02-106">Issue description</span></span>

<span data-ttu-id="7af02-107">ปัญหานี้อาจเกิดขึ้นจากสาเหตุหลายประการ</span><span class="sxs-lookup"><span data-stu-id="7af02-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="7af02-108">ตัวอย่างเช่น ใบสั่งอยู่ระหว่างการระงับการบริหารเครดิต และไม่สามารถสร้างการจัดส่งจนกว่าจะมีการป้อนที่อยู่ไปรษณีย์ที่ถูกต้องสำหรับรายการการขายทั้งหมดที่เชื่อมโยงกับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7af02-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="7af02-109">อีกทางหนึ่งคือ มีการระงับใบสั่งที่ต้องมีการแก้ไขก่อนจึงจะสามารถนำใบสั่งออกใช้ไปยังคลังสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="7af02-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="7af02-110">การระงับนี้อาจเป็นใบสั่งเฉพาะ หรืออาจอยู่ในรหัสลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7af02-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7af02-111">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="7af02-111">Issue resolution</span></span>

<span data-ttu-id="7af02-112">เพิ่มหรืออัพเดตที่อยู่ในใบสั่งขายและรายการใบสั่ง แล้วปล่อยใบสั่งไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7af02-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="7af02-113">คุณสามารถนำใบสั่งออกใช้ไปยังคลังสินค้าได้เฉพาะเมื่อมีที่อยู่ที่จัดส่งที่ถูกต้อง (ตามการตั้งค่ารูปแบบที่อยู่ในโมดูล **การจัดการองค์กร**)</span><span class="sxs-lookup"><span data-stu-id="7af02-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="7af02-114">ตรวจสอบการระงับใบสั่ง และแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="7af02-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="7af02-115">ลบการระงับจากใบสั่งหรือลูกค้า แล้วปล่อยใบสั่งไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7af02-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="7af02-116">ฉันได้รับข้อความแสดงข้อความต่อไปนี้: "การจัดส่งสำหรับจำนวนงานในศูนย์การผลิต 1% ถูกยืนยันแล้ว"</span><span class="sxs-lookup"><span data-stu-id="7af02-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="7af02-117">อย่างไรก็ตาม จะไม่มีการลงรายการบัญชีรายการใด ๆ</span><span class="sxs-lookup"><span data-stu-id="7af02-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7af02-118">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="7af02-118">Issue description</span></span>

<span data-ttu-id="7af02-119">การจัดส่งสินค้าในจำนวนงานในศูนย์การผลิตได้รับการยืนยันแล้ว แต่ยังไม่มีการลงรายการบัญชีเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7af02-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7af02-120">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="7af02-120">Issue resolution</span></span>

<span data-ttu-id="7af02-121">การยืนยันการจัดส่งไม่มีผลกระทบต่อการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="7af02-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="7af02-122">อัพเดตสถานะการจัดส่งและโหลดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7af02-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="7af02-123">การลงรายการบัญชีต้องเกิดขึ้นในกระบวนการแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="7af02-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="7af02-124">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "การจัดส่งสินค้าโดยตรงไม่สามารถดำเนินการสำหรับคลังสินค้า 1% เนื่องจากมีการเปิดใช้งานการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7af02-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="7af02-125">โปรดระบุคลังสินค้าอื่นที่ไม่ได้เปิดใช้งานสำหรับการจัดการคลังสินค้า"</span><span class="sxs-lookup"><span data-stu-id="7af02-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7af02-126">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="7af02-126">Issue description</span></span>

<span data-ttu-id="7af02-127">มีการเพิ่มสินค้าในรายการขายสำหรับการจัดส่งสินค้าโดยตรงจากคลังสินค้าที่เปิดใช้งานสำหรับการจัดการคลังสินค้า (WMS)</span><span class="sxs-lookup"><span data-stu-id="7af02-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="7af02-128">คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้เมื่อมีการอัพเดตรายการการขาย</span><span class="sxs-lookup"><span data-stu-id="7af02-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="7af02-129">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="7af02-129">Issue resolution</span></span>

<span data-ttu-id="7af02-130">Microsoft ได้ประเมินปัญหานี้แล้วและได้ระบุว่าเป็นข้อจำกัดของลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="7af02-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="7af02-131">ปัจจุบัน WMS ไม่สนับสนุนการจัดส่งสินค้าโดยตรง</span><span class="sxs-lookup"><span data-stu-id="7af02-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="7af02-132">เมื่อต้องการใช้การจัดส่งสินค้าโดยตรง คุณต้องเลือกสินค้าที่ไม่ใช่ WMS และคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7af02-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]