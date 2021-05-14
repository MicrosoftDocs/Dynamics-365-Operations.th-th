---
title: คุณไม่สามารถยกเลิกงานที่อยู่บนผู้ใช้ได้
description: คุณไม่สามารถยกเลิกงานที่อยู่บนผู้ใช้ได้
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924412"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="60dc3-103">คุณไม่สามารถยกเลิกงานที่อยู่บนผู้ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="60dc3-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="60dc3-104">รหัสข้อผิดพลาด: WAX708</span><span class="sxs-lookup"><span data-stu-id="60dc3-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="60dc3-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="60dc3-105">Symptoms</span></span>

<span data-ttu-id="60dc3-106">ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="60dc3-106">The system shows the following error message:</span></span>

> <span data-ttu-id="60dc3-107">คุณไม่สามารถยกเลิกงานที่อยู่กับผู้ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="60dc3-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="60dc3-108">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="60dc3-108">Cause</span></span>

<span data-ttu-id="60dc3-109">งานถูกล็อคโดยผู้ใช้ไม่สามารถยกเลิกได้</span><span class="sxs-lookup"><span data-stu-id="60dc3-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="60dc3-110">เมื่อต้องการยืนยันสิ่งนี้ ให้เปิดรหัสงานแล้วเปิดแท็บ **ทั่วไป** ถ้างานถูกล็อคไว้ ฟิลด์ **สถานะของงาน** จะถูกตั้งค่าเป็น *อยู่ระหว่างการดำเนินการ* และฟิลด์ **ล็อคโดย** จะตั้งค่าเป็นรหัสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="60dc3-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="60dc3-111">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="60dc3-111">Resolution</span></span>

<span data-ttu-id="60dc3-112">หากต้องการยกเลิกงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="60dc3-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="60dc3-113">ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> การล้าง \> ยกเลิกงาน**</span><span class="sxs-lookup"><span data-stu-id="60dc3-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="60dc3-114">ในฟิลด์ **รหัสงาน** ให้ระบุรหัสงานที่คุณต้องการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="60dc3-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="60dc3-115">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="60dc3-115">Select **OK**.</span></span>
1. <span data-ttu-id="60dc3-116">เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการยกเลิกงาน</span><span class="sxs-lookup"><span data-stu-id="60dc3-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="60dc3-117">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยกเลิกงานของคลังสินค้าสำหรับการจัดการข้อยกเว้น](../../warehousing/cancel-warehouse-work.md)</span><span class="sxs-lookup"><span data-stu-id="60dc3-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
