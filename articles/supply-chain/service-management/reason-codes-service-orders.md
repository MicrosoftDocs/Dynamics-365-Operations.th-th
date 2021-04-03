---
title: รหัสเหตุผลสำหรับใบสั่งบริการ
description: ใช้รหัสเหตุผลเพื่อช่วยอธิบายสถานะของใบสั่งบริการ เมื่อมีการอัพเดตขั้นตอนของใบสั่งบริการ
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b059ad5b2ea9cd577624355cf17925cfb9b4867b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258529"
---
# <a name="reason-codes-for-service-orders"></a><span data-ttu-id="e7794-103">รหัสเหตุผลสำหรับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="e7794-103">Reason codes for service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e7794-104">คุณสามารถใช้รหัสเหตุผลเพื่อช่วยอธิบายสถานะของใบสั่งบริการได้ เมื่อมีการอัพเดตขั้นตอนของใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="e7794-104">You can use reason codes to help explain the status of a service order when the stage of a service order is updated.</span></span> <span data-ttu-id="e7794-105">ตัวอย่างเช่น ถ้าคุณยกเลิกใบสั่งบริการ คุณสามารถเลือกรหัสเหตุผลสำหรับการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="e7794-105">For example, if you cancel a service order, you can select a reason code for the cancellation.</span></span>

<span data-ttu-id="e7794-106">หากต้องการดูข้อมูลเกี่ยวกับรหัสเหตุผลที่ใช้โดยติดตามความคืบหน้าของใบสั่งบริการ ให้รันรายงานความคืบหน้าของใบสั่งบริการ </span><span class="sxs-lookup"><span data-stu-id="e7794-106">To view information about reason codes that are used to track the progress of service orders, run the Service order progress report.</span></span> <span data-ttu-id="e7794-107">รายงานนี้จะแสดงรายการใบสั่งบริการทั้งหมด และรหัสเหตุผลใดที่ระบุเมื่อมีการอัพเดตขั้นใบสั่งบริการ ไม่ว่าจะเป็นขั้นใดก็ตาม</span><span class="sxs-lookup"><span data-stu-id="e7794-107">This report lists all service orders, regardless of their stage, and the reason codes that are specified when a service order stage is updated.</span></span>

## <a name="turn-reason-codes-on-or-off"></a><span data-ttu-id="e7794-108">เปิดหรือปิดรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="e7794-108">Turn reason codes on or off</span></span>

<span data-ttu-id="e7794-109">ไม่จำเป็นต้องระบุรหัสเหตุผล </span><span class="sxs-lookup"><span data-stu-id="e7794-109">Reason codes are optional.</span></span> <span data-ttu-id="e7794-110">คุณสามารถตัดสินใจว่าต้องมีรหัสเหตุผล เมื่อคุณอัพเดตใบสั่งบริการไปยังขั้นบริการเฉพาะหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e7794-110">You can decide whether to require a reason code when you update a service order to a specific service stage.</span></span>

1.  <span data-ttu-id="e7794-111">คลิก **การจัดการงานบริการ** \> **ตั้งค่า** \> **ใบสั่งบริการ** \> **ขั้นตอนการบริการ**</span><span class="sxs-lookup"><span data-stu-id="e7794-111">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="e7794-112">ในแบบฟอร์ม **ขั้นตอนการบริการ** เลือกขั้นตอนการบริการ และจากนั้น เลือกกล่องกาเครื่องหมาย **เหตุผล** สำหรับขั้นตอนการบริการ</span><span class="sxs-lookup"><span data-stu-id="e7794-112">In the **Service stages** form, select a service stage, and then select the **Reason** check box for the service stage.</span></span>

3.  <span data-ttu-id="e7794-113">ปิดแบบฟอร์มเพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="e7794-113">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7794-114">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="e7794-114">See also</span></span>

[<span data-ttu-id="e7794-115">ตั้งค่าระยะใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="e7794-115">Set up service order stages</span></span>](set-up-service-order-stages.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]