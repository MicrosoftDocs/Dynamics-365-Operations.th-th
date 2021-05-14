---
title: ไม่สามารถยกเลิกงานได้เนื่องจากสถานะของงาน
description: ไม่สามารถยกเลิกงานได้เนื่องจากสถานะของงาน
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924266"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="3668c-103">ไม่สามารถยกเลิกงานได้เนื่องจากสถานะของงาน</span><span class="sxs-lookup"><span data-stu-id="3668c-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="3668c-104">รหัสข้อผิดพลาด: WAX2190</span><span class="sxs-lookup"><span data-stu-id="3668c-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="3668c-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="3668c-105">Symptoms</span></span>

<span data-ttu-id="3668c-106">ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3668c-106">The system shows the following error message:</span></span>

> <span data-ttu-id="3668c-107">คุณไม่สามารถยกเลิกงาน %1 เนื่องจากมีสถานะ %2</span><span class="sxs-lookup"><span data-stu-id="3668c-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="3668c-108">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="3668c-108">Cause</span></span>

<span data-ttu-id="3668c-109">ไม่สามารถยกเลิกงานในสถานะปัจจุบันได้</span><span class="sxs-lookup"><span data-stu-id="3668c-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="3668c-110">หัวข้องานหรือรายการงานไม่มีค่า **สถานะของงาน** ที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="3668c-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="3668c-111">ฟิลด์ **สถานะของงาน** ไม่ได้ตั้งค่าบนหัวข้องานเป็น *เปิด* หรือ *อยู่ระหว่างการดำเนินการ*</span><span class="sxs-lookup"><span data-stu-id="3668c-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="3668c-112">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="3668c-112">Resolution</span></span>

<span data-ttu-id="3668c-113">หากต้องการยกเลิกงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="3668c-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="3668c-114">ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> การล้าง \> ยกเลิกงาน**</span><span class="sxs-lookup"><span data-stu-id="3668c-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="3668c-115">ในฟิลด์ **รหัสงาน** ให้ระบุรหัสงานที่คุณต้องการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="3668c-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="3668c-116">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3668c-116">Select **OK**.</span></span>
1. <span data-ttu-id="3668c-117">เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการยกเลิกงาน</span><span class="sxs-lookup"><span data-stu-id="3668c-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="3668c-118">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยกเลิกงานของคลังสินค้าสำหรับการจัดการข้อยกเว้น](../../warehousing/cancel-warehouse-work.md)</span><span class="sxs-lookup"><span data-stu-id="3668c-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
