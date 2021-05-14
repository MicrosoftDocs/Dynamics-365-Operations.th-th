---
title: รายการงานที่ปิดครั้งสุดท้ายต้องเป็นส่งสินค้า
description: รายการงานที่ปิดครั้งสุดท้ายต้องเป็นส่งสินค้า
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924386"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="5c5d0-103">รายการงานที่ปิดครั้งสุดท้ายต้องเป็นส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="5c5d0-103">The last closed work line must be a put</span></span>

<span data-ttu-id="5c5d0-104">รหัสข้อผิดพลาด: WAX1285</span><span class="sxs-lookup"><span data-stu-id="5c5d0-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="5c5d0-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="5c5d0-105">Symptoms</span></span>

<span data-ttu-id="5c5d0-106">ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5c5d0-106">The system shows the following error message:</span></span>

> <span data-ttu-id="5c5d0-107">รายการงานที่ปิดครั้งสุดท้ายต้องเป็นส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="5c5d0-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="5c5d0-108">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="5c5d0-108">Cause</span></span>

<span data-ttu-id="5c5d0-109">ไม่สามารถยกเลิกงานในสถานะปัจจุบันได้</span><span class="sxs-lookup"><span data-stu-id="5c5d0-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="5c5d0-110">บนรายการงานล่าสุด ฟิลด์ **สถานะของงาน** ได้รับการตั้งค่าเป็น *ปิด* แต่ไม่ได้ตั้งค่าฟิลด์ **ชนิดงาน** เป็น *ส่ง*</span><span class="sxs-lookup"><span data-stu-id="5c5d0-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="5c5d0-111">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="5c5d0-111">Resolution</span></span>

<span data-ttu-id="5c5d0-112">หากต้องการยกเลิกงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5c5d0-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="5c5d0-113">ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> การล้าง \> ยกเลิกงาน**</span><span class="sxs-lookup"><span data-stu-id="5c5d0-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="5c5d0-114">ในฟิลด์ **รหัสงาน** ให้ระบุรหัสงานที่คุณต้องการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="5c5d0-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="5c5d0-115">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5c5d0-115">Select **OK**.</span></span>
1. <span data-ttu-id="5c5d0-116">เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการยกเลิกงาน</span><span class="sxs-lookup"><span data-stu-id="5c5d0-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="5c5d0-117">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยกเลิกงานของคลังสินค้าสำหรับการจัดการข้อยกเว้น](../../warehousing/cancel-warehouse-work.md)</span><span class="sxs-lookup"><span data-stu-id="5c5d0-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
