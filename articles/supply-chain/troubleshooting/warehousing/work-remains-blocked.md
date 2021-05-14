---
title: งานถูกบล็อค
description: งานถูกบล็อค
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924141"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="2a5c6-103">งานถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="2a5c6-103">Work remains blocked</span></span>

<span data-ttu-id="2a5c6-104">รหัสข้อผิดพลาด: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="2a5c6-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="2a5c6-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="2a5c6-105">Symptoms</span></span>

<span data-ttu-id="2a5c6-106">ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2a5c6-106">The system shows the following error message:</span></span>

> <span data-ttu-id="2a5c6-107">งาน %1ยังคงถูกบล็อกเนื่องจากเวฟที่เกี่ยวข้อง %2 มีสถานะ %3</span><span class="sxs-lookup"><span data-stu-id="2a5c6-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="2a5c6-108">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="2a5c6-108">Cause</span></span>

<span data-ttu-id="2a5c6-109">งานมีการประมวลผลอยู่ในเวฟอยู่ในขณะนี้ไม่สามารถยกเลิกการบล็อคได้ ตามที่ระบุโดยเงื่อนไขอย่างใดอย่างหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2a5c6-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="2a5c6-110">บนแท็บ **เหตุผลการบล็อค** ฟิลด์ **เหตุผลการบล็อคงาน** ของอย่างน้อยหนึ่งรายการถูกตั้งค่าเป็น *เวฟการประมวลผล*</span><span class="sxs-lookup"><span data-stu-id="2a5c6-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="2a5c6-111">เมื่อคุณเลือก **เวฟ** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** บนแท็บ **ข้อมูลที่เกี่ยวข้อง** ของบานหน้าต่างการลงบัญชี ฟิลด์ **สถานะเวฟ** จะถูกตั้งค่าเป็น *กำลังประมวลผล*</span><span class="sxs-lookup"><span data-stu-id="2a5c6-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="2a5c6-112">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="2a5c6-112">Resolution</span></span>

<span data-ttu-id="2a5c6-113">บนบานหน้าต่างการดำเนินการ บนแท็บ **ข้อมูลที่เกี่ยวข้อง** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** ให้เลือก **เวฟ**</span><span class="sxs-lookup"><span data-stu-id="2a5c6-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="2a5c6-114">จากนั้นบนหน้า **เวฟ** ในบานหน้าต่างการดำเนินการ ให้เปิดแท็บ **เวฟ** และ ในกลุ่ม **เวฟ** ให้เลือก **ล้างข้อมูลเวฟ**</span><span class="sxs-lookup"><span data-stu-id="2a5c6-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="2a5c6-115">วิธีการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="2a5c6-115">Workaround</span></span>

<span data-ttu-id="2a5c6-116">ถ้าขั้นตอนก่อนหน้านี้ไม่ได้แก้ปัญหา คุณสามารถยกเลิกงานได้โดยปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2a5c6-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="2a5c6-117">ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> การล้าง \> ยกเลิกงาน**</span><span class="sxs-lookup"><span data-stu-id="2a5c6-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="2a5c6-118">ในฟิลด์ **รหัสงาน** ให้ระบุรหัสของงานที่คุณต้องการยกเลิก และในปัจจุบันมี **ค่าสถานะงาน** เป็น *เปิด* *อยู่ระหว่างดำเนินการ* *ยกเลิก* *รวม* หรือ *ปิด*</span><span class="sxs-lookup"><span data-stu-id="2a5c6-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="2a5c6-119">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2a5c6-119">Select **OK**.</span></span>
1. <span data-ttu-id="2a5c6-120">เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการยกเลิกงาน</span><span class="sxs-lookup"><span data-stu-id="2a5c6-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="2a5c6-121">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยกเลิกงานของคลังสินค้าสำหรับการจัดการข้อยกเว้น](../../warehousing/cancel-warehouse-work.md)</span><span class="sxs-lookup"><span data-stu-id="2a5c6-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
