---
title: จัดประเภทส่วนระยะสั้นของหนี้สินสัญญาเช่าใหม่
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างรายการสมุดรายวันรายเดือนเพื่อจัดประเภทส่วนของหนี้สินสัญญาเช่าเป็นระยะสั้น
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9189033987a3072c7122e1a198768d9de6aa2a52
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254094"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="35111-103">จัดประเภทส่วนระยะสั้นของหนี้สินสัญญาเช่าใหม่</span><span class="sxs-lookup"><span data-stu-id="35111-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35111-104">หัวข้อนี้จะอธิบายถึงวิธีการสร้างรายการสมุดรายวันรายเดือนเพื่อจัดประเภทส่วนของหนี้สินสัญญาเช่าเป็นระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="35111-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="35111-105">เมื่อกำหนดการที่เลือกไว้ในกระบวนการชุดงานจะเป็น **การจัดประเภทหนี้สินสัญญาเช่าระยะสั้น** จะมีการสร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="35111-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="35111-106">รายการนี้ใช้ในการลงรายการบัญชีส่วนของหนี้สินสัญญาเช่าปัจจุบันในวันสุดท้ายของเดือน</span><span class="sxs-lookup"><span data-stu-id="35111-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="35111-107">ในเวลาเดียวกัน จะมีการลงรายการบัญชีการกลับรายการในวันแรกของเดือนถัดไป</span><span class="sxs-lookup"><span data-stu-id="35111-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="35111-108">โดยมีการแสดงผลของหนี้สินสัญญาเช่าระยะสั้นบนกำหนดการการตัดบัญชีหนี้สิน</span><span class="sxs-lookup"><span data-stu-id="35111-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="35111-109">เมื่อลงรายการบัญชีรายการสมุดรายวัน คอลัมน์ **การจัดประเภทของหนี้สินสัญญาเช่าระยะสั้น** ที่สร้างจะพร้อมใช้งาน และรหัสสมุดรายวันจะถูกเติมด้วยในกำหนดการด้วย</span><span class="sxs-lookup"><span data-stu-id="35111-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="35111-110">เมื่อต้องการสร้างและลงรายการบัญชีรายการสมุดรายวันการจัดประเภทหนี้สินในระยะสั้น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="35111-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="35111-111">ไปที่ **การเช่าสินทรัพย์ \> ประจำงวด \> การสร้างสมุดรายวันชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="35111-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="35111-112">ในกล่องโต้ตอบ **การสร้างสมุดรายวันชุดงาน** ในฟิลด์ **เลือกกำหนดการ** ให้เลือก **จัดประเภทหนี้สินสัญญาเช่าระยะสั้น**</span><span class="sxs-lookup"><span data-stu-id="35111-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="35111-113">ในฟิลด์ **กลุ่มสัญญาเช่า** ให้เลือกกลุ่มสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="35111-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="35111-114">อีกทางหนึ่งคือ ในฟิลด์ **รหัสสมุดบัญชี** ให้เลือกรหัสสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="35111-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="35111-115">เปิดพารามิเตอร์ **การลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="35111-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="35111-116">อีกทางหนึ่งคือ ถ้าควรสร้างรายการแล้วแต่ยังไม่ได้ลงรายการบัญชี ให้ปล่อยพารามิเตอร์นี้ปิด</span><span class="sxs-lookup"><span data-stu-id="35111-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="35111-117">เปิดใช้งานพารามิเตอร์ **การแสดงตัวอย่างก่อนที่จะลงรายการบัญชี** เพื่อดูรายการก่อนที่จะมีการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="35111-117">Turn on the **Preview before posting** parameter to view the entry before it's posted.</span></span>
6. <span data-ttu-id="35111-118">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="35111-118">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]