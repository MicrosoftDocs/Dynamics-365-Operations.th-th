---
title: ตั้งค่าคอนฟิกพารามิเตอร์สัญญาเช่า (พรีวิว)
description: หัวข้อนี้จะอธิบายการตั้งค่าของการตั้งค่าคอนฟิกสำหรับสัญญาเช่าสินทรัพย์ เช่น ข้อมูลความปลอดภัย และการตั้งค่าการบัญชี
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4bb8372c5e4a1d7183b5d793b142fed92e833d5a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210444"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="d4833-103">ตั้งค่าคอนฟิกพารามิเตอร์สัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="d4833-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4833-104">การตั้งค่าของการตั้งค่าคอนฟิกต่างๆ มีผลกระทบต่อลักษณะการทำงานของสัญญาเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="d4833-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="d4833-105">การตั้งค่าเหล่านี้รวมถึงชื่อสมุดรายวัน พารามิเตอร์ทั่วไป และการตั้งค่าโพรไฟล์การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d4833-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="d4833-106">ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> พารามิเตอร์การเช่าสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="d4833-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="d4833-107">บนแท็บ **สัญญาเช่า** ให้เลือก FastTab **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="d4833-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="d4833-108">พารามิเตอร์ **อนุญาตการแทนที่การจัดประเภทด้วยตนเอง** จะกำหนดว่าคุณสามารถแทนที่การจัดประเภทสัญญาเช่าได้ก่อนการยืนยันกำหนดการชำระเงินหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d4833-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="d4833-109">พารามิเตอร์ **ชุดงานข้ามเอนทิตี** จะกำหนดว่าคุณสามารถลงรายการบัญชีไปยังนิติบุคคลอื่นๆ จากนิติบุคคลปัจจุบันได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="d4833-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="d4833-110">ถ้าพารามิเตอร์นี้เปิดอยู่ คุณสามารถสร้างรายการสมุดรายวันสำหรับนิติบุคคลที่คุณมีสิทธิ์เข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="d4833-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="d4833-111">ตั้งค่าตัวเลือก **อนุญาตให้ลบสัญญาเช่าที่ยืนยัน** เป็น **ใช่** เพื่ออนุญาตให้มีการลบสัญญาเช่าที่มีกำหนดการชำระเงินที่ยืนยันแล้ว</span><span class="sxs-lookup"><span data-stu-id="d4833-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="d4833-112">ไม่สามารถลบสัญญาเช่าได้ ถ้าธุรกรรมที่ลงรายการบัญชีหรือธุรกรรมที่ยังไม่ได้ลงรายการบัญชีมีการเชื่อมโยง โดยไม่คำนึงถึงการตั้งค่าตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="d4833-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="d4833-113">คุณไม่สามารถคืนค่าเรกคอร์ดสัญญาเช่า หลังจากที่มีการลบ</span><span class="sxs-lookup"><span data-stu-id="d4833-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="d4833-114">ถ้าคุณอัปโหลดเรกคอร์ดใดๆ สำหรับสัญญาเช่าที่ลบออกด้วยตนเองหรือโดยใช้เอนทิตีข้อมูล ข้อมูลที่อัปโหลดจะถือว่าเป็นข้อมูลใหม่ ไม่ใช่การอัปเดตไปยังสัญญาเช่าที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="d4833-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="d4833-115">ถ้าคุณกำหนดตัวเลือกนี้เป็น **ใช่** และชนิดของการเปลี่ยนแปลงของสมุดบัญชีเป็น **ตัวเลือกการติดตามที่สะสม A หรือ B** ระบบจะตั้งค่าฟิลด์ **อัตราดอกเบี้ยเงินกู้ส่วนเพิ่ม** เป็นค่าของฟิลด์ **อัตราดอกเบี้ยเงินกู้ส่วนเพิ่มขณะที่เปลี่ยนแปลง** เป็นหน้า **การตั้งค่าสมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="d4833-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="d4833-116">ถ้ามีการตั้งค่าตัวเลือกนี้เป็น **ไม่** อัตราในสัญญาเช่าหลักถูกตั้งค่าเป็นค่าของฟิลด์ **อัตราดอกเบี้ยเงินกู้ส่วนเพิ่ม** บนหน้า **รายละเอียดของสมุดบัญชี** โดยไม่คำนึงถึงชนิดการเปลี่ยนแปลงของสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="d4833-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="d4833-117">ตั้งค่าตัวเลือก **อนุญาตให้มีการกลับรายการธุรกรรมค่าเสื่อมราคาในสมุดบัญชีที่ปิด** เป็น **ใช่** เพื่ออนุญาตให้มีการกลับรายการธุรกรรมค่าใช้จ่ายค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="d4833-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="d4833-118">คุณสามารถกลับรายการธุรกรรมค่าใช้จ่ายได้ แม้ว่าจะมีการปิดรุ่นของสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="d4833-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4833-119">เราขอแนะนำให้คุณตั้งค่าตัวเลือกนี้เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="d4833-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="d4833-120">การตั้งค่าของตัวเลือกนี้จะใช้เป็นการตรวจสอบความถูกต้องและการควบคุม เพื่อป้องกันไม่ให้มีการคิดค่าเสื่อมราคารุ่นของสมุดบัญชีที่ปิดโดยบังเอิญ</span><span class="sxs-lookup"><span data-stu-id="d4833-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="d4833-121">โดยการตั้งค่าตัวเลือกเป็น **ไม่** คุณช่วยในการรักษามูลค่าตามบัญชีสุทธิและในการคำนวณค่าเสื่อมราคาในอนาคตให้ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d4833-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]