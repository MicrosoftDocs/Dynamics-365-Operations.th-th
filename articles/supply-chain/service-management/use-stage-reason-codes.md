---
title: ใช้รหัสเหตุผลของขั้น
description: คุณใช้รหัสเหตุผลเพื่อระบุเหตุที่ข้อตกลงระดับบริการ (SLA) ถูกยกเลิก หรือเหตุใดที่ใบสั่งบริการเกินขอบเขตเวลาที่คุณตั้งไว้ใน SLA
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 307e6b3e67de702135662e047aef00fd181d4749
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824257"
---
# <a name="use-stage-reason-codes"></a><span data-ttu-id="6c4b8-103">ใช้รหัสเหตุผลของขั้น</span><span class="sxs-lookup"><span data-stu-id="6c4b8-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6c4b8-104">คุณใช้รหัสเหตุผลเพื่อระบุเหตุที่ข้อตกลงระดับบริการ (SLA) ถูกยกเลิก หรือเหตุใดที่ใบสั่งบริการเกินขอบเขตเวลาที่คุณตั้งไว้ใน SLA</span><span class="sxs-lookup"><span data-stu-id="6c4b8-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="6c4b8-105">นอกจากนี้คุณสามารถระบุว่ารหัสเหตุผลจำเป็นหรือไม่เมื่อยกเลิก SLA หรือเมื่อขอบเขตเวลาที่จำกัดเกิดจากที่ระบุใน SLA สำหรับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="6c4b8-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="6c4b8-106">ถ้าคุณได้ระบุว่ารหัสเหตุผลจำเป็น คุณต้องป้อนรหัสเหตุผลในสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c4b8-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="6c4b8-107">เมื่อใบสั่งบริการย้ายไปยังขั้นตอนที่หยุดการบันทึกเวลาเทียบกับ SLA สำหรับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="6c4b8-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="6c4b8-108">เมื่อใบสั่งบริการออกจากระบบ</span><span class="sxs-lookup"><span data-stu-id="6c4b8-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="6c4b8-109">เมื่อหยุดบันทึกเวลาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="6c4b8-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="6c4b8-110">ตั้งค่ารหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="6c4b8-110">Set up reason codes</span></span>

1.  <span data-ttu-id="6c4b8-111">คลิก **การจัดการงานบริการ** \> **ตั้งค่า** \> **ใบสั่งบริการ** \> **รหัสเหตุผลของขั้นตอน**</span><span class="sxs-lookup"><span data-stu-id="6c4b8-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="6c4b8-112">ในแบบฟอร์ม **รหัสเหตุผลของขั้นตอน** ให้คลิก **สร้าง** เพื่อสร้างรหัสเหตุผลใหม่</span><span class="sxs-lookup"><span data-stu-id="6c4b8-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="6c4b8-113">ในฟิลด์ **รหัสเหตุผลของขั้นตอน** ให้ป้อนรหัสเหตุผลของขั้นที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="6c4b8-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="6c4b8-114">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบายของรหัสเหตุผลของขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="6c4b8-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="6c4b8-115">ปิดแบบฟอร์มเพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="6c4b8-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="6c4b8-116">การใช้รหัสเหตุผลเมื่อยกเลิกข้อตกลงระดับบริการ</span><span class="sxs-lookup"><span data-stu-id="6c4b8-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="6c4b8-117">คลิก **การจัดการงานบริการ** \> **ตั้งค่า** \> **พารามิเตอร์การจัดการงานบริการ**</span><span class="sxs-lookup"><span data-stu-id="6c4b8-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="6c4b8-118">ในฟอร์ม **พารามิเตอร์การจัดการบริการ** คลิกที่ลิงค์ **ทั่วไป** และจากนั้นเลือกกล่องกาเครื่องหมาย **รหัสเหตุผลในการยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="6c4b8-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="6c4b8-119">การใช้รหัสเหตุผลเมื่อเมื่อใบสั่งบริการเกิดขีดจำกัดเวลาที่ตั้งค่าไว้โดยข้อตกลงระดับการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="6c4b8-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="6c4b8-120">คลิก **การจัดการงานบริการ** \> **ตั้งค่า** \> **พารามิเตอร์การจัดการงานบริการ**</span><span class="sxs-lookup"><span data-stu-id="6c4b8-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="6c4b8-121">ในฟอร์ม **พารามิเตอร์การจัดการบริการ** คลิกที่ลิงค์ **ทั่วไป** และจากนั้นเลือกกล่องกาเครื่องหมาย **รหัสเหตุผลที่เกินเวลา**</span><span class="sxs-lookup"><span data-stu-id="6c4b8-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c4b8-122">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="6c4b8-122">See also</span></span>

[<span data-ttu-id="6c4b8-123">การเริ่มต้นและหยุดการบันทึกเวลาของใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="6c4b8-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]