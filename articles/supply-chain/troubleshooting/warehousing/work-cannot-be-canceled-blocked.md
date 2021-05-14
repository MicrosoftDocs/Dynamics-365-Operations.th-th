---
title: ไม่สามารถยกเลิกงานได้เนื่องจากถูกบล็อค
description: ไม่สามารถยกเลิกงานได้เนื่องจากถูกบล็อค
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924290"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="afbe5-103">ไม่สามารถยกเลิกงานได้เนื่องจากถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="afbe5-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="afbe5-104">รหัสข้อผิดพลาด: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="afbe5-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="afbe5-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="afbe5-105">Symptoms</span></span>

<span data-ttu-id="afbe5-106">ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="afbe5-106">The system shows the following error message:</span></span>

> <span data-ttu-id="afbe5-107">งาน %1 ไม่สามารถยกเลิกงานได้ เนื่องจากงานถูกบล็อคโดยชนิดเหตุผล %2</span><span class="sxs-lookup"><span data-stu-id="afbe5-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="afbe5-108">งานต้องได้รับการยกเลิกการบล็อคก่อนจึงจะสามารถยกเลิกได้</span><span class="sxs-lookup"><span data-stu-id="afbe5-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="afbe5-109">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="afbe5-109">Cause</span></span>

<span data-ttu-id="afbe5-110">งานถูกบล็อคและไม่สามารถยกเลิกได้</span><span class="sxs-lookup"><span data-stu-id="afbe5-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="afbe5-111">บนหน้า **งาน** บนแท็บ **ทั่วไป** ตัวเลือกที่ **ถูกบล็อค** จะถูกตั้งค่าเป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="afbe5-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="afbe5-112">การตั้งค่านี้บ่งชี้ว่างานถูกบล็อคอยู่</span><span class="sxs-lookup"><span data-stu-id="afbe5-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="afbe5-113">แท็บ **เหตุผลการบล็อค** แสดงเหตุผลที่งานถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="afbe5-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="afbe5-114">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="afbe5-114">Resolution</span></span>

<span data-ttu-id="afbe5-115">เมื่อต้องการยกเลิกการบล็อคงาน ให้เลือกแท็บ **เหตุผลการบล็อค** แล้วปฏิบัติตามขั้นตอนใดขั้นตอนหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="afbe5-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="afbe5-116">ถ้าฟิลด์ **เหตุผลการบล็อคงาน** ได้รับการตั้งค่าเป็น *เหตุผลที่ไม่อาจระบุได้*: ในบานหน้าต่างการดำเนินการ บนแท็บ **งาน** ในกลุ่ม **งาน** ให้เลือก **ยกเลิกการบล็อคงาน**</span><span class="sxs-lookup"><span data-stu-id="afbe5-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="afbe5-117">หากฟิลด์ **เหตุผลการบล็อคงาน** ได้รับการตั้งค่าเป็น *การประมวลผลเวฟ* : บนบานหน้าต่างการดำเนินการ บนแท็บ **ข้อมูลที่เกี่ยวข้อง** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** เลือก **กำลังประมวลผล**</span><span class="sxs-lookup"><span data-stu-id="afbe5-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="afbe5-118">จากนั้นบนหน้า **เวฟ** ในบานหน้าต่างการดำเนินการ ให้เปิดแท็บ **เวฟ** และ ในกลุ่ม **เวฟ** ให้เลือก **ล้างข้อมูลเวฟ**</span><span class="sxs-lookup"><span data-stu-id="afbe5-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="afbe5-119">วิธีการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="afbe5-119">Workaround</span></span>

<span data-ttu-id="afbe5-120">ถ้าขั้นตอนก่อนหน้านี้ไม่ได้แก้ปัญหา คุณสามารถยกเลิกงานได้โดยปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="afbe5-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="afbe5-121">ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> การล้าง \> ยกเลิกงาน**</span><span class="sxs-lookup"><span data-stu-id="afbe5-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="afbe5-122">ในฟิลด์ **รหัสงาน** ให้ระบุรหัสของงานที่คุณต้องการยกเลิก และในปัจจุบันมี **ค่าสถานะงาน** เป็น *เปิด* *อยู่ระหว่างดำเนินการ* *ยกเลิก* *รวม* หรือ *ปิด*</span><span class="sxs-lookup"><span data-stu-id="afbe5-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="afbe5-123">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="afbe5-123">Select **OK**.</span></span>
1. <span data-ttu-id="afbe5-124">เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการยกเลิกงาน</span><span class="sxs-lookup"><span data-stu-id="afbe5-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="afbe5-125">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยกเลิกงานของคลังสินค้าสำหรับการจัดการข้อยกเว้น](../../warehousing/cancel-warehouse-work.md)</span><span class="sxs-lookup"><span data-stu-id="afbe5-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
